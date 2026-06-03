[![DOI](https://img.shields.io/badge/DOI-10.82901%2Fnemar.nm000236-blue)](https://doi.org/10.82901/nemar.nm000236)

# Dataset of an EEG-based BCI experiment in Virtual Reality using P300

Dataset of an EEG-based BCI experiment in Virtual Reality using P300.

## Dataset Overview

- **Code**: Cattan2019-VR
- **Paradigm**: p300
- **DOI**: https://doi.org/10.5281/zenodo.2605204
- **Subjects**: 21
- **Sessions per subject**: 1
- **Events**: Target=2, NonTarget=1
- **Trial interval**: [0, 1.0] s
- **Runs per session**: 60
- **Session IDs**: PC, VR
- **File format**: mat, csv
- **Contributing labs**: GIPSA-lab

## Acquisition

- **Sampling rate**: 512.0 Hz
- **Number of channels**: 16
- **Channel types**: eeg=16
- **Channel names**: Fp1, Fp2, Fc5, Fz, Fc6, T7, Cz, T8, P7, P3, Pz, P4, P8, O1, Oz, O2
- **Montage**: 10-10
- **Hardware**: g.USBamp (g.tec, Schiedlberg, Austria)
- **Software**: OpenVibe
- **Reference**: right earlobe
- **Ground**: AFZ
- **Sensor type**: wet electrodes
- **Line frequency**: 50.0 Hz
- **Online filters**: no digital filter applied
- **Cap manufacturer**: EasyCap
- **Cap model**: EC20

## Participants

- **Number of subjects**: 21
- **Health status**: healthy
- **Age**: mean=26.38, std=5.78, min=19.0, max=44.0
- **Gender distribution**: male=14, female=7
- **BCI experience**: varied gaming experience: some played video games occasionally, some played First Person Shooters; varied VR experience from none to repetitive

## Experimental Protocol

- **Paradigm**: p300
- **Number of classes**: 2
- **Class labels**: Target, NonTarget
- **Study design**: randomized session order (PC vs VR); limit eye blinks, head movements and face muscular contractions
- **Feedback type**: visual
- **Stimulus type**: flashing white crosses in 6x6 matrix
- **Stimulus modalities**: visual
- **Primary modality**: visual
- **Mode**: offline
- **Training/test split**: False
- **Instructions**: focus on a red-squared target symbol while groups of six symbols flash
- **Stimulus presentation**: description=6x6 matrix of white crosses; groups of 6 symbols flash; each symbol flashes exactly 2 times per repetition, platform=Unity engine exported to PC and VR

## HED Event Annotations

Schema: HED 8.4.0 | Browse: https://www.hedtags.org/hed-schema-browser

```
  Target
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Target

  NonTarget
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Non-target

```
## Paradigm-Specific Parameters

- **Detected paradigm**: p300
- **Number of targets**: 1
- **Number of repetitions**: 12

## Data Structure

- **Trials**: {'target': 120, 'non_target': 600}
- **Trials per class**: target=120, non_target=600
- **Blocks per session**: 12
- **Trials context**: per session: 12 blocks × 5 repetitions × 12 flashes per repetition (2 target, 10 non-target)

## Preprocessing

- **Data state**: raw EEG with software tagging via USB (note: tagging introduces jitter and latency - mean 38ms in PC, 117ms in VR)
- **Preprocessing applied**: False
- **Notes**: mean tagging latency: ~38 ms in PC, ~117 ms in VR due to different hardware/software setup; these latencies should be used to correct ERPs

## Signal Processing

- **Classifiers**: xDAWN, Riemannian
- **Feature extraction**: Covariance/Riemannian, xDAWN

## Cross-Validation

- **Evaluation type**: cross_session

## BCI Application

- **Applications**: speller
- **Environment**: PC and Virtual Reality (VRElegiant HMD with Huawei Ascend Mate 7 smartphone)
- **Online feedback**: False

## Tags

- **Pathology**: Healthy
- **Modality**: Visual
- **Type**: Perception

## Documentation

- **Description**: EEG recordings of 21 subjects doing a visual P300 experiment on PC and VR to compare BCI performance and user experience
- **DOI**: 10.5281/zenodo.2605204
- **Associated paper DOI**: hal-02078533v3
- **License**: CC-BY-4.0
- **Investigators**: Grégoire Cattan, Anton Andreev, Pedro Luiz Coelho Rodrigues, Marco Congedo
- **Senior author**: Marco Congedo
- **Institution**: GIPSA-lab
- **Department**: GIPSA-lab, CNRS, University Grenoble-Alpes, Grenoble INP
- **Address**: GIPSA-lab, 11 rue des Mathématiques, Grenoble Campus BP46, F-38402, France
- **Country**: FR
- **Repository**: Zenodo
- **Data URL**: https://doi.org/10.5281/zenodo.2605204
- **Publication year**: 2019
- **Funding**: IHMTEK Company (Interaction Homme-Machine Technologie)
- **Ethics approval**: Ethical Committee of the University of Grenoble Alpes (Comité d'Ethique pour la Recherche Non-Interventionnelle)
- **Acknowledgements**: promoted by the IHMTEK Company
- **Keywords**: Electroencephalography (EEG), P300, Brain-Computer Interface (BCI), Virtual Reality (VR), experiment

## Abstract

Dataset contains electroencephalographic recordings on 21 subjects doing a visual P300 experiment on PC and VR. The visual P300 is an event-related potential elicited by a visual stimulation, peaking 240–600 ms after stimulus onset. The experiment compares P300-based BCI on PC vs VR headset (passive HMD with smartphone) concerning physiological, subjective and performance aspects. EEG recorded with 16 electrodes. Experiment conducted at GIPSA-lab in 2018.

## Methodology

Two randomized sessions (PC and VR). Each session: 12 blocks of 5 repetitions. Each repetition: 12 flashes of groups of 6 symbols, ensuring each symbol flashes exactly 2 times. Target flashes twice per repetition (2 target flashes), non-target flashes 10 times. Random feedback given after each repetition (70% expected accuracy). P300 interface: 6x6 matrix of white flashing crosses with red-squared target. VR used passive HMD (VRElegiant) with Huawei Mate 7 smartphone. IMU deactivated to prevent drift. Unity engine used for identical visual stimulation across PC and VR.

## References

G. Cattan, A. Andreev, P. L. C. Rodrigues, and M. Congedo (2019). Dataset of an EEG-based BCI experiment in Virtual Reality and on a Personal Computer. Research Report, GIPSA-lab; IHMTEK. https://doi.org/10.5281/zenodo.2605204

.. versionadded:: 0.5.0
Appelhoff, S., Sanderson, M., Brooks, T., Vliet, M., Quentin, R., Holdgraf, C., Chaumon, M., Mikulan, E., Tavabi, K., Hochenberger, R., Welke, D., Brunner, C., Rockhill, A., Larson, E., Gramfort, A. and Jas, M. (2019). MNE-BIDS: Organizing electrophysiological data into the BIDS format and facilitating their analysis. Journal of Open Source Software 4: (1896). https://doi.org/10.21105/joss.01896

Pernet, C. R., Appelhoff, S., Gorgolewski, K. J., Flandin, G., Phillips, C., Delorme, A., Oostenveld, R. (2019). EEG-BIDS, an extension to the brain imaging data structure for electroencephalography. Scientific Data, 6, 103. https://doi.org/10.1038/s41597-019-0104-8

---
Generated by MOABB 1.5.0 (Mother of All BCI Benchmarks)
https://github.com/NeuroTechX/moabb
