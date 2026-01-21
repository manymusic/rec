---
title: Repair notes🛠️
layout: page
nav_order: 10
---
# Repair-on-the-fly🛠️✈️

## Why did some tracks abruptly stop during replay?🎤🙀
Updated: 2026-01-07

In fact, some of the MTG-Jamendo tracks were cropped incorrectly at the source (i.e., Jamendo). Those tracks are not available online anymore, but the faulty versions were included in the MTG-Jamendo dataset we used.

But in other cases, I was playing tracks at a wrong sampling rate. Some tracks were at 44.1 kHz, others at 48 kHz. But cleverly, when I loaded tracks at 48 kHz into MATLAB, they were meant to be resampled to 44.1 kHz.

But! I made a mistake when resampling the tracks. In my memory, the syntax was like this:
```matlab
x_new = resample(x_old, fs_old, fs_new);
```

But in fact, the correct syntax is:
```matlab
x_new = resample(x_old, fs_new, fs_old);
```
Because what it actually does is to resample the signal at the p/q times the original sampling rate in `x_new = resample(x_old, p, q)`. So, `p/q*fs_old = fs_new/fs_old*fs_old = fs_new`.

Thus, it could have been playing a bit slower than the original, but because of the bug, it was actually played even more slowly because it was then resampled at 48/44.1*48 = 52.24 kHz. 🙃

This bug caused 3 tracks to be played incorrectly, and those tracks were redone in later sessions.


## Why the batteris of the StimTrak ran out so quickly?🪫
Updated: 2026-01-21

It seems that the battery chargers at the EEGLAB1 lab were not fully functional, causing the StimTrak batteries to be not fully charged before use. Users must put only one battery in a single deck charger slot, not two batteries in one slot. Putting two batteries in one slot can cause incomplete charging of both batteries.

Use the additional charger (one with the blue LED display) to charge more than 4 batteries at once.


## Why does the ARS flag FC1/2 as BAD in some participants, consistently across sessions?
Updated: 2026-01-21

We observed that the ARS function in EEGLAB's CLEAN_ARTIFACTS() often flagged FC1 and FC2 channels as BAD in some participants, consistently across sessions (i.e., sub-07, sub-10; see [Channel-goodness-per-session]). Since the central electrodes (`*C`, `*Z`) are critical in observing auditory cortical responses, we investigated what caused such a classification by the ASR.

What are the common causes?

### ~~Are the electrodes broken?⛓️‍💥~~
Perhaps the electrodes FC1 and FC2 were faulty?
> We mostly have been using the ELEC-17 for these participants, but we see BAD channels when using other channels, and the same electrode bundle (ELEC-17) works fine for other participants. So, it is unlikely that the electrodes are faulty.

### ~~Are we gelling the electrodes right?💦~~
**Too much?** Are we using too much gel on these electrodes, causing them to be bridged together?
> [Alschuler+2014] proposed a method to identify bridged electrodes by looking at the correlation between channels. However, in our case, we do not see high correlations between FC1 and FC2 or with other channels. So, it is unlikely that the electrodes are bridged. 🤷

**Too little?** Are we using too little gel on these electrodes, causing high impedance and noisy signals?

### Because of the head shapes?💀

Could it be that their head shapes cause poor contact of those electrodes? Does the cap fit them poorly around those electrodes?

### To cut the wild goose chase short🪿
Let's look at the actual data.

|![raw-sub10](figs/example-raw-sub10.png)|![raw-sub09](figs/example-raw-sub09.png)|
|:--:|:--:|

<small>**LEFT**: Sub-10, **RIGHT**: Sub-09; Blue=raw, Red=cleaned</small>

From these segments, the amplitudes of FC1 and FC2 are low in both subjects. This maybe due to bridge, but the eBridge algorithm ([Alschuler+2014]) did not detect any bridged electrodes.




---

[Channel-goodness-per-session]: https://manymusic.net/rec/#channel-goodness-per-session
[Alschuler+2014]: https://doi.org/10.1016/j.clinph.2013.08.024