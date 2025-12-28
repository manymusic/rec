---
title: ICA kitchen
layout: page
nav_order: 5
has_children: true
---

# Denoising using EEGLAB

ICA-denoising is a half-art, half-science procedure.
There is no single best practice that works for all datasets. As we always do, we have to cook it ourselves, adjusting the recipe according to the ingredients at hand in the "ICA kitchen".

Here, I summarize the preprocessing steps implemented in `musafx-exg/maexg_prep()` function in our analysis pipeline, which prepares the EEG data for ICA denoising using custom functions and EEGLAB (v2025.0):

1. **Filtering**: Band-pass filtering (1-100 Hz) using `EEGLAB/pop_eegfiltnew()`.
2. **EXG-GLM**: Regressing out the EXG channels (EOGv, EOGh, EMGs, EMGf, ACC_X, ACC_Y, ACC_Z, VEL_X, VEL_Y, VEL_Z) from the EEG channels using a general linear model.
3. **Downsampling**: Downsampling to 250 Hz using `EEGLAB/pop_resample()`.
4. **Clean raw data**: Cleaning the raw data using `EEGLAB/clean_artifacts()` and interporating removed channels using spherical interpoation using `EEGLAB/eeg_interp()`.
5. **Re-reference**: Re-referencing to the common average reference using `EEGLAB/pop_reref()`.
6. **IC-Label**: Running ICA using `EEGLAB/pop_runica()` in EEGLAB (extended Infomax).
7. **ICA cooking**: Identifying artifact ICs using `EEGLAB/iclabel()` plugin in EEGLAB.
8. **Bad IC removal**: Removing the artifact ICs and reconstructing the EEG using `EEGLAB/pop_subcomp()`.

The band-pass cutoffs (1-100 Hz) in step 1 were chosen to be consistent with the IC-Label training data filtering ([Pion-Tonachini+.2019](https://doi.org/10.1016/j.neuroimage.2019.05.026)).

The details of step 2 (regressing out EXG channels) are described in [Regressing EXG out from EEG](denoising-exg.md).

The step 7 (ICA cooking) is actually a semi-automatic procedure. EEGLAB's IC-Label provides the probability of each IC belonging to each of the seven classes (Brain, Muscle, Eye, Heart, Line Noise, Channel Noise, Other), but its performance may vary depending on the dataset. Even in the original paper ([Pion-Tonachini+.2019](https://doi.org/10.1016/j.neuroimage.2019.05.026)), the accuracy for Muscle ICs was only about 80% but other classes were below 60%. Therefore, it is still recommended to manually inspect the ICs (topography, power spectrum, and timeseries) before removing them.

