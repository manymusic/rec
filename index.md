---
title: Current progress
layout: home
nav_order: 0
---

# Overview of the current progress
Here, the current (04-Feb-2026 18:36:42 CE[S]T) progress of the EXG data acquisition of the [ManyMusic](https://manymusic.net/) project is shared. Please direct any questions to [Dr. Seung-Goo Kim](mailto:seung-goo.kim@ae.mpg.de).

## Current recordings

![recordings](figs/run-prog.png)
<br><small>Each box represents a run. *GREY*: Yet to be done. *RED*: With major issues like a wrong song was played and so on. Needs to be rerun. *YELLOW*: With minor issues like the StimTrak was turned off. No need to rerun. *GREEN*: All good (but possibly with "normal" artefacts.</small>

## Overall emotional responses
![emo-ridge](figs/emo-ridges.png)

<small>Overall ratings pooled across all subjects. White bands mark 95%-confidence intervals. White circles mark arithmetic means (of ordinal variables! yes, I know). At the bottom, subject-wise Z-scored values are plotted (i.e., the average across all sources within a subject is zero).*jam*=Jamendo, *boh*=Bohemian, *app*=Apple. </small>
## Average channel goodness percentages

![recordings](figs/avg-isgood.png)
<br><small>Percentages of "GOOD" runs for each channel are plotted. *EEG*: "BAD" channels were identified by EEGLAB/CLEAN_ARTIFACTS(). *EXG*: "BAD" cahnnels were identified by value ranges (and expected peak frequencies for RESP & PULSE).</small>


## Channel goodness per session

![isgood](figs/avg-isgood-sess.png)
<br><small> *EEG*: "BAD" channels were identified by EEGLAB/CLEAN_ARTIFACTS().</small>

## Average r^2 with movements

![recordings](figs/grandvag-movr2.png)
<br><small>Averaged zero-lag r^2 with movements. *acc?*: acceleration-X/Y/Z. *vel?*: velocity-X/Y/Z (i.e., the integration of acceleration). </small>

## Session-averaged zero-lag correlation matrices
![corr-matrices](figs/corr-matrices.png)

<small>Zero-lag correlation matrices of EEG and EXG channels after detrending. *EEG*: 32 channels in the International 10-20 System. *EXG*: EOGv, EOGh, EXGs, EXGf, acc-X/Y/Z, vel-X/Y/Z. </small>
