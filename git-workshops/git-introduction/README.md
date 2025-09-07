# Git and GitHub Workshop

This tutorial modifies content from [Jenna Jordan's Intro to Git & GitHub (Speedrun edition)](https://jennajordan.me/git-novice-speedrun/), which draws from the [Software Carpentry Version Control with Git lesson](https://swcarpentry.github.io/git-novice/), the [Carpentries Incubator Version Control with Git lesson](https://carpentries-incubator.github.io/git-novice-branch-pr/), and the [Library Carpentry Introduction to Git lesson](https://librarycarpentry.github.io/lc-git/).

> [!NOTE]
> All Carpentries (Software Carpentry, Data Carpentry, and Library Carpentry) instructional material is made available under the Creative Commons Attribution license. The following is a human-readable summary of (and not a substitute for) the full legal text of the CC BY 4.0 license. See [LICENSE.md](./LICENSE.md) for details.

The actual delivered content is designed to be taught in 90 minutes, but requires learners to complete set-up and installation steps prior to the workshop.

The workshop prioritizes the typical developer workflow, which is why it is taught in VS Code with a bash terminal, and starts with the creation of the repo on GitHub rather than the local computer. Terminal commands are used first, before the VS Code Source Control pane is introduced. Learners should be encouraged to use the workflow they are most comfortable with.

## Setup

Please complete [the setup instructions](/git-novice-speedrun/1_setup) prior to the workshop. In order to participate in this workshop, you must have a GitHub account, and have VS Code, git, and bash installed on your computer.

## Git Cheatsheets for Quick Reference

* A great [printable git cheatsheet](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf) is available in PDF from the
[GitHub training website](https://services.github.com/resources/).
* An [interactive one-page visualisation](http://ndpsoftware.com/git-cheatsheet.html)
    about the relationships between workspace, staging area, local repository, upstream repository, and the commands associated with each (with explanations).
* Both resources are also available in other languages e.g. Spanish, French, and more
* "[Happy Git and GitHub for the useR](http://happygitwithr.com)" is an accessible, free online book by Jenny Bryan on how to setup and use git and GitHub with specific references on the integration of git with RStudio and working with git in R.

## Glossary

changeset
:   A group of changes to one or more files that are or will be added
    to a single commit in a version control
    repository.

commit
:   To record the current state of a set of files (a changeset)
    in a version control repository. As a noun,
    the result of committing, i.e. a recorded changeset in a repository.
    If a commit contains changes to multiple files,
    all of the changes are recorded together.

conflict
:   A change made by one user of a version control system
    that is incompatible with changes made by other users.
    Helping users resolve conflicts
    is one of version control's major tasks.

HTTP
:   The Hypertext Transfer Protocol used for sharing web pages and other data
    on the World Wide Web.

merge
:   (a repository): To reconcile two sets of changes to a
    repository.

protocol
:   A set of rules that define how one computer communicates with another.
    Common protocols on the Internet include HTTP and SSH.

remote
:   (of a repository) A version control repository connected to another,
    in such way that both can be kept in sync exchanging commits.

repository
:   A storage area where a version control system
    stores the full history of commits of a project and information
    about who changed what, when.

resolve
:   To eliminate the conflicts between two or more incompatible changes to a file or set of files
    being managed by a version control system.

revision
:   A synonym for commit.

SHA-1
:   [SHA-1 hashes](https://en.wikipedia.org/wiki/SHA-1) is what Git uses to compute identifiers, including for commits.
    To compute these, Git uses not only the actual change of a commit, but also its metadata (such as date, author,
    message), including the identifiers of all commits of preceding changes. This makes Git commit IDs virtually unique.
    I.e., the likelihood that two commits made independently, even of the same change, receive the same ID is exceedingly
    small.

SSH
:   The Secure Shell protocol used for secure communication between computers.

timestamp
:   A record of when a particular event occurred.

version control
:   A tool for managing changes to a set of files.
    Each set of changes creates a new commit of the files;
    the version control system allows users to recover old commits reliably,
    and helps manage conflicting changes made by different users.

This lesson was built with [The Carpentries Workbench](https://carpentries.github.io/sandpaper-docs). The content was adapted from the [Software Carpentry Version Control with Git lesson](https://swcarpentry.github.io/git-novice/), the [Carpentries Incubator Version Control with Git lesson](https://carpentries-incubator.github.io/git-novice-branch-pr/) that incorporates branches and PRs, and the [Library Carpentry Introduction to Git lesson](https://librarycarpentry.github.io/lc-git/).
This lesson is designed to contain only the minimal amount of information to get learners functional with Git & GitHub, and should not be considered a comprehensive introduction to git.

The goal of this lesson is to introduce core git concepts and commands while following a common git workflow pattern. Learners will start with creating a repository on GitHub, then use VS Code to clone the repo, make edits locally, and push those changes to the remote GitHub repo.

Bash is not a pre-requisite for this lesson, and any bash commands used (like `pwd` or `ls -a`) are purely optional. The VS Code interface is used to create new files, and provides a GUI interface that learners should be more comfortable with compared to a purely terminal-based workflow.

By the end of the lesson, learners should be ready to follow the same workflow in a repo of their own creation/choosing, and understand the core git commands: `config`, `status`, `log`, `add`, `commit`, `diff`, `push`, `pull`, and `branch`. They should be comfortable using both the terminal and the VS Code Source Control pane to perform these git operations.
