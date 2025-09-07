# Programming with Python

An introduction to Python for non-programmers using inflammation data.

## About the Lesson

This lesson teaches novice programmers to write modular code to perform data analysis
using Python. The emphasis, however, is on teaching language-agnostic principles of
programming such as automation with loops and encapsulation with functions,
see [Best Practices for Scientific Computing][best-practices] and
[Good enough practices in scientific computing][good-practices] to learn more.

The example used in this lesson analyses a set of 12 files with simulated inflammation
data collected from a trial for a new treatment for arthritis. Learners are shown
how it is better to automate analysis using functions instead of repeating analysis
steps manually.

The rendered version of the lesson is available at:
[https://swcarpentry.github.io/python-novice-inflammation/](https://swcarpentry.github.io/python-novice-inflammation/).

This lesson is also available in [R] and [MATLAB].

## Episodes

| \#   | Episode | Time | Question(s)                                                                  |
| --: | :------ | :--: | :--------------------------------------------------------------------------- |
| 1   | [Python Fundamentals][episode01]        | 30   | What basic data types can I work with in Python?<br>How can I create a new variable in Python?<br>Can I change the value associated with a variable after I create it?                             |
| 2   | [Analyzing Patient Data][episode02]        | 60   | How can I process tabular data files in Python?                              |
| 3   | [Visualizing Tabular Data][episode03]        | 50   | How can I visualize tabular data in Python?<br>How can I group several plots together?                                  |
| 4   | [Storing Multiple Values in Lists][episode04]        | 30   | How can I store many values together?                                        |
| 5   | [Repeating Actions with Loops][episode05]        | 30   | How can I do the same operations on many different values?                   |
| 6   | [Analyzing Data from Multiple Files][episode06]        | 20   | How can I do the same operations on many different files?                    |
| 7   | [Making Choices][episode07]        | 30   | How can my programs do different things based on data values?                |
| 8   | [Creating Functions][episode08]        | 30   | How can I define new functions?<br>What's the difference between defining and calling a function?<br>What happens when I call a function?                                              |
| 9   | [Errors and Exceptions][episode09]        | 30   | How does Python report errors?<br>How can I handle errors in Python programs?                                               |
| 10  | [Defensive Programming][episode10]        | 30   | How can I make my programs more reliable?                                    |
| 11  | [Debugging][episode11]        | 30   | How can I debug my program?                                                  |
| 12  | [Command-Line Programs][episode12]        | 30   | How can I write Python programs that will work like Unix command-line tools? |

The best way to learn how to program is to do something useful,
so this introduction to Python is built around a common scientific task:
**data analysis**.

### Scenario: A Miracle Arthritis Inflammation Cure

Our imaginary colleague "Dr. Maverick" has invented a new miracle drug that promises to
cure arthritis inflammation flare-ups after only 3 weeks since initially taking the
medication! Naturally, we wish to see the clinical trial data, and after months of asking
for the data they have finally provided us with a CSV spreadsheet containing the clinical
trial data.

The CSV file contains the number of inflammation flare-ups per day for the 60 patients
in the initial clinical trial, with the trial lasting 40 days. Each row corresponds to a
patient, and each column corresponds to a day in the trial. Once a patient has their first
inflammation flare-up they take the medication and wait a few weeks for it to take effect
and reduce flare-ups.

To see how effective the treatment is we would like to:

1. Calculate the average inflammation per day across all patients.
2. Plot the result to discuss and share with colleagues.

![](episodes/figures/lesson-overview.svg "Lesson Overview"){alt='3-step flowchart shows inflammation data records for patients moving to the Analysis stepwhere a heat map of provided data is generated moving to the Conclusion step that asks thequestion, How does the medication affect patients?'}

### Data Format

The data sets are stored in
[comma-separated values](learners/reference.md#comma-separated-values) (CSV) format:

- each row holds information for a single patient,
- columns represent successive days.

The first three rows of our first file look like this:

```source
0,0,1,3,1,2,4,7,8,3,3,3,10,5,7,4,7,7,12,18,6,13,11,11,7,7,4,6,8,8,4,4,5,7,3,4,2,3,0,0
0,1,2,1,2,1,3,2,2,6,10,11,5,9,4,4,7,16,8,6,18,4,12,5,12,7,11,5,11,3,3,5,4,4,5,5,1,1,0,1
0,1,1,3,3,2,6,2,5,9,5,7,4,5,4,15,5,11,9,10,19,14,12,17,7,12,11,7,4,2,10,5,4,2,2,3,2,2,1,1
```

Each number represents the number of inflammation bouts that a particular patient experienced on a
given day.

For example, value "6" at row 3 column 7 of the data set above means that the third
patient was experiencing inflammation six times on the seventh day of the clinical study.

In order to analyze this data and report to our colleagues, we'll have to learn a little bit
about programming.

::::::::::::::::::::::::::::::::::::::::::  prereq

## Prerequisites

You need to understand the concepts of **files** and **directories** and how to start a Python
interpreter before tackling this lesson. This lesson sometimes references Jupyter
Notebook although you can use any Python interpreter mentioned in the [Setup](learners/setup.md).

The commands in this lesson pertain to any [officially supported Python version](https://devguide.python.org/versions/#supported-versions).
Newer versions usually have better error printouts, so using newer Python versions is
recommend if possible.

### Getting Started

To get started, follow the directions on the [Setup](learners/setup.md) page to download data
and install a Python interpreter.

## License

Instructional material from this lesson is made available under the
[Creative Commons Attribution][cc-by-human] ([CC BY 4.0][cc-by-legal]) license. Except where
otherwise noted, example programs and software included as part of this lesson are made available
under the [MIT license][mit-license]. For more information, see [LICENSE.md](LICENSE.md).

## Citation

Please cite as:

Azalee Bostroem, Trevor Bekolay, and Valentina Staneva (eds):
"Software Carpentry: Programming with Python."  Version 2016.06, June
2016, <https://github.com/swcarpentry/python-novice-inflammation>,
10.5281/zenodo.57492.

## About Software Carpentry

Software Carpentry is a volunteer project that teaches basic computing skills to researchers since
1998\. More information about Software Carpentry can be found [here][swc-about].

## About The Carpentries

The Carpentries is a registered 501(c)3 non-profit organisation based in Delaware, USA. We are a global community
teaching foundational computational and data science skills to researchers in academia,
industry and government. More information can be found [here][cp-about].

[best-practices]: https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.1001745
[good-practices]: https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005510
[R]: https://github.com/swcarpentry/r-novice-inflammation
[MATLAB]: https://github.com/swcarpentry/matlab-novice-inflammation
[episode01]: https://swcarpentry.github.io/python-novice-inflammation/01-intro.html
[episode02]: https://swcarpentry.github.io/python-novice-inflammation/02-numpy.html
[episode03]: https://swcarpentry.github.io/python-novice-inflammation/03-matplotlib.html
[episode04]: https://swcarpentry.github.io/python-novice-inflammation/04-lists.html
[episode05]: https://swcarpentry.github.io/python-novice-inflammation/05-loop.html
[episode06]: https://swcarpentry.github.io/python-novice-inflammation/06-files.html
[episode07]: https://swcarpentry.github.io/python-novice-inflammation/07-cond.html
[episode08]: https://swcarpentry.github.io/python-novice-inflammation/08-func.html
[episode09]: https://swcarpentry.github.io/python-novice-inflammation/09-errors.html
[episode10]: https://swcarpentry.github.io/python-novice-inflammation/10-defensive.html
[episode11]: https://swcarpentry.github.io/python-novice-inflammation/11-debugging.html
[episode12]: https://swcarpentry.github.io/python-novice-inflammation/12-cmdline.html
[cc-by-human]: https://creativecommons.org/licenses/by/4.0/
[cc-by-legal]: https://creativecommons.org/licenses/by/4.0/legalcode
[mit-license]: https://opensource.org/licenses/mit-license.html
[swc-about]: https://software-carpentry.org/about/
[cp-about]: https://carpentries.org/about
