# Argus

Intelligent Cyberattack Analysis System, built for IT7009 Artificial Intelligence (Selected Project Brief #2).

The project analyses labelled network-flow records (46 numerical features, 33 cyberattack classes) using supervised classification and unsupervised clustering. The notebook is organised by phase and currently covers **Phase 1: Data Cleaning and Preprocessing**.

## Requirements

- [uv](https://docs.astral.sh/uv/) (manages Python and the virtual environment)
- Python 3.14 (uv can install it for you)
- Main libraries: pandas, numpy, matplotlib, scikit-learn, ipykernel

## Setup

Clone the repository and let uv build the environment:

```bash
git clone https://github.com/MR-Goldenyt/Argus.git
cd Argus

# Only needed if you don't have Python 3.13 yet
uv python install 3.13

# Create .venv and install all dependencies
uv sync
```

## Dataset

The dataset is **not included in this repository** for security reasons, so you need to add it yourself.

1. Obtain `Dataset_Brief_2.csv` from the course materials.
2. Place it in the **root of the project directory**, next to this README:

```
Argus/
├── Argus.ipynb
├── Dataset_Brief_2.csv    <- put it here
├── README.md
└── pyproject.toml
```

The notebook reads it with a relative path, so the file name and location need to match exactly. If you run the notebook on Google Colab instead, upload the file to the session storage first.

## Running the notebook

1. Open `Argus.ipynb` in VS Code or Jupyter.
2. **Select the `argus` kernel** (the project's `.venv`) before running anything.
   - VS Code: click *Select Kernel* (top right) > *Python Environments* > `argus`.
   - Jupyter: choose `argus` from the *Kernel* > *Change Kernel* menu.
3. Run the cells from top to bottom. Later cells depend on earlier ones, so the order matters.


## Generated files

Running the notebook creates:

- `figures/` with the plots used in the analysis and report
- `cleaned_train.csv`, `cleaned_val.csv` and `cleaned_test.csv` with the cleaned splits (set `EXPORT = False` in the last Phase 1 cell to skip this)

These are derived from the dataset, so keep them out of version control.