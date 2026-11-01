# ELEC5305 Final Project

## Acoustic Cues and Listener Variability in Gender-Related Voice Perception

Meiqi Song | Student ID: 550200770

This project examines how pitch and vocal-tract cues relate to listeners' gender-related voice judgments. It uses 240 recordings from 20 talkers and published perception summaries. The response variable is the percentage of “man” responses, not the speaker's gender identity.

## Report, code and video

- [Final report (PDF)](ELEC5305_Final_Meiqi_Song.pdf)
- [MATLAB live script](Final_MeiqiSong.mlx)
- [Demonstration video](https://youtu.be/cVo23rYBB2s)
- [Project website](https://meiqi0747.github.io/elec5305-project-550200770/)
- [Code repository](https://github.com/meiqi0747/elec5305-project-550200770)

## Requirements

Use MATLAB R2024a or later for this live script. Its local MFCC function appears before later script sections; earlier MATLAB releases require local functions at the end of scripts. See [MathWorks documentation](https://www.mathworks.com/help/matlab/matlab_prog/local-functions-in-scripts.html).

The code implements the MFCC calculation and ridge regression directly. Static inspection found no calls requiring Audio Toolbox or Statistics and Machine Learning Toolbox. This packaging check did not rerun MATLAB or test all MATLAB releases.

## Files and data

Keep the following layout after downloading and extracting the repository:

```text
Final_MeiqiSong.mlx
ELEC5305_Final_Meiqi_Song.pdf
README.md
Final_Analysis_Table.csv
Final_Condition_Summary.csv
Final_Model_Results.csv
Data/
    MunsonDolquist2025_SummaryPerceptionData.xlsx
    required_audio_files.txt
    [240 WAV files listed in required_audio_files.txt]
Final_Results/
    [14 figure PNGs and 7 result CSVs]
```

The Data folder contains the workbook and the 240 WAV files named in its Data sheet. The audio filenames and condition suffixes must remain unchanged. Two additional WAV files in the local working folder were not referenced by the workbook and are not included in this package.

## How to run

1. On GitHub, select Code > Download ZIP and extract it.
2. Open MATLAB and set Current Folder to the extracted folder containing Final_MeiqiSong.mlx. The script uses `pwd`, so this step is required.
3. Open Final_MeiqiSong.mlx and click Run to execute the whole file.
4. Check that the console reports 240 stimulus records and zero missing WAV files. Resolve missing files before interpreting results; the script can skip missing audio.
5. Wait for `Part 12 completed successfully.` The script writes the three root CSVs and the figure and table outputs in Final_Results. Running it again overwrites these generated results.

## Analysis and example results

The analysis compares F0, estimated vocal-tract length (VTL), and 26 MFCC summary features. Five-fold validation holds out four complete talkers in each fold. Standardisation is fitted on training data. The ridge penalty is 1.

Values below are rounded from Final_Model_Results.csv:

| Features | RMSE (percentage points) | R-squared |
|---|---:|---:|
| F0 only | 18.7749 | 0.7122 |
| VTL only | 29.6508 | 0.2823 |
| F0 + VTL | 15.7750 | 0.7969 |
| F0 + VTL + MFCC | 18.4077 | 0.7234 |

F0 and VTL together perform best in this comparison. Adding MFCCs does not improve held-out prediction. These are predictions of listener responses, not gender-classification accuracy.

The report uses Figures 1, 3, 5, 12, 13 and 14. Original figure numbers are retained to match the code. Earlier exploratory outputs are also included. The code's variable `ListenerAgreement` measures response concentration; it is not a measure of correct responses or a formal reliability coefficient.

The three listener groups are equally weighted when computing the overall response. There are only 20 talkers, and the sentences differ across conditions. Condition comparisons therefore do not isolate acoustic manipulation from sentence content.

## Data and source acknowledgement

The recordings, listener responses and published acoustic measurements originate from Munson and Dolquist (2025). They are not newly collected data for this project. Project analysis adds MFCC summaries, descriptive comparisons, regression evaluation and bootstrap summaries.

Munson, B., & Dolquist, D. V. (2025). Journal of Speech, Language, and Hearing Research, 68(8), 3798–3822. Original publication: https://doi.org/10.1044/2025_JSLHR-24-00756

Original study materials: https://osf.io/n3twm/

The original authors retain rights in their source materials; this repository does not grant a new licence for those materials. Further research references are listed in the report.
