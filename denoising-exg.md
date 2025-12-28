---
title: Regressing EXG out
layout: page
nav_order: 3
has_children: true
---

# Regressing EXG out from EEG
Because of the proximity to the EEG electrodes, the frontalis and temporalis muscles generate strong electromyographic (EMG) artefacts in EEG recordings. 
Their spectral and topographical characteristics in EEG recordings have been well-documented in [Goncharova *et al.* (2003). *Clin. Neurophysiol.*](https://doi.org/10.1016/S1388-2457(03)00070-2) as:

![Spatial and spectral characteristics of EMG artefacts in EEG](https://ars.els-cdn.com/content/image/1-s2.0-S1388245703000932-gr6.jpg)<br><small>Fig. 6 in [Goncharova *et al.* (2003)](https://doi.org/101016/S1388-2457(03)00070-2). *CAR*: Common Average Reference.</small>

In our dataset, the lower band (0.5-30 Hz) EEG signals showed strong *"frontalis artefacts"* whereas the higher band (30-50 Hz) EEG signals showed strong *"temporalis artefacts"*.

In addition, the temporal electrodes (T7 and T8) showed strong power in the higher band.
This is consistent with the "muscle activity topography" shown below from [Ma *et al.* (2012). *Clin. Neurophysiol.*](https://doi.org/10.1016/j.clinph.2011.11.083), where the  CO2-induced gamma band (24-50 Hz) power in the T7 and T8 channels was significantly reduced by their ICA-based EMG denoising algorithm.

![muscle-ICs](https://ars.els-cdn.com/content/image/1-s2.0-S1388245711009084-gr3.jpg)<br><small>Fig. 3 in [Ma *et al.* (2012)](https://doi.org/10.1016/j.clinph.2011.11.083). *CT1*: clinical trial 1. *CT2*: clinical trial 2. *UER*: unilateral left ear reference. *LER*: left ear reference. *CAR*: common average reference. </small>.