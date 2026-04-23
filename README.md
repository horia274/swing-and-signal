# Swing & Signal

**Motion meets biosignals** — a single notebook pipeline for **racket-sports** multivariate time series (UCR-style ARFF) and **ECG** heartbeat data (MIT-BIH multi-class, PTB binary). Exploratory analysis, hand-crafted features, and **classic ML** (Random Forest, SVM, XGBoost) meet a **PyTorch** section for neural networks.

The main artifact is **`swing_and_signal.ipynb`**: sections **3.1** (EDA), **3.2** (feature extraction + classical models), **3.3** (neural nets), plus experimental snippets (e.g. Conv1d playground).

## Layout

```
.
├── swing_and_signal.ipynb
├── RacketSports/          # TRAIN / TEST ARFF (safe for Git)
├── ECG/                   # CSVs are large — see ECG/DATA.md
├── requirements.txt
└── README.md
```

## Setup

**Python 3.10+** recommended.

```bash
python3 -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

**PyTorch:** for GPU or a specific CUDA build, install `torch` from [pytorch.org/get-started/locally](https://pytorch.org/get-started/locally/) first if the default wheel is not what you need.

**Data:** add the four ECG CSVs under `ECG/` as described in [ECG/DATA.md](ECG/DATA.md). `mitbih_train.csv` is too large for normal GitHub uploads, so those files are listed in `.gitignore`; the RacketSports ARFF pair ships with the repo.

**Run** from the repo root (paths are relative):

```bash
jupyter lab swing_and_signal.ipynb
```

## Notes

- **sktime** is used to load ARFF; the ecosystem moves quickly — if loaders break on a new release, pin versions similar to `requirements.txt` or check the current [sktime](https://www.sktime.net/) docs.
- **Notebook installs:** the first cell may use `%pip install sklearn`; use **`scikit-learn`** on the command line (`requirements.txt` already does).
- **Datasets:** ECG data comes with PhysioNet / redistributor terms — cite and comply when you publish results.

**Why “Swing & Signal”?** It was a memorable shorthand: **swing** → racket motion (the sports time series), **signal** → ECG and IMU waveforms. If you prefer another repo title, rename the folder and this file to match—nothing in the notebook depends on the filename.
