# Minimal Data Science Project

This repository is a **minimal, universal template** for Data Science and Machine Learning projects.  
It contains only the folders that **every project has in common**, avoiding unnecessary clutter.

---

## Project Structure
```text
project/
│
├── data/                  # Data artifacts (not in git, usually in .gitignore)
│   ├── external/          # Third-party sources (APIs, S3, etc.)
│   ├── raw/               # Original, immutable data dumps
│   ├── interim/           # Intermediate, cleaned versions
│   └── processed/         # Final datasets ready for modeling
│
├── models/                # Serialized trained models (e.g. .pkl, .joblib, .h5, .pt)
│
├── notebooks/             # Jupyter notebooks for exploration and experiments
│
└── src/                   # Source code
    ├── data/              # Scripts to fetch or generate data
    ├── features/          # General transformations and feature engineering
    ├── models/            # Training and evaluation scripts
    └── utils/             # Helper functions and utilities
```

---


## How to Use

1. Clone or copy this template into your new project:
   git clone <this-repo-url> my_project
   cd my_project

2. Put your data inside the data/ folder:
   - External datasets → data/external/
   - Raw dumps → data/raw/
   - Cleaned or staged versions → data/interim/
   - Final ready-to-use datasets → data/processed/

3. Write your code inside src/:
   - Data ingestion / generation → src/data/
   - Transformations and feature engineering → src/features/
   - Model training & evaluation → src/models/
   - Utilities (common helpers) → src/utils/

4. Keep experiments in notebooks/.
   - Use notebooks for exploration and EDA.
   - Once stable, migrate logic into src/.

5. Store artifacts in models/.
   - Save trained models here (.pkl, .h5, .pt, etc.).
   - Consider adding models/ to .gitignore if large.

---

## Why This Template?

- Covers the minimum common ground for all DS/ML projects: data, models, code, notebooks.
- Lightweight and easy to extend if you need more folders (e.g., reports/, configs/).
- Keeps a clear separation between code and artifacts.

---

## Notes

- Add data/ and models/ to .gitignore.
- Keep configs lightweight and versioned.
- Every artifact should be reproducible from the code in src/.

