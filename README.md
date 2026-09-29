# ELEC5305 Project

## Acoustic Cues and Listener Variability in Gender-Related Voice Perception

**Student:** Meiqi Song  
**SID:** 550200770

## Project Overview

This project studies how measurable acoustic features of speech relate to gender-related voice perception.

The original project focused on comparing F0, MFCC and combined acoustic features using KNN and SVM. After receiving project feedback, the final direction was revised to focus more on the acoustic cues themselves and how they may influence listener responses.

The main acoustic features considered are:

- Fundamental Frequency (F0)
- Formant-related features
- MFCCs

The final project will also examine listener agreement and disagreement under different acoustic conditions.

## Research Question

How do fundamental frequency and vocal-tract spectral cues influence listeners’ gender-related perception of speech, and under what acoustic conditions do listeners show greater agreement or disagreement?

## Feedback 1 – Project Proposal

The first stage focused on defining the project topic, methodology and expected outcomes.

The original proposal is available here:

[ELEC5305 Project Proposal](ELEC5305%20Project%20Proposal.pdf)

## Feedback 2 – Preliminary Work

For Feedback 2, I completed a preliminary MATLAB analysis using 96 neutral speech recordings from the RAVDESS dataset.

The dataset contains:

- 24 speakers
- 48 recordings with corpus-provided male labels
- 48 recordings with corpus-provided female labels

The current MATLAB work includes:

- Audio preprocessing and resampling
- F0 extraction
- MFCC extraction
- Spectral Centroid extraction
- KNN classification
- Basic linear SVM classification
- Speaker-independent five-fold validation
- Accuracy comparison
- Confusion matrix analysis

## Preliminary Results

| Feature Set | KNN Accuracy | SVM Accuracy |
|---|---:|---:|
| F0 | 88.54% | 67.71% |
| MFCC | 81.25% | 57.29% |
| Combined | 82.29% | 55.21% |

The best preliminary result was obtained using F0 features with KNN, with an accuracy of **88.54%**.

These results are kept as preliminary work. The final project will extend the analysis to formant-related features and perceptual response data.

## Result Figures

The current result figures are stored in the `Results_Figures` folder and include:

- Mean F0 distribution
- Average F0 comparison
- MFCC comparison
- Spectral Centroid comparison
- Classification accuracy comparison
- Best-model confusion matrix

## Dataset

The preliminary analysis uses neutral speech recordings from the RAVDESS dataset.

Original dataset:

https://zenodo.org/records/1188976

Only the recordings used in the current experiment are included in this repository.

## How to Run

1. Download or clone this repository.
2. Open the project folder in MATLAB.
3. Keep the `Audio_Speech_Actors_01-24` folder in the same project folder as the MATLAB Live Script.
4. Open `Feedback2_Meiqi_Song.mlx`.
5. Run the Live Script from the beginning.

The script performs preprocessing, feature extraction, preliminary classification and result generation.

## Current Files

- `ELEC5305 Project Proposal.pdf` – original project proposal
- `Feedback2_Meiqi_Song.mlx` – current MATLAB implementation
- `Audio_Speech_Actors_01-24` – speech recordings used in the preliminary experiment
- `Results_Figures` – current result figures

## Next Stage

For the final project, I will:

- Add formant extraction
- Use perceptual response data
- Compare F0 and formant-related cues
- Analyse listener agreement and disagreement
- Extend the literature review
- Complete the final analysis and report
