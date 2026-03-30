# MAE223 — Week 1: Time Series Analysis

Starter repository for the Week 1 Time Series Analysis lab.

## Files

| File | Description |
|------|-------------|
| `Tidal Analysis_Python.ipynb` | Lab notebook — work here |
| `sample_data.json` | Velocity time series (CLASS10 mooring, 30-min sampling, 16,000 samples) |
| `la_jolla_tide.json` | NOAA La Jolla tide gauge sea level — full ~100-year record, hourly, in mm |
| `environment.yml` | Conda environment specification |

---

## Setup (do this once)

### What is a Jupyter Notebook?

A Jupyter Notebook is an interactive document that combines code, text, and figures in a single file (`.ipynb`). It is organized into **cells** — each cell contains either code or explanatory text, and you can run cells individually or all at once. When you run a code cell, the output (numbers, plots, etc.) appears directly below it. Notebooks are widely used in science and data analysis because they make it easy to write, run, and inspect code in small chunks.

### What is VS Code?

VS Code (Visual Studio Code) is a free code editor made by Microsoft. It can open and run Jupyter Notebooks directly. It is a popular alternative to running notebooks in a web browser (the classic JupyterLab interface). Both work with the same `.ipynb` files — the choice is just a matter of preference. For this course we use VS Code.

### What is a kernel?

A kernel is the Python engine that actually runs the code in your notebook. When you open a notebook you need to tell it which Python environment to use — in our case that is the `mae223` environment you will create below. Think of the kernel as the engine and the notebook as the dashboard.

---

### Step 1 — Install Miniconda

Miniconda is a lightweight Python package manager. It lets you create isolated Python environments so that different projects do not interfere with each other. **Skip this step if you already have Anaconda or Miniconda installed.**

**Mac:**
1. Go to https://docs.conda.io/en/latest/miniconda.html
2. Download the **macOS** installer — choose **Apple Silicon** if you have an M1/M2/M3/M4 Mac, otherwise choose **Intel**
3. Open the downloaded `.pkg` file and follow the prompts
4. Open a **Terminal** window: press `Cmd+Space`, type `Terminal`, and hit Enter
5. Type `conda --version` and press Enter — you should see something like `conda 24.x.x`

**Windows:**
1. Go to https://docs.conda.io/en/latest/miniconda.html
2. Download the **Windows 64-bit** installer (`.exe`)
3. Run the installer. When you reach the **Advanced Options** screen, check **"Add Miniconda3 to my PATH environment variable"**
4. Click through the remaining prompts and finish the installation
5. Open **Anaconda Prompt**: click the Windows Start menu, type `Anaconda Prompt`, and open it. A black window will appear — this is your command line and is what you will use for all terminal commands below
6. Type `conda --version` and press Enter — you should see something like `conda 24.x.x`

---

### Step 2 — Clone this repository

If you are viewing this on GitHub Classroom, click the green **Code** button and copy the repository URL. Then in Terminal (Mac) or Anaconda Prompt (Windows) run:

```bash
git clone <your-repo-url>
```

This will download all the files into a folder on your computer. Navigate into it:

```bash
cd time-series-analysis
```

---

### Step 3 — Create the course environment

This installs all the Python packages needed for the lab into an isolated environment called `mae223`.

```bash
conda env create -f environment.yml
```

This may take a few minutes. When it finishes, run:

```bash
conda activate mae223
python -m ipykernel install --user --name mae223 --display-name "mae223"
```

The first command activates the environment. The second registers it as a kernel so VS Code can find it.

---

### Step 4 — Install VS Code

1. Download and install VS Code from https://code.visualstudio.com
2. Open VS Code and go to the **Extensions** panel — click the square icon on the left sidebar or press `Cmd+Shift+X` (Mac) / `Ctrl+Shift+X` (Windows)
3. Search for **Python** and click Install
4. Search for **Jupyter** and click Install
5. Restart VS Code after both extensions finish installing

---

### Step 5 — Open the notebook

1. In VS Code, open the repo folder: **File → Open Folder**, navigate to the `time-series-analysis` folder, and click Open
2. Click `Tidal Analysis_Python.ipynb` in the left file panel to open the notebook
3. In the top-right corner click **Select Kernel → Select Another Kernel... → Jupyter Kernel... → mae223**
4. Click **Run All** in the toolbar to execute all cells — plots and output will appear below each cell

> **Note:** Always run cells from top to bottom. If you see a `NameError`, it usually means an earlier cell has not been run yet. Use **Run All** to avoid this.
