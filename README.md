# CoinTrace

Unsupervised and graph-based clustering of Bitcoin transaction data to surface patterns consistent with illicit fund movement across unlabeled addresses.

## Overview

CoinTrace explores how far unsupervised and graph-based clustering methods can go in flagging suspicious Bitcoin transaction behavior without relying on ground-truth labels during training. Labels in the dataset are reserved strictly for evaluation, keeping the core task genuinely unsupervised.

## Dataset

**Source:** [Elliptic Dataset](https://www.kaggle.com/datasets/ellipticco/elliptic-data-set) (classic version, 3 CSVs)

| File | Description |
|------|-------------|
| `elliptic_txs_features.csv` | Transaction-level features |
| `elliptic_txs_classes.csv` | Labels (illicit / licit / unknown) — used for evaluation only |
| `elliptic_txs_edgelist.csv` | Transaction graph edges |

Data is retrieved programmatically via `kagglehub` rather than checked into the repo.

## Repository Structure

```
cointrace/
├── data/                 # Raw and processed data (gitignored)
├── notebooks/            # Exploratory analysis and experiments
├── src/                  # Core pipeline code
│   ├── data_loading.py
│   ├── features.py
│   ├── graph.py
│   ├── clustering.py
│   └── evaluation.py
├── requirements.txt
└── README.md
```

## Installation

```bash
git clone https://github.com/<your-username>/cointrace.git
cd cointrace
pip install -r requirements.txt
```

Dataset download requires a Kaggle account and API credentials configured for `kagglehub` (see [kagglehub docs](https://github.com/Kaggle/kagglehub) for setup).

## Roadmap

| # | Stage | Status |
|---|-------|--------|
| 1 | Environment setup | Complete |
| 2 | Data understanding | Complete |
| 3 | Exploratory data analysis | In progress |
| 4 | Data cleaning | Planned |
| 5 | Feature engineering | Planned |
| 6 | Graph construction | Planned |
| 7 | Baseline clustering | Planned |
| 8 | Graph-based clustering | Planned |
| 9 | Evaluation against labels | Planned |
| 10 | Explainability | Planned |
| 11 | Final report & packaging | Planned |

## Tech Stack

- Python
- pandas, scikit-learn
- networkx (graph construction)
- kagglehub (dataset access)

*Additional libraries will be added as feature engineering and clustering stages are implemented.*

## Status

Active development. This README will be updated as each stage of the roadmap is completed.

## License

MIT
