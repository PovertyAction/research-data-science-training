# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the IPA Research and Data Science Training repository - a collection of tutorials and technical references for research and data staff at Innovations for Poverty Action (IPA). The content focuses on practical aspects of research design, data collection, data quality, data analysis, data science, ethics/IRB processes, and software tools.

The repository is built with Quarto and follows the Diátaxis framework, organizing documentation into tutorials and how-to guides. Content is written in `.qmd`, `.md`, `.ipynb` or `.py` format.

## Essential Commands

All project commands are managed through a `Justfile`. Key commands:

### Development Setup

```bash
just get-started          # Install dependencies and set up environment
just venv                  # Create Python virtual environment with uv
just activate-venv         # Activate the virtual environment
```

### Site Development

```bash
just lab                   # Launch Jupyter Lab
just preview-docs          # Preview site locally (quarto preview)
just build-docs            # Build site (quarto render)
```

### Code Quality and Formatting

```bash
just fmt-all              # Format all code and content (run before commits)
just fmt-markdown         # Fix markdown formatting issues
just fmt-md <file>         # Format a single markdown file
just lint-py              # Lint Python code with ruff
just fmt-python           # Format Python code with ruff
just pre-commit-run       # Run all pre-commit hooks
```

## Architecture and Structure

### Content Organization

- **Workshop-based structure**: `python-workshops/`, `commandline-workshops/`, `git-workshops/`, `stata-workshops/`, `ide-workshops/`
- **Quarto-based**: Uses `.qmd` files for content with YAML frontmatter
- **Template system**: `page-template.qmd` and `page-template.py` provide structure for new pages

### Key Files

- `Justfile`: Command automation and development workflow
- `pyproject.toml`: Python dependencies (altair, causaldata, duckdb, great-tables, jupyterlab, pandas, polars, etc.) and tool configuration
- `.pre-commit-config.yaml`: Pre-commit hooks for code quality (ruff, codespell, markdownlint)
- `.markdownlint.yaml`: Markdown linting rules
- `convert_md_to_qmd.py`: Script for converting markdown files to Quarto format
- `fix_converted_files.py`: Script for fixing converted files

### Python Environment

- Uses `uv` for Python environment management
- Python 3.12+ required
- Virtual environment created in `.venv/`
- Dependencies include data science libraries: pandas, polars, altair, seaborn, jupyterlab

## Content Guidelines

### File Naming

- Use lowercase, hyphenated names (e.g., `data-collection.qmd`, `python-basics.py`)
- Each directory should have an `index.qmd` file

### Required YAML Frontmatter for .qmd files

- `title`: Page title
- `abstract`: Page description
- `date: last-modified`: Auto-update modification date
- `authors-ipa`: List of main content creators
- `contributors`: List of supporting contributors
- `keywords`: List of research and data science keywords
- `license`: "CC BY" unless otherwise specified

### Documentation Philosophy

Follows the Diátaxis framework:

- **Tutorials**: Learning-oriented lessons that take users step-by-step
- **How-to guides**: Problem-oriented practical directions for competent users

## Development Workflow

1. Set up environment: `just get-started`
2. Activate virtual environment: `just activate-venv`
3. Make changes to content
4. Format and lint: `just fmt-all`
5. Preview changes: `just preview-docs`
6. Run pre-commit hooks: `just pre-commit-run`

## Platform Support

The project supports Windows, macOS, and Linux with platform-specific installation commands in the Justfile for required tools like `just`, `uv`, `gh`, `quarto`, and `markdownlint-cli`.
