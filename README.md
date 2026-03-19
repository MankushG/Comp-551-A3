# COMP 551 - Assignment 3

Outlier detection/classification pipeline for grouped image data (`5 x 32 x 32` per sample), implemented in a notebook workflow. Includes baseline logistic regression and optional PyTorch experimentation.

## Project Structure

```text
├── assignment3.ipynb      # Main notebook (data loading, training, evaluation, Kaggle export)
├── datasets/
│   ├── x_train.npy
│   ├── y_train.npy
│   ├── x_test.npy
│   └── y_test.npy
├── pyproject.toml         # uv project metadata and top-level dependencies
├── uv.lock                # Locked dependency graph (reproducible installs)
├── requirements.txt       # Simple pip-friendly dependency list
├── .python-version        # Pinned Python version (3.12)
└── README.md
```

## Setup

### Option 1: uv (recommended)

Install `uv` if needed:

```bash
pip install uv
```

Get into the project directory:

```bash
cd Comp-551-A3
```

Install dependencies and create `.venv`:

```bash
uv sync
```

### Option 2: venv + pip

```bash
python -m venv .venv
# On Windows:
.venv\Scripts\activate
# On macOS/Linux:
source .venv/bin/activate

pip install -r requirements.txt
```

### Option 3: conda

```bash
conda create -n comp551a3 python=3.12
conda activate comp551a3
pip install -r requirements.txt
```

## Run

1. Open the notebook:

```bash
code assignment3.ipynb
```

2. In VS Code, select kernel:
- `Select Kernel` -> `Python Environments...`
- Choose `.venv/bin/python` (from this project)

3. Run cells top-to-bottom (`Run All`).

## Configuration

- Python version is pinned in `.python-version`.
- For `uv` users, `pyproject.toml` + `uv.lock` are the source of truth.
- `requirements.txt` is kept for teammates who prefer `pip`/`conda` workflows.
