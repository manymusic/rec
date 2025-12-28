---
title: Regressing EXG out
layout: page
nav_order: 3
has_children: true
---

# Regressing EXG out from EEG
Because of the proximity to the EEG electrodes, the frontalis and temporalis muscles generate strong electromyographic (EMG) artefacts in EEG recordings. 
Their spectral and topographical characteristics in EEG recordings are well-documented in [Goncharova+.2003] as:

![Spatial and spectral characteristics of EMG artefacts in EEG](https://ars.els-cdn.com/content/image/1-s2.0-S1388245703000932-gr6.jpg)<br><small>Fig. 6 in [Goncharova+.2003]. *CAR*: common average reference.</small>

Based on [Goncharova+.2003], our dataset (e.g., [sub-01])seems to show typical *"frontalis artefacts"* in the lower frequency band (0.5-30 Hz) and *"temporalis artefacts"* in the higher frequency band (30-50 Hz).

In addition, our dataset also shows the temporal electrodes (T7 and T8) with strong power in the higher (30-50 Hz) band (e.g. [sub-03]).
This is consistent with the "muscle activity topography" shown below from [Ma+.2012], where the  CO2-induced gamma band (24-50 Hz) power in the T7 and T8 channels was significantly reduced by their ICA-based EMG denoising algorithm.

![muscle-ICs](https://ars.els-cdn.com/content/image/1-s2.0-S1388245711009084-gr3.jpg)<br><small>Fig. 3 in [Ma+.2012]. *CT1*: clinical trial 1. *CT2*: clinical trial 2. *UER*: unilateral left ear reference. *LER*: linked-ear reference. *CAR*: common average reference. </small>.

Therefore, we attempted to regress out the EXG channels (vertical and horizontal electrooculography \[EOGv, EOGh\], smiling and frowning EMGs \[EMGs, EMGf\], and X-/Y-/Z-accelerometer \[ACC_X, ACC_Y, ACC_Z\]) from the EEG channels by using a multiple regression model for each EEG channel:
$$\mathbf{y}^{[i]} = \mathbf{X}\mathbf{b}^{[i]} + \mathbf{e}^{[i]}$$
where $\mathbf{y}^{[i]}$ is the timeseries of the $i$-th EEG channel, $\mathbf{b}^{[i]}$ is the coefficient vector, $\mathbf{X}$ is a matrix of the EXG channels including an intercept, and $\mathbf{e}^{[i]}$ is the residual timeseries.
The residuals were then used as the *"denoised"* EEG signals.

[sub-01]: denoising-exg-sub01.md
[sub-03]: denoising-exg-sub03.md
[Goncharova+.2003]: https://doi.org/10.1016/S1388-2457(03)00093-2
[Ma+.2012]: https://doi.org/10.1016/j.clinph.2011.11.083 