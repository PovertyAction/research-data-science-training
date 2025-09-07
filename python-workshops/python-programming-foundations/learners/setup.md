---
title: Setup
---

## Overview

This lesson is designed to be run on a personal computer.
All of the software and data used in this lesson are freely available online,
and instructions on how to obtain them are provided below.

## Install Python

In this lesson, we will be using Python 3 with some of its most popular scientific libraries. We'll use **uv**, a modern Python package manager that makes installation simple and reliable.

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

### Step 2: Install Python

uv makes Python installation simple - it will automatically install Python when needed:

```bash
uv python install
```

This installs the latest stable Python version. You can also specify a version:

```bash
uv python install 3.12
```

### Step 3: Install Required Libraries

Create a new project for this workshop:

```bash
uv init swc-python
cd swc-python
```

Add the scientific libraries we'll need:

```bash
uv add numpy matplotlib
```

This automatically creates a virtual environment and installs the packages.

## Obtain lesson materials

1. Download [python-programming-foundations-data.zip][zipfile1]
  and [python-programming-foundations-code.zip][zipfile2].
2. Move downloaded files to your `swc-python` project directory.
3. Unzip the files.

You should see two folders called `data` and `code` in the `swc-python` directory.

## Launch Python interface

To start working with Python, we'll use uv to run Python in your project environment. This ensures you have access to all the libraries we installed. Below are several options for working with Python:

### Recommended: Using uv run

The simplest approach is to use `uv run` with your preferred Python interface. This automatically uses your project's virtual environment.

## Option A: Jupyter Notebook

A Jupyter Notebook provides a browser-based interface for working with Python.

First, add Jupyter to your project:

```bash
uv add jupyter
```

Then launch a notebook using uv:

1. Navigate to your project directory:

```bash
cd swc-python
```

2. Navigate to the `data` directory:

```bash
cd data
```

3. Start Jupyter using uv:

```bash
uv run jupyter notebook
```

4. In the browser window that opens, click "New" and select "Python 3" to create a new notebook.

## Option B: IPython interpreter

IPython is an alternative solution situated somewhere in between the plain-vanilla Python
interpreter and Jupyter Notebook. First add IPython to your project:

```bash
uv add ipython
```

To start using IPython with uv:

```bash
uv run ipython
```

## Option C: Plain Python interpreter

To launch a plain Python interpreter using uv:

```bash
uv run python
```

This ensures you're using the Python version and packages from your project environment.

## Why use uv?

uv is a modern Python package manager that provides several benefits for beginners:

- **Automatic environment management**: Creates isolated environments for each project
- **Fast and reliable**: Downloads and installs packages quickly
- **Simple commands**: `uv add package_name` instead of complex pip commands
- **No conflicts**: Each project has its own dependencies
- **Automatic Python installation**: No need to manually install Python first

[zipfile1]: data/python-programming-foundations-data.zip
[zipfile2]: ../episodes/files/code/python-programming-foundations-code.zip
