---
title: Current progress
layout: home
nav_order: 1
---

# Overview of the current progress
Here, the current (27-Dec-2025 12:15:18 CE[S]T) progress of the EXG data acquisition is shared.

## Current recordings

![recordings](figs/run-prog.png)
<br><small>Each box represents a run. *GREY*: Yet to be done. *RED*: With major issues like a wrong song was played and so on. Needs to be rerun. *YELLOW*: With minor issues like the StimTrak was turned off. No need to rerun. *GREEN*: All good (but possibly with "normal" artefacts.</small>

## Average channel goodness percentages

![recordings](figs/avg-isgood.png)
<br><small>Percentages of "GOOD" runs for each channel are plotted. *EEG*: "BAD" channels were identified by EEGLAB/CLEAN_ARTIFACTS(). *EXG*: "BAD" cahnnels were identified by value ranges (and expected peak frequencies for RESP & PULSE).</small>

## Average r^2 with movements

![recordings](figs/grandvag-movr2.png)
<br><small>Averaged zero-lad r^2 with movements. *acc?*: acceleration-X/Y/Z. *vel?*: velocity-X/Y/Z (i.e., the integration of acceleration). </small>

## Session-averaged zero-lag correlation matrices
![corr-matrices](figs/corr-matrices.png)

<small>Zero-lag correlation matrices of EEG and EXG channels after detrending. *EEG*: 32 channels in the International 10-20 System. *EXG*: EOGv, EOGh, EXGs, EXGf, acc-X/Y/Z, vel-X/Y/Z. </small>
## Overall emotional responses
![emo-ridge](figs/emo-ridges.png)

<small>Overall ratings pooled across all subjects. White bands mark 95%-confidence intervals. White circles mark arithmetic means (of ordinal variables! yes, I know)*jam*=Jamendo, *boh*=Bohemian, *app*=Apple. </small>