# ECG CSV data (not stored in Git)

These files are required by `swing_and_signal.ipynb` and are **ignored by Git** because `mitbih_train.csv` is larger than GitHub’s per-file limit (~100 MB).

Place the following four files in this directory:

| File | Role |
|------|------|
| `mitbih_train.csv` | MIT-BIH arrhythmia (train) |
| `mitbih_test.csv` | MIT-BIH arrhythmia (test) |
| `ptbdb_normal.csv` | PTB Diagnostic ECG — normal beats |
| `ptbdb_abnormal.csv` | PTB Diagnostic ECG — abnormal beats |

## Where to get the data

Processed MIT-BIH and PTB CSVs are distributed on several mirrors (e.g. Kaggle) under names such as “MIT-BIH Arrhythmia” / “PTB Diagnostic ECG”. Search for datasets that ship exactly these filenames and column layout (last column = label).

Original scientific sources (for citation):

- MIT-BIH Arrhythmia Database — PhysioNet  
  https://physionet.org/content/mitdb/
- PTB Diagnostic ECG Database — PhysioNet  
  https://physionet.org/content/ptbdb/

Ensure you comply with each provider’s license and citation requirements when publishing results.
