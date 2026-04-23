# Swing & Signal

**Motion meets biosignals** — a single notebook pipeline for **racket-sports** multivariate time series (UCR-style ARFF) and **ECG** heartbeat data (MIT-BIH multi-class, PTB binary). Exploratory analysis, hand-crafted features, and **classic ML** (Random Forest, SVM, XGBoost) plus a **PyTorch** section for neural networks.

Main notebook: **`swing_and_signal.ipynb`** (sections **3.1** EDA, **3.2** feature extraction and classical models, **3.3** neural nets, plus optional Conv1d experiments).

## Layout

```
.
├── swing_and_signal.ipynb
├── RacketSports/
├── ECG/
├── requirements.txt
└── README.md
```

## Setup

Python **3.10+** recommended.

```bash
python3 -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

Install a specific **PyTorch** / CUDA build from [pytorch.org/get-started/locally](https://pytorch.org/get-started/locally/) if needed.

Download the four ECG CSVs into `ECG/` as described in [ECG/DATA.md](ECG/DATA.md). Run from the repository root:

```bash
jupyter lab swing_and_signal.ipynb
```

## Troubleshooting

- **sktime** loads the ARFF files; with newer releases, pin versions like in `requirements.txt` or check the [sktime](https://www.sktime.net/) docs if loaders change.
- Prefer **`scikit-learn`** via `pip` / `requirements.txt` (not the `sklearn` stub on PyPI).
