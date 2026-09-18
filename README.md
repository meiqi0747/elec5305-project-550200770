## Comparison of Acoustic Features for Male and Female Speaker Classification Using MATLAB

**Student:** Meiqi Song

## Project Overview

This project compares different acoustic features for male and female speaker classification using MATLAB.

The feature sets are:

- F0
- MFCC
- F0 + MFCC + Spectral Centroid

KNN and linear SVM are used for classification.

## Feedback 1

The first stage focused on the project proposal and methodology.

- [ELEC5305 Project Proposal](ELEC5305%20Project%20Proposal.pdf)

## Feedback 2

The current stage uses 96 neutral speech recordings from the RAVDESS dataset, including 48 male and 48 female recordings.

The current work includes:

- Audio preprocessing
- F0, MFCC and Spectral Centroid extraction
- KNN and SVM classification
- Speaker-independent five-fold validation
- Accuracy comparison
- Confusion matrix analysis

## Preliminary Results

| Feature Set | KNN Accuracy | SVM Accuracy |
|---|---:|---:|
| F0 | 88.54% | 67.71% |
| MFCC | 81.25% | 57.29% |
| Combined | 82.29% | 55.21% |

The best current result is **88.54%** using F0 features with KNN.

## Files

- `ELEC5305 Project Proposal.pdf`
- `Feedback2_Meiqi_Song.mlx`
- `Results_Figures`

The RAVDESS dataset is not uploaded because of its size.

## Next Steps

- Precision, recall and F1-score
- Final result analysis
- Final report
