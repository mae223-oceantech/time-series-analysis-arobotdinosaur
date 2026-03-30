# MAE223 — Week 1: Time Series Analysis

Starter repository for the Week 1 Time Series Analysis lab.

## Files

| File | Description |
|------|-------------|
| `Tidal Analysis_Python.ipynb` | Lab notebook — work here |
| `sample_data.json` | Velocity time series (CLASS10 mooring, 30-min sampling) |
| `la_jolla_tide.json` | NOAA La Jolla tide gauge sea level — longest contiguous segment (~18.9 years, hourly) |
| `environment.yml` | Conda environment specification |

## Setup

**Step 1 — Install Miniconda** (skip if already installed)

- Download from https://docs.conda.io/en/latest/miniconda.html
- Mac: run the `.pkg` installer, then open Terminal (`Cmd+Space` → "Terminal")
- Windows: run the `.exe` installer, check **"Add Miniconda3 to my PATH"**, then open **Anaconda Prompt** from the Start menu

**Step 2 — Create the course environment**

In Terminal (Mac) or Anaconda Prompt (Windows), navigate to the folder where you cloned this repo, then run:

```bash
conda env create -f environment.yml
conda activate mae223
python -m ipykernel install --user --name mae223 --display-name "mae223"
```

**Step 3 — Open the notebook in VS Code**

1. Install VS Code from https://code.visualstudio.com
2. Install the **Python** and **Jupyter** extensions (`Ctrl/Cmd+Shift+X`)
3. Open this folder in VS Code: **File → Open Folder**
4. Open `Tidal Analysis_Python.ipynb`
5. Click **Select Kernel** (top right) → **Select Another Kernel... → Jupyter Kernel... → mae223**
6. Click **Run All**
