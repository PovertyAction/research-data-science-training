# shell-novice

An introduction to the Unix shell for people who have never used the command line before.
Please see [https://swcarpentry.github.io/shell-novice/](https://swcarpentry.github.io/shell-novice/)
for a rendered version of this material
for instructions on formatting, building, and submitting material.

The Unix shell has been around longer than most of its users
have been alive. It has survived because it's a powerful tool that
allows users to perform complex and powerful tasks, often with just
a few keystrokes or lines of code. It helps users automate repetitive
tasks and easily combine smaller tasks into larger, more powerful workflows.

Use of the shell is fundamental to a wide range of advanced computing
tasks, including high-performance computing. These lessons will introduce
you to this powerful tool.

## Prerequisites

This lesson guides you through the basics of file systems and the
shell. If you have stored files on a computer at all and recognize
the word "file" and either "directory" or "folder" (two common words
for the same thing), you're ready for this lesson.

## Download files

You need to download some files to follow this lesson.

1. Download [shell-lesson-data.zip][zip-file] and move the file to your Desktop.
2. Unzip/extract the file.
  **Let your instructor know if you need help with this step**.
  You should end up with a new folder called **`shell-lesson-data`** on your Desktop.

## Install software

If you do not already have the shell software installed, you will need to
[download and install][install_shell] it.

## Open a new shell

After installing the software

1. Open a terminal.
  If you're not sure how to open a terminal on your operating system, see the instructions below.
1. In the terminal type `cd` then press the <kbd>Return</kbd> key.
  This step will make sure you start with your home folder as your working directory.

In the lesson, you will find out how to access the data files in this folder.

:::::::::::::::::::::::::::::::::::::::::  callout

## Where to type commands: How to open a new shell

The shell is a program that enables us to send commands to the computer and receive output.
It is also referred to as the terminal or command line.

Some computers include a default Unix Shell program.
The steps below describe some methods for identifying and opening
a Unix Shell program if you already have one installed.
There are also options for identifying and downloading a Unix Shell program,
a Linux/UNIX emulator, or a program to access a Unix Shell on a server.

If none of the options below address your circumstances,
try an online search for: Unix shell [your computer model] [your operating system].

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::: solution

### Windows {#windows}

Computers with Windows operating systems do not automatically have a Unix Shell program
installed.
In this lesson, we encourage you to use an emulator included in [Git for Windows][install_shell],
which gives you access to both Bash shell commands and Git.

Once installed, you can open a terminal by running the program Git Bash from the Windows start
menu.

**For advanced users:**

As an alternative to Git for Windows you may wish to [Install the Windows Subsystem for Linux][wsl]
which gives access to a Bash shell command-line tool in Windows 10 and above.

Please note that commands in the Windows Subsystem for Linux (WSL) may differ slightly
from those shown in the lesson or presented in the workshop.

::::::::::::

:::::::::::: solution

### MacOS {#macos}

For a Mac computer running macOS Mojave or earlier releases, the default Unix Shell is Bash.
For a Mac computer running macOS Catalina or later releases, the default Unix Shell is Zsh.
Your default shell is available via the Terminal program within your Utilities folder.

To open Terminal, try one or both of the following:

- In Finder, select the Go menu, then select Utilities.
  Locate Terminal in the Utilities folder and open it.
- Use the Mac 'Spotlight' computer search function.
  Search for: `Terminal` and press <kbd>Return</kbd>.

To check if your machine is set up to use something other than Bash,
type `echo $SHELL` in your terminal window.

If your machine is set up to use something other than Bash,
you can run it by opening a terminal and typing `bash`.

[How to Use Terminal on a Mac][mac-terminal]

::::::::::::

:::::::::::: solution

### Linux {#linux}

The default Unix Shell for Linux operating systems is usually Bash.
On most versions of Linux, it is accessible by running the
[Gnome Terminal][gnome-terminal] or [KDE Konsole][kde-konsole] or [xterm],
which can be found via the applications menu or the search bar.
If your machine is set up to use something other than Bash,
you can run it by opening a terminal and typing `bash`.

::::::::::::

[zip-file]: data/shell-lesson-data.zip
[install_shell]: https://carpentries.github.io/workshop-template/install_instructions/#shell
[wsl]: https://learn.microsoft.com/en-us/windows/wsl/install
[mac-terminal]: https://www.macworld.co.uk/feature/mac-software/how-use-terminal-on-mac-3608274/
[gnome-terminal]: https://help.gnome.org/users/gnome-terminal/stable/
[kde-konsole]: https://konsole.kde.org/
[xterm]: https://en.wikipedia.org/wiki/Xterm

## Summary of Basic Commands

| Action       | Files | Folders      |
| ------------ | ----- | ------------ |
| Inspect      | ls    | ls           |
| View content | cat   | ls           |
| Navigate to  |       | cd           |
| Move         | mv    | mv           |
| Copy         | cp    | cp -r        |
| Create       | nano  | mkdir        |
| Delete       | rm    | rmdir, rm -r |

## Filesystem hierarchy

The following is an overview of a standard Unix filesystem.
The exact hierarchy depends on the platform. Your file/directory structure may differ slightly:

![Linux filesystem hierarchy](figures/standard-filesystem-hierarchy.svg)

## Glossary

[absolute path]{#absolute-path}
:   A path that refers to a particular location in a file system.
Absolute paths are usually written with respect to the file system's
root directory,
and begin with either "/" (on Unix) or "\\" (on Microsoft Windows).
See also: relative path.

[argument]{#argument}
:   A value given to a function or program when it runs.
The term is often used interchangeably (and inconsistently) with parameter.

[command shell]{#command-shell}
:   See shell

[command-line interface]{#command-line-interface}
:   A user interface based on typing commands,
usually at a REPL.
See also: graphical user interface.

[comment]{#comment}
:   A remark in a program that is intended to help human readers understand what is going on,
but is ignored by the computer.
Comments in Python, R, and the Unix shell start with a `#` character
and run to the end of the line;
comments in SQL start with `--`,
and other languages have other conventions.

[current working directory]{#current-working-directory}
:   The directory that relative paths are calculated from;
equivalently,
the place where files referenced by name only are searched for.
Every process has a current working directory.
The current working directory is usually referred to using the shorthand notation `.`
(pronounced "dot").

[file system]{#file-system}
:   A set of files, directories, and I/O devices (such as keyboards and screens).
A file system may be spread across many physical devices,
or many file systems may be stored on a single physical device;
the operating system manages access.

[filename extension]{#filename-extension}
:   The portion of a file's name that comes after the final "." character.
By convention this identifies the file's type:
`.txt` means "text file", `.png` means "Portable Network Graphics file",
and so on. These conventions are not enforced by most operating systems:
it is perfectly possible (but confusing!) to name an MP3 sound file `homepage.html`.
Since many applications use filename extensions to identify the
MIME type of the file,
misnaming files may cause those applications to fail.

[filter]{#filter}
:   A program that transforms a stream of data.
Many Unix command-line tools are written as filters:
they read data from standard input,
process it, and write the result to standard output.

[for loop]{#for-loop}
:   A loop that is executed once for each value in some kind of set, list, or range.
See also: while loop.

[graphical user interface]{#graphical-user-interface}
:   A user interface based on selecting items and actions from a graphical display,
usually controlled by using a mouse.
See also: command-line interface.

[home directory]{#home-directory}
:   The default directory associated with an account on a computer system.
By convention, all of a user's files are stored in or below her home directory.

[loop]{#loop}
:   A set of instructions to be executed multiple times.
Consists of a loop body and (usually) a
condition for exiting the loop. See also for loop and while loop.

[loop body]{#loop-body}
:   The set of statements or commands that are repeated inside a for loop
or while loop.

[MIME type]{#mime-type}
:   MIME (Multi-Purpose Internet Mail Extensions) types describe different file types for exchange
on the Internet, for example, images, audio, and documents.

[operating system]{#operating-system}
:   Software that manages interactions between users, hardware, and software processes.
Common examples are Linux, macOS, and Windows.

[option]{#option}
:   A way to specify an argument or setting to a command-line program.
By convention Unix applications use a dash followed by a single letter,
such as `-v`, or two dashes followed by a word, such as `--verbose`,
while DOS applications use a slash, such as `/V`.
Depending on the application, an option may be followed by a single argument,
as in `-o /tmp/output.txt`.

[parameter]{#parameter}
:   A variable named in a function's declaration that is used to hold a value passed into the call.
The term is often used interchangeably (and inconsistently) with argument.

[parent directory]{#parent-directory}
:   The directory that "contains" the one in question.
Every directory in a file system except the root directory has a parent.
A directory's parent is usually referred to using the shorthand notation `..`
(pronounced "dot dot").

[path]{#path}
:   A description that specifies the location of a file or directory within a
file system.
See also: absolute path, relative path.

[pipe]{#pipe}
:   A connection from the output of one program to the input of another.
When two or more programs are connected in this way, they are called a "pipeline".

[process]{#process}
:   A running instance of a program, containing code, variable values,
open files and network connections, and so on.
Processes are the "actors" that the operating system manages;
it typically runs each process for a few milliseconds at a time
to give the impression that they are executing simultaneously.

[prompt]{#prompt}
:   A character or characters display by a REPL to show that
it is waiting for its next command.

[quoting]{#quoting}
:   (in the shell):
Using quotation marks of various kinds to prevent the shell from interpreting special
characters.
For example, to pass the string `*.txt` to a program,
it is usually necessary to write it as `'*.txt'` (with single quotes)
so that the shell will not try to expand the `*` wildcard.

[read-evaluate-print loop]{#read-evaluate-print-loop}
:   (REPL): A command-line interface that reads a command from the user,
executes it, prints the result, and waits for another command.

[redirect]{#redirect}
:   To send a command's output to a file rather than to the screen or another command,
or equivalently to read a command's input from a file.

[regular expression]{#regular-expression}
:   A pattern that specifies a set of character strings.
REs are most often used to find sequences of characters in strings.

[relative path]{#relative-path}
:   A path that specifies the location of a file or directory
with respect to the current working directory.
Any path that does not begin with a separator character ("/" or "\\") is a relative path.
See also: absolute path.

[root directory]{#root-directory}
:   The top-most directory in a file system.
Its name is "/" on Unix (including Linux and macOS) and "\\" on Microsoft Windows.

[shell]{#shell}
:   A command-line interface such as Bash (the Bourne-Again Shell)
or the Microsoft Windows DOS shell
that allows a user to interact with the operating system.

[shell script]{#shell-script}
:   A set of shell commands stored in a file for re-use.
A shell script is a program executed by the shell;
the name "script" is used for historical reasons.

[standard input]{#standard-input}
:   A process's default input stream.
In interactive command-line applications,
it is typically connected to the keyboard;
in a pipe,
it receives data from the standard output of the preceding process.

[standard output]{#standard-output}
:   A process's default output stream.
In interactive command-line applications,
data sent to standard output is displayed on the screen;
in a pipe,
it is passed to the standard input of the next process.

[sub-directory]{#sub-directory}
:   A directory contained within another directory.

[tab completion]{#tab-completion}
:   A feature provided by many interactive systems in which
pressing the Tab key triggers automatic completion of the current word or command.

[variable]{#variable}
:   A name in a program that is associated with a value or a collection of values.

[while loop]{#while-loop}
:   A loop that keeps executing as long as some condition is true.
See also: for loop.

[wildcard]{#wildcard}
:   A character used in pattern matching.
In the Unix shell,
the wildcard `*` matches zero or more characters,
so that `*.txt` matches all files whose names end in `.txt`.

## External references

### Opening a terminal

- [How to Use Terminal on a Mac](https://www.macworld.co.uk/feature/mac-software/how-use-terminal-on-mac-3608274/)
- [Git for Windows](https://git-for-windows.github.io/)
- [How to Install Bash shell command-line tool on Windows 10](https://www.windowscentral.com/how-install-bash-shell-command-line-windows-10)
- [Install and Use the Linux Bash Shell on Windows 10](https://www.howtogeek.com/249966/how-to-install-and-use-the-linux-bash-shell-on-windows-10/)
- [Using the Windows 10 Bash Shell](https://www.howtogeek.com/265900/everything-you-can-do-with-windows-10s-new-bash-shell/)
- [Using a UNIX/Linux emulator (Cygwin) or Secure Shell (SSH) client (Putty)](https://faculty.smu.edu/reynolds/unixtut/windows.html)

### Manuals

- [GNU manuals](https://www.gnu.org/manual/manual.html)
- [Core GNU utilities](https://www.gnu.org/software/coreutils/manual/coreutils.html)

### Miscellaneous

- [North Pacific Gyre](https://en.wikipedia.org/wiki/North_Pacific_Gyre)
- [Great Pacific Garbage Patch](https://en.wikipedia.org/wiki/Great_Pacific_Garbage_Patch)
- ['Ensuring the longevity of digital information' by Jeff Rothenberg](https://www.clir.org/pubs/archives/ensuring.pdf)
- [Computer error haikus](https://wiki.c2.com/?ComputerErrorHaiku)
- [How to name files nicely, by Jenny Bryan](https://speakerdeck.com/jennybc/how-to-name-files)

## Additional Resources

To learn more about the Unix shell you may want to explore the
[shell-extras](https://carpentries-incubator.github.io/shell-extras/) lesson in the Carpentries Incubator.

---

## Discussion

## Alphabet Soup

If the command to find out who we are is `whoami`, the command to find
out where we are ought to be called `whereami`, so why is it `pwd`
instead? The usual answer is that in the early 1970s, when Unix was
first being developed, every keystroke counted: the devices of the day
were slow, and backspacing on a teletype was so painful that cutting the
number of keystrokes in order to cut the number of typing mistakes was
actually a win for usability. The reality is that commands were added to
Unix one by one, without any master plan, by people who were immersed in
its jargon. The result is as inconsistent as the roolz uv Inglish
speling, but we're stuck with it now.

## Job Control Codes

The shell accepts a few special commands that allow users to interact
with running processes or programs. You can enter each of these
"control codes" by holding down the `Ctrl` key and then pressing one
of the control characters. In other tutorials, you may see the term
`Control` or the `^` used to represent the `Ctrl` key (e.g. the
following are all equivalent `Ctrl-C`, `Ctrl+C`, `Control-C`, `Control+C`, `^C`).

- `Ctrl-C`:
  interrupts and cancels a running program.
  This is useful if you want to cancel a command that is taking too long to execute.

- `Ctrl-D`:
  indicates the end of a file or stream of characters that you are entering on the command line.
  For example, we saw earlier that the `wc` command counts lines, words, and characters in a file.
  If we just type `wc` and hit the Enter key without providing a file name,
  then `wc` will assume we want it to analyze all the stuff we type next.
  After typing our magnum opus directly into the shell prompt,
  we can then type Ctrl-D to tell `wc` that we're done
  and we'd like to see the results of the word count.

- `Ctrl-Z`:
  Suspends a process but does not terminate it.
  You can then use the command `fg` to restart the job in the foreground.

For new shell users, these control codes can all appear to have
the same effect: they make things "go away." But it is helpful to
understand the differences. In general, if something went wrong and
you just want to get your shell prompt back, it is better to use
`Ctrl-C`.

## Other Shells

Before Bash became popular in the end of nineties, scientists widely
used (and some still use) another shell, C-shell, or Csh. Bash and Csh
have similar feature sets, but their syntax rules are different and
this makes them incompatible with each other. A few other shells have
appeared since, including ksh, zsh, and a number of others; they are
mostly compatible with Bash, and Bash is the default shell on most
modern implementations of Unix (including most packages that provide
Unix-like tools for Windows) but if you get strange errors in shell
scripts written by colleagues, check to see which shell they were
written for.

## Bash Configurations

Want to customize paths, environment variables, aliases,
and other behaviors of your shell?
This excellent blog post "[Bash Configurations Demystified][bash-demystified]"
from Dalton Hubble
covers tips, tricks, and how to avoid dangers.

[bash-demystified]: https://blog.dghubble.io/posts/.bashprofile-.profile-and-.bashrc-conventions/
