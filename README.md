# IPA Research and Data Science Training

A comprehensive collection of tutorials and technical references for research and data staff at Innovations for Poverty Action (IPA). This repository focuses on practical aspects of research design, data collection, data quality, data analysis, data science, ethics/IRB processes, and software tools.

## Development set up

Development relies on the following software

- `winget` (Windows) or `homebrew` (MacOS/Linux) or `snap` (Linux) for package management and installation
- `git` for source control management
- `just` for running common command line patterns
- `uv` for installing Python and managing virtual environments

This repository uses a `Justfile` for collecting common command line actions that we run
to set up the computing environment and build the assets of the handbook. Note that you
should also have Git installed

To get started, make sure you have `Just` installed on your computer by running the
following from the command line:

| Platform  | Commands                                                            |
| --------- | ------------------------------------------------------------------- |
| Windows   | `winget install Git.Git Casey.Just astral-sh.uv GitHub.cli Posit.Quarto` |
| Mac/Linux | `brew install just uv gh`                                          |

This will make sure that you have the latest version of `Just`, as well as
[uv](https://docs.astral.sh/uv/) (installer for Python) and
[Quarto](https://quarto.org/docs/guide/) (for writing and compiling scientific and
technical documents).

- We use `Just` in order to make it easier for all IPA users to be productive with data
  and technology systems. The goal of using a `Justfile` is to help make the end goal of
  the user easier to achieve without needing to know or remember all of the technical
  details of how we get to that goal.
- We use `uv` to help ease use of Python. `uv` provides a global system for creating and
  building computing environments for Python.
- We use Quarto to allow users to focus on writing and data analytics. Writing in
  markdown, jupyter notebooks, python scripts, R scripts, etc. makes it easier to
  review, update, and deploy technical documentation.
- We also recommend using in Integrated Development Environment (IDE).
  Preferred options are `VS Code` or `Positron`.

| Platform  | Commands                                                            |
| --------- | ------------------------------------------------------------------- |
| Windows   | `winget install Microsoft.VisualStudioCode`                         |
| Mac       | `brew install --cask visual-studio-code`                            |
| Linux     | `sudo snap install code --classic`                                  |

| Platform  | Commands                                                            |
| --------- | ------------------------------------------------------------------- |
| Windows   | `winget install Posit.Positron`                                     |
| Mac       | `brew install --cask positron`                                      |

As a shortcut, if you already have `Just` installed, you can run the following to
install required software and build a python virtual environment that is used to build
the handbook pages:

```bash
just get-started
```

Note: you may need to restart your terminal after running the command above to activate
the installed software.

After the required software is installed, you can activate the Python virtual
environment:

| Shell      | Commands                                |
| ---------- | --------------------------------------- |
| Bash       | `.venv/Scripts/activate`                |
| Powershell | `.venv/Scripts/activate.ps1`            |
| Nushell    | `overlay use .venv/Scripts/activate.nu` |

## Workshop Table of Contents

This repository contains comprehensive workshops organized to take you from complete beginner to proficient data scientist. The workshops are designed with a logical learning progression to build foundational skills before advancing to specialized topics.

### Recommended Learning Path

For new users unfamiliar with VS Code/Positron, command line, and programming, we recommend following this order:

#### Phase 1: Foundation Setup (Choose Your IDE)

Start with **one** of these IDE workshops based on your preference:

| Workshop | Duration | Description | Prerequisites |
|----------|----------|-------------|---------------|
| **[VS Code Introduction](ide-workshops/vscode-introduction/)** | 2-3 hours | Learn the most popular code editor | None |
| **[Positron Introduction](ide-workshops/positron-introduction/)** | 6-8 hours | Learn the next-generation data science IDE | None |

**Recommendation**: Choose VS Code for general programming or Positron for data science focus.

#### Phase 2: Essential Skills

Complete these workshops in order to build core technical skills:

| Order | Workshop | Duration | Description | Prerequisites |
|-------|----------|----------|-------------|---------------|
| 1 | **[Markdown Introduction](ide-workshops/markdown-introduction/)** | 1-2 hours | Learn to write formatted documentation | IDE setup |
| 2 | **[Shell/Command Line Introduction](commandline-workshops/shell-introduction/)** | 3-4 hours | Master the command line interface | IDE setup |
| 3 | **[Git Introduction](git-workshops/git-introduction/)** | 1.5 hours | Version control and collaboration | Command line basics |

#### Phase 3: Python Programming

Build your Python skills with these workshops:

| Order | Workshop | Duration | Description | Prerequisites |
|-------|----------|----------|-------------|---------------|
| 1 | **[Python Data Analysis](python-workshops/python-data-analysis/)** | 6-8 hours | Learn Python basics with real data | Foundation skills |
| 2 | **[Python Programming Foundations](python-workshops/python-programming-foundations/)** | 4-6 hours | Advanced Python programming concepts | Python basics |

#### Phase 4: Specialized Python Applications

Choose workshops based on your interests and needs:

| Workshop | Duration | Description | Prerequisites |
|----------|----------|-------------|---------------|
| **[Web Scraping Introduction](python-workshops/webscraping-introduction/)** | 3-4 hours | Extract data from websites | Python fundamentals |
| **[LLM Introduction](python-workshops/llm-introduction/)** | 6-8 hours | Build AI applications with Large Language Models | Python fundamentals |

#### Phase 5: Additional Data Tools

Expand your toolkit with these specialized workshops:

| Workshop | Duration | Description | Prerequisites |
|----------|----------|-------------|---------------|
| **[SQL Introduction](sql-workshops/sql-introduction/)** | 4-6 hours | Database querying for social scientists | None (independent) |
| **[Stata Training](stata-workshops/IPA-Stata-Trainings/)** | Variable | Statistical software for economists | None (independent) |

### Quick Reference by Skill Level

#### Complete Beginner (Never programmed before)

1. Choose IDE: VS Code OR Positron Introduction
2. Markdown Introduction
3. Shell Introduction
4. Git Introduction
5. Python Data Analysis
6. Python Programming Foundations

#### Some Programming Experience

1. VS Code Introduction (if needed)
2. Git Introduction (if needed)
3. Python Data Analysis
4. Python Programming Foundations
5. Choose specialization: Web Scraping or LLM Introduction

#### Python Programmer Looking to Specialize

1. Web Scraping Introduction
2. LLM Introduction
3. SQL Introduction (for database work)

### Workshop Details

#### IDE Workshops

##### VS Code Introduction

- **Path**: `ide-workshops/vscode-introduction/`
- **Tutorials**: 7 comprehensive lessons
- **Topics**: Installation, interface navigation, code editing, customization, extensions, debugging, version control
- **Best for**: General programming and development work

##### Positron Introduction

- **Path**: `ide-workshops/positron-introduction/`
- **Tutorials**: 6 progressive lessons
- **Topics**: Installation, interface, interpreter setup, data exploration, Python workflow, R workflow
- **Best for**: Data science and statistical analysis work

##### Markdown Introduction

- **Path**: `ide-workshops/markdown-introduction/`
- **Tutorials**: 3 focused lessons
- **Topics**: Basic syntax, GitHub Flavored Markdown, Quarto integration
- **Best for**: Creating documentation and reports

#### Foundation Skills Workshops

##### Shell/Command Line Introduction

- **Path**: `commandline-workshops/shell-introduction/`
- **Tutorials**: 7 essential lessons
- **Topics**: Navigation, file operations, pipes and filters, loops, scripts, finding files
- **Best for**: Essential system interaction skills

##### Git Introduction

- **Path**: `git-workshops/git-introduction/`
- **Tutorials**: 10 practical lessons
- **Topics**: Repository creation, version control, collaboration, branches, pull requests, conflict resolution
- **Best for**: Code management and collaboration

#### Python Programming Workshops

##### Python Data Analysis

- **Path**: `python-workshops/python-data-analysis/`
- **Tutorials**: 20 comprehensive lessons
- **Topics**: Variables, data types, libraries, data frames, visualization, loops, conditionals, functions
- **Best for**: Learning Python with real-world data analysis

##### Python Programming Foundations

- **Path**: `python-workshops/python-programming-foundations/`
- **Tutorials**: 12 advanced lessons
- **Topics**: NumPy arrays, matplotlib visualization, file processing, error handling, debugging, command-line programs
- **Best for**: Scientific computing and data analysis

##### Web Scraping Introduction

- **Path**: `python-workshops/webscraping-introduction/`
- **Tutorials**: 5 focused lessons
- **Topics**: Gazpacho library, HTML parsing, data extraction, pandas integration, ethical scraping
- **Best for**: Automated data collection from websites

##### LLM Introduction

- **Path**: `python-workshops/llm-introduction/`
- **Tutorials**: 4 comprehensive lessons
- **Topics**: API setup, conversation management, function calling, multimodal content, real-world applications
- **Best for**: Building AI-powered applications

#### Additional Data Tools

##### SQL Introduction

- **Path**: `sql-workshops/sql-introduction/`
- **Tutorials**: 10 database lessons
- **Topics**: Relational databases, querying, joins, aggregation, data management
- **Best for**: Working with structured data and databases

##### Stata Training

- **Path**: `stata-workshops/IPA-Stata-Trainings/`
- **Courses**: 5 progressive courses (101, 102, 103, 104, 201)
- **Topics**: Statistical analysis, data management, econometrics
- **Best for**: Economic research and statistical analysis

### Learning Tips

1. **Start with the basics**: Don't skip the foundation workshops even if they seem simple
2. **Practice regularly**: Work through exercises and try variations on your own
3. **Use real data**: Apply concepts to your own research questions when possible
4. **Join the community**: Connect with other learners and get help when needed
5. **Build projects**: Create your own projects to reinforce learning

### Getting Started

1. **Install required software** using the commands above
2. **Choose your learning path** based on your current skill level
3. **Start with Phase 1** and work through systematically
4. **Practice with real data** whenever possible
5. **Ask for help** when you get stuck
