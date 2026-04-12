---
title: Technical details
layout: page
nav_order: 100
---
# Very trivial technical details 🤓

## General information
- Location: EEG LAB #1, Max Planck Institute for Empirical Aesthetics.
- Address: Grüneburgweg 14, 60322 Frankfurt am Main, Germany.
- Acquisition period: 2025-11-12 to 2026-04-XX.

## EEG Chamber
- Booth: IAC Acoustics (IAC already stands for   Industrial Acoustics Company; Germany office: IAC GmbH, Mönchengladbach), two-wall Electrically Shielded Metal Booth, 2.53 m x 2.73 m, complying ISO 8253 standard (Acoustics—Audiometric test methods) <https://www.iacacoustics.global/audiology-test-rooms/audiology-booths/>
- Air conditioning (not working during the recordings!)
- Lighting: dimmable LED spotlight (GU5.3 MR16 7.5W 621 lm 3000K, dimmable down to 10% without flickering)

## Stimulus Presentation System
### PC
- Computer: Fujitsu CELSIUS M740B (Intel Xeon ES-1620 v4 3.5 GHz, 16 GB RAM)
- Trigger port: LPT3 (0xDFF8)
- OS: Windows 10 Pro (Enterprise LTSC)
- Software: Psychtoolbox-3.0.19.16 (MATLAB R2024b) <https://github.com/Psychtoolbox-3/Psychtoolbox-3/releases/tag/3.0.19.16>

### Video
- Video card: ASUS ROG STRIX-GTX1050-O2G-GAMING (GDDR5 2 GB, r. 2016)

- In-chamber monitor: XL2402Z (BenQ, Taipei, TW), 24-inch, 1920 x 1080 pixels^2, 91 ppi, W-LED, viewing angles = 170/160 degrees [H/V], brightness = 350 cd/m^2, refresh rate = 24--144 Hz, min response time = 1 ms

### Audio
- Sound card: FireFace UCX (RME Audio, DE), connected via USB 2.0

- Software mixer: TotalMix FX (RME Audio, DE)

- In-chamber loudspeakers: KH120A studio monitors (Georg Neumann GmbH, DE), frequency range = 52 Hz – 21 kHz (+/- 3 dB), maximum output = 112.2 dB SPL, 50 watt power


### User input
- Trackball mouse: Expert Mouse (Kensington Computer Products Group, USA), wired, USB, 4 bottons and a scroll ring, 1000 DPI, black and blue colours

### Network
- No internet, only the central intranet to access the project disks ("P-drive") in the Windows file server


## EEG system
### Electrodes
- ActiCAP-snap 32-channel active electrodes (Brain Products GmbH). <https://www.brainproducts.com/solutions/acticap/>
  - Electrode type: active gel electrode with Ag/AgCl (silver/silver chloride) pellet
  - Electrode diameter: ~5.5 mm (snap holder: 2 mm)
  - Dynamic range: ± 1000 mV


### Amplifier
- 2x BrainAmp DC (Brain Products GmbH). <https://www.brainproducts.com/solutions/brainamp/>
  - Number of channels: 32
  - Sampling rate: 1000 Hz

- Powered by 3x PowerPack rechargeable battery kits (Brain Products GmbH).

### Control box
- ActiCAP ControlBox II (BrainProducts; r. 2011): controlling and powering active electrode units.


### EEG cap
- Easycap EEG Recording Cap (Brain Products GmbH). 
  - Cap type: Subtemporal
  - Cap cut: C-cut (Caucasian cut) [cf, A-cut: Asian cut for round heads]
  - Cap fabrics: High Precision (adults)
  - Cap sizes: 54, 56, 60 cm (circumference)

- EEG wire braiding style: 2 pigtails (instead of 4 pigtails).


### Impedance check system
- Target impedance: < 25 kOhm (as recommended by Brain Products GmbH for the actiCAP-snap system).

- Software: BrainVision actiCAP Control Software (Brain Products GmbH). <https://www.brainproducts.com/downloads/more-software/#acticap-control-software>

### Acquisition software

- BrainVision Recorder (Brain Products GmbH). <https://www.brainproducts.com/downloads/more-software/#brainvision-recorder>

### Consumables
- Gel

- Syringe

- Needle


## EXG system

### Electrodes & Sensors
- Multirode ring electrode B18 (EaseyCap?): Ag/AgCl 

- 3D Acceleration Sensor (Brain Products GmbH): range = ±2 g, output = 1400 mV, gain = 1450 mV/g ± 10%, dimensions = 22 x 14 x 8 mm^3, weight = 8 g.

- GSR Sensor (Brain Products GmbH): constant = 0.5 V, measurement range = 1–100 µS, gain = 25 mV/µS, output range = 0.01–4.71 V, dimensions = 15 x 36 x 36 mm^3, weight = 30 g.

- Respiration Belt (Brain Products GmbH):


- Blood Pulse Sensor (Brain Products GmbH):


- Photo Sensor (Brain Products GmbH): 

- StimTrack (Brain Products GmbH):

### Amplifier
- 1x BrainAmp ExG (Brain Products GmbH).
  - 16 bipolar channels
  - 2 bipolar ground channels
  - 8 auxiliary channels
  - DC recording is possible (i.e., no high-pass filter)

### Consumables
- NuPrep Skin Prep Gel (Walter)

- Disinfectant: 70% isopropyl alcohol

- Cotton swabs

- Cotton pads

- Disposable gloves

- Adhesive rings for ring electrodes (3M?)

- Pre-gelled Disposable Ag/AgCl Electrodes (???)

- 