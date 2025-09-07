---
title: Setup
---

## Getting the Data

The data we will be using is taken from the [gapminder] dataset.
To obtain it:

1. Download and unzip [python-data-analysis-data.zip](files/python-data-analysis-data.zip)
2. Move the unzipped data files to your `python-data-analysis` project directory

You should see the data files in the same directory as your project.

## Installing Python Using uv

We use **uv**, a modern Python package manager that makes installation simple and reliable.

### Step 1: Install uv

First, install uv using one of these methods:

**Windows (PowerShell):**

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

or

```powershell
winget install -e --id astral-sh.uv
```

**macOS/Linux:**

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

or

```bash
brew install uv
```

### Step 2: Create Project and Install Dependencies

Create a new project for this data analysis workshop:

```bash
uv init python-data-analysis
cd python-data-analysis
```

Add the required libraries:

```bash
uv add pandas matplotlib jupyter
```

This automatically installs Python (if needed), creates a virtual environment, and installs the data science packages.

### Step 3: Launch JupyterLab

To start working with the notebooks:

```bash
uv run jupyter lab
```

This will open JupyterLab in your browser with access to all the installed packages.

[gapminder]: https://en.wikipedia.org/wiki/Gapminder_Foundation
