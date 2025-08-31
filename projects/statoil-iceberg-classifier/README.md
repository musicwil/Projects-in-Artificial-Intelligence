# Statoil Iceberg Classifier Challenge

Satellite SAR imagery classification (Kaggle competition)

## Overview
This repository contains a reproducible notebook and supporting files to train and evaluate a classifier that distinguishes **icebergs vs. ships** in Synthetic Aperture Radar (SAR) images. The work is based on the Statoil / C-CORE Kaggle competition dataset.

## Repo structure
```
statoil-iceberg-classifier/
├── statoil_iceberg_final_08312025.ipynb
├── requirements.txt
├── .gitignore
└── LICENSE
```

## Quickstart
```bash
# 1) Create a fresh environment (optional)
python -m venv .venv && . .venv/bin/activate  # Windows: .venv\Scripts\activate

# 2) Install dependencies
pip install -r requirements.txt

# 3) Open the notebook
jupyter notebook statoil_iceberg_final_08312025.ipynb
```

## Data
You will need the SAR image data (JSON with `band_1`, `band_2`, and `inc_angle`). Place the downloaded files under `data/` and adjust any paths in the notebook accordingly.

## Results
Key metrics, model choices, and plots are documented inside the notebook.

## License
MIT — see `LICENSE`.
