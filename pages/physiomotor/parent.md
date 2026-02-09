---
title: Physiomotor responses
layout: page
nav_order: 8
has_children: true
---

# Physiomotor responses
Let's analyse the neurophysiological and motor data as "emotional responses" rather than "EEG artefacts".

## Possible response types
- [ ] vEOG: blink rates
- [ ] hEOG: Mouse-cursor-locked horizontal EOG? meaningless?
- [ ] facial EMG: smiling and frowning?
- [ ] SCR: event-related phasic responses
- [ ] RESP: breathing rate variability?
- [ ] PULSE: heart rate variability?
- [ ] ACC: frequency-tagging: magnitude; or phase-locking.

## TODOs
- [ ] Neurokit2 preprocessing
- [X] Motor-beat coherence with tempoCNN (but not too convincing)
- [X] BEAT-THIS! (ismir-2024 SOTA) for beat tracking
- [ ] Jerk beat contrast 

# Motor-beat coherence
* [Toiviainen & Carlson (2021)](https://doi.org/10.1525/mp.2022.39.3.249) proposed a wavelet tensor decomposition to analyse motion-capture data acquired during spontaneous dance to musical excerpts. *[BUT DO I NEED IT?]*

* [Ito et al. (2022)](https://doi.org/10.1126/sciadv.abo7019) showed spontaneous beat synchronization in rats using "jerk (dA/dt) beat contrast". This time-based methods requires a beat annotation. (but frequency tagging also needs a tempo estimation, and the assumption of constant tempo). *[HMMPH!]*

