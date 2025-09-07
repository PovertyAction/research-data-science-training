# Positron Introduction Workshop

This tutorial series provides a comprehensive introduction to Positron, a next-generation data science IDE built by Posit PBC. These hands-on tutorials are designed following the Diátaxis framework to provide practical, learner-focused instruction.

> [!NOTE]
> This content is adapted from the [Positron Documentation](https://positron.posit.co/) and is made available under the Creative Commons Attribution-ShareAlike 4.0 license. See [LICENSE.md](./LICENSE.md) for details.

## What is Positron?

Positron is a free, next-generation data science IDE built on the foundation of Visual Studio Code (Code OSS). It provides:

- **Polyglot Support**: Native support for Python and R
- **Interactive Computing**: Built-in console, data viewer, and plots panel
- **Enhanced Data Science Tools**: Variables panel, data explorer, and integrated help
- **Familiar Interface**: VS Code-based interface with data science enhancements
- **Extensible Platform**: Support for extensions and customization

## Workshop Overview

This workshop is designed to take you from installation to productive data science work in Positron. The tutorials are structured as hands-on lessons that you complete step-by-step.

### Target Audience

- Data scientists and analysts who want to learn Positron
- Python and R users looking for an enhanced IDE experience
- VS Code users interested in data science-specific features
- Researchers and analysts seeking an integrated data science environment

### Prerequisites

- Basic familiarity with Python or R
- Understanding of fundamental data science concepts
- Access to a computer where you can install software

## Tutorial Structure

The workshop consists of five progressive tutorials:

### [0. Setting Up Positron](0_setup.qmd)

**Type**: Tutorial | **Duration**: 20-30 minutes

Learn to download, install, and verify your Positron installation. Covers system requirements, installation steps for different operating systems, and initial setup verification.

**You will learn to**:

- Download Positron for your operating system
- Install and launch Positron successfully
- Verify that your installation is working correctly
- Troubleshoot common installation issues

### [1. Exploring the Positron Interface](1_interface-overview.qmd)

**Type**: Tutorial | **Duration**: 30-45 minutes

Navigate the Positron interface and understand its key components. Discover data science-specific panels and learn to customize your workspace.

**You will learn to**:

- Navigate the main areas of the Positron interface
- Use data science panels (Console, Variables, Plots)
- Customize your workspace and layouts
- Use essential keyboard shortcuts
- Understand how Positron differs from VS Code

### [2. Setting Up Python and R Interpreters](2_interpreter-setup.qmd)

**Type**: Tutorial | **Duration**: 45-60 minutes

Configure Python and R interpreters, manage virtual environments, and install essential data science packages.

**You will learn to**:

- Install and configure Python and R interpreters
- Create and manage Python virtual environments
- Switch between different interpreters
- Install essential data science packages
- Verify your setup with test code

### [3. Data Exploration with Positron's Tools](3_data-exploration.qmd)

**Type**: Tutorial | **Duration**: 60-75 minutes

Use Positron's built-in data exploration tools including the Data Viewer, Variables panel, and Plots panel for interactive data analysis.

**You will learn to**:

- Import datasets using Python and R
- Navigate the Data Viewer for interactive data exploration
- Use the Variables panel to track and inspect objects
- Create visualizations in the Plots panel
- Filter and examine data interactively

### [4. Complete Python Data Science Workflow](4_python-workflow.qmd)

**Type**: Tutorial | **Duration**: 90-120 minutes

Work through a complete Python data science project from setup to documentation, using real-world housing price data.

**You will learn to**:

- Set up a professional Python data science project
- Perform data cleaning and exploratory analysis
- Create publication-quality visualizations
- Build and evaluate predictive models
- Use Jupyter notebooks within Positron
- Document and save your analysis

### [5. Complete R Data Science Workflow](5_r-workflow.qmd)

**Type**: Tutorial | **Duration**: 90-120 minutes

Complete an end-to-end R analysis project using the tidyverse ecosystem and Titanic passenger data.

**You will learn to**:

- Set up a professional R data science project
- Use tidyverse for data manipulation and visualization
- Perform statistical analysis and hypothesis testing
- Create interactive visualizations with plotly
- Generate reproducible reports with Quarto
- Follow R best practices in Positron

## Getting Started

### Quick Start

1. **Complete the Setup**: Start with [0_setup.qmd](0_setup.qmd) to install Positron
2. **Learn the Interface**: Work through [1_interface-overview.qmd](1_interface-overview.qmd)
3. **Configure Interpreters**: Follow [2_interpreter-setup.qmd](2_interpreter-setup.qmd)
4. **Choose Your Path**:
   - For Python focus: Complete tutorials 3 → 4
   - For R focus: Complete tutorials 3 → 5
   - For both languages: Complete all tutorials

### Time Commitment

- **Minimum Path** (Python or R): 4-5 hours
- **Complete Workshop**: 6-8 hours
- **Self-paced**: Can be completed over multiple sessions

## System Requirements

- **Operating System**: Windows 10/11, macOS 10.15+, or Linux (Ubuntu 18.04+)
- **RAM**: 4GB minimum, 8GB recommended
- **Disk Space**: 2GB for Positron and all dependencies
- **Internet Connection**: Required for package installation and some data sources

## Additional Resources

### Official Documentation

- [Positron Official Website](https://positron.posit.co/)
- [Positron GitHub Repository](https://github.com/posit-dev/positron)
- [Positron Documentation](https://positron.posit.co/welcome)

### Community and Support

- [Positron GitHub Discussions](https://github.com/posit-dev/positron/discussions)
- [Community Forum](https://forum.posit.co/)

### Related Learning Resources

- [Python for Data Analysis](https://wesmckinney.com/book/)
- [R for Data Science](https://r4ds.had.co.nz/)
- [Quarto Documentation](https://quarto.org/)

## Workshop Structure and Philosophy

This workshop follows the **Diátaxis framework** for technical documentation:

- **Tutorials** (like these): Learning-oriented, hands-on lessons that take you through practical exercises
- **How-to guides**: Problem-oriented instructions for specific tasks
- **Reference material**: Information-oriented technical descriptions
- **Explanation**: Understanding-oriented discussions of concepts

All tutorials in this workshop are designed as **tutorials** in the Diátaxis sense - they are hands-on, practical lessons that guide you through learning by doing.

## Contributing and Feedback

This workshop is part of the IPA Research and Data Science Training. If you find issues or have suggestions:

1. Check the [GitHub Issues](https://github.com/your-repo/issues) for existing reports
2. Submit new issues or suggestions
3. Contribute improvements via pull requests

## License and Attribution

This workshop content is licensed under [CC BY-SA 4.0](./LICENSE.md).

**Original Content**: Adapted from [Positron Documentation](https://positron.posit.co/) (CC BY-SA 4.0)
**Modifications**: Restructured as hands-on tutorials following the Diátaxis framework
**Created for**: IPA Research and Data Science Training

## Troubleshooting

### Common Issues

**Positron won't start**:

- Check system requirements
- Verify installation completed successfully
- Try running as administrator (Windows) or with sudo (Linux)

**Python/R interpreter not found**:

- Ensure Python/R is installed and in system PATH
- Use Command Palette to manually select interpreter
- Check virtual environment activation

**Packages won't install**:

- Verify internet connection
- Check for permission issues
- Try installing one package at a time
- Use virtual environments to avoid conflicts

**Data Viewer won't open**:

- Ensure data is in DataFrame/data.frame format
- Try viewing a subset for large datasets
- Check that Variables panel shows the object

### Getting Help

1. **Check tutorial troubleshooting sections**: Each tutorial includes specific troubleshooting guidance
2. **Consult Positron documentation**: [https://positron.posit.co/](https://positron.posit.co/)
3. **Search GitHub discussions**: Often questions have been asked before
4. **Ask for help**: Use the community forums or GitHub discussions

---

**Workshop Duration**: 6-8 hours total | **Skill Level**: Beginner to Intermediate | **Last Updated**: 2024

Get started with [Tutorial 0: Setting Up Positron](0_setup.qmd)!
