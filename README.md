# Data Cleaning

A small project for exploring and cleaning tabular data (example: crime dataset).

## Contents

- `cleaning.ipynb` — Jupyter notebook with the data-cleaning workflow.
- `data/crime.csv` — Example dataset used by the notebook.

## Requirements

- Python 3.13 (this repository's `environment.yml` is configured for 3.13)
- Conda (recommended) or a Python virtual environment manager (`venv` or `poetry`).

## Quick start

1. Create and activate an environment (Conda, pip/venv, or Poetry — see options below).
2. Install dependencies.
3. Launch the notebook:

```bash
jupyter notebook cleaning.ipynb
```

Open the notebook in your browser or in VS Code to run the cleaning steps.

## Installation options

Option A — Conda (recommended)

```bash
# create the environment from the provided file
conda env create -f environment.yml

# activate it (replace `data-cleaning` with the env name defined in environment.yml)
conda activate data-cleaning
```

If you prefer to create the environment manually:

```bash
conda create -n data_environment python=3.13
conda activate data_environment
conda install pandas numpy jupyter
```

Option B — pip + venv (Windows example)

If you don't use Conda, create a virtual environment and install via `pip`.

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1    # PowerShell
# or .venv\Scripts\activate      # cmd.exe
pip install --upgrade pip
# install from requirements.txt if you have one
pip install -r requirements.txt
```

If this repository does not include a `requirements.txt`, you can install the minimal packages used by the notebook:

```bash
pip install pandas numpy jupyter matplotlib seaborn
```

Option C — Poetry

Use `poetry` to manage a virtual environment and dependencies.

```bash
poetry init --no-interaction
poetry add pandas numpy jupyter matplotlib seaborn
poetry shell
jupyter notebook cleaning.ipynb
```

If you already have a `pyproject.toml`, run `poetry install`.

## Creating a `requirements.txt` from a Conda environment

If you created the environment with Conda and want a `requirements.txt` for `pip` users:

```bash
conda activate data_environment
pip freeze > requirements.txt
```

Note: `pip freeze` may include packages not available on PyPI or platform-specific builds; prefer Conda for reproducing full environments.

## Usage

- Launch `cleaning.ipynb` with Jupyter and run the notebook cells to reproduce the cleaning steps.
- The notebook reads data from `data/crime.csv` (update the path in the notebook if your data is elsewhere).

## Notes

- This repository is a focused demo for data cleaning; adapt dependency versions in `environment.yml` or `pyproject.toml` to match your environment.
- If you'd like, I can also add a `requirements.txt` or `pyproject.toml` with exact dependencies — tell me which tool you prefer.

## Files

- [cleaning.ipynb](cleaning.ipynb)
- [data/crime.csv](data/crime.csv)
- [environment.yml](environment.yml)

## Cleaned Files

- [cleaned_data/crime.csv](cleaned_data/crime.csv)
- [cleaned_data/crime.xlsx](cleaned_data/crime.xlsx)
