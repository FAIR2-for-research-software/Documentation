---
title: Setup
---

Please complete these steps **before the course begins**. Setup takes around 30–60 minutes, most of which is
waiting for downloads and installers.

## Checklist

You can complete this course using *either* Python **or** R — choose whichever you prefer. You only need to install
one of them.

| Software | Who needs it | Purpose |
| --- | --- | --- |
| [GitHub account](https://github.com/signup) | Everyone | Hosting and sharing code |
| [Visual Studio Code](https://code.visualstudio.com/) | Everyone | Recommended code editor, with a built-in terminal |
| [Git](https://git-scm.com/downloads) | Everyone | Publishing your documentation website to GitHub |
| A web browser | Everyone | Viewing GitHub, the course pages, and your documentation website |
| [Python 3](https://www.python.org/downloads/) | Python learners | Running the course exercises |
| [R](https://cran.rstudio.com/) | R learners | Running the course exercises |
| [RStudio Desktop](https://posit.co/download/rstudio-desktop/) | R learners (optional) | An alternative editor for R |

Some extra packages, such as [MkDocs](https://www.mkdocs.org/), are installed during the course itself, so your
computer will need internet access during the sessions.

::: callout

### University of Sheffield managed computers

At the University of Sheffield, Visual Studio Code and RStudio Desktop are available on managed computers via the
[Software Centre](https://students.sheffield.ac.uk/it-services/software/university-applications) desktop shortcut.
If you can't install software on your computer, please contact IT Services before the course.

:::

## Sample code

An example project is available on GitHub at
[Joe-Heffer-Shef/oddsong](https://github.com/Joe-Heffer-Shef/oddsong). Throughout the course, we will build a similar
collection of scripts. Refer to this example as you work through the course.

## 1. Create a GitHub account

This course uses [GitHub](https://github.com/) to host and share code. Please
[sign up for a free GitHub account](https://github.com/signup) if you do not already have one, and
[sign in](https://github.com/login) before the course begins.

See the [GitHub module of the FAIR4RS course](https://rse.shef.ac.uk/training/fair4rs/) for further guidance.

## 2. Install a text editor

[Visual Studio Code](https://code.visualstudio.com/) (VS Code) is a free, open-source editor with excellent support
for Python, R, and many other languages. It is the recommended editor for this course because it includes a built-in
terminal, so you can edit files and run commands in the same window.

1. [Download and install VS Code](https://code.visualstudio.com/Download) for your operating system.
2. Open VS Code and go to the Extensions view (<kbd>Ctrl + Shift + X</kbd>, or <kbd>Cmd + Shift + X</kbd> on macOS).
3. Install the extension for your chosen language, which adds syntax highlighting and IntelliSense (autocompletion
   and tooltips):
    - [Python extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
    - [R extension](https://marketplace.visualstudio.com/items?itemName=REditorSupport.r)

You can use another editor if you prefer, but the course instructions assume VS Code.

## 3. Install Git

[Git](https://git-scm.com/) is a version control tool. We use it to publish a documentation website to GitHub.

::: group-tab

### Windows

Download and run the [Git for Windows](https://git-scm.com/downloads/win) installer. The default options are fine.

### macOS

Open the Terminal app and run the command below. If Git isn't installed yet, macOS will offer to install the Xcode
Command Line Tools, which include Git.

```bash
git --version
```

### Linux

Install Git using your distribution's package manager. On Ubuntu or Debian:

```bash
sudo apt update
sudo apt install git
```

:::

Then tell Git who you are, using the email address linked to your GitHub account:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

## 4. Install Python *or* R

Follow the instructions for the language you've chosen.

### Python

[Python](https://python.org) is a popular general-purpose language widely used in research computing. This course
uses the built-in functionality of Python 3, plus a few packages that we'll install together during the course.

::: group-tab

### Windows

Download the latest Python 3 installer from [Python Releases for Windows](https://www.python.org/downloads/windows/)
and run it. On the first screen of the installer, tick **Add python.exe to PATH** before clicking **Install Now**.

See [using Python on Windows](https://docs.python.org/3/using/windows.html) for more details.

### macOS

Download the latest Python 3 installer from [Python Releases for macOS](https://www.python.org/downloads/macos/) and
run it.

See [using Python on a Mac](https://docs.python.org/3/using/mac.html) for more details.

### Linux

Most Linux distributions include Python 3. On Ubuntu or Debian, install the `venv` and `pip` tools too, as they're
needed during the course:

```bash
sudo apt update
sudo apt install python3 python3-venv python3-pip
```

See [using Python on Unix platforms](https://docs.python.org/3/using/unix.html) for more details.

:::

If you already use [Anaconda](https://www.anaconda.com/), [Miniconda](https://docs.conda.io/projects/miniconda/), or
[Miniforge](https://github.com/conda-forge/miniforge), you can use that instead.

### R

The [R programming language](https://cran.rstudio.com/) is a statistical package designed for data exploration,
visualization, and data analysis. Many R users work in [RStudio Desktop](https://posit.co/download/rstudio-desktop/),
which you can install alongside VS Code if you prefer it.

::: group-tab

### Windows

[Download R for Windows](https://cran.rstudio.com/bin/windows/base/) and run the installer.

### macOS

[Download R for macOS](https://cran.rstudio.com/bin/macosx/), choosing the installer that matches your Mac's
processor (Apple silicon or Intel), and run it.

### Linux

Follow the [instructions for your distribution](https://cran.rstudio.com/bin/linux/) on CRAN. On Ubuntu or Debian:

```bash
sudo apt update
sudo apt install r-base
```

:::

Next, open R (or RStudio) and install the packages we'll use in the course:

```r
install.packages(c("roxygen2", "optparse"))
```

## 5. Check your installation

Open a terminal and run the commands below. Each should print a version number. In VS Code, open a terminal using
**Terminal → New Terminal** or <kbd>Ctrl + \`</kbd>.

::: group-tab

### Windows

```bash
git --version
python --version
R --version
```

### macOS

```bash
git --version
python3 --version
R --version
```

### Linux

```bash
git --version
python3 --version
R --version
```

:::

You only need the Python **or** the R command to work, depending on which language you chose.

::: spoiler

### Troubleshooting

- **"command not found" or "is not recognized"**: close and reopen your terminal (or VS Code) after installing, so it
  picks up the new software.
- **Python on Windows opens the Microsoft Store**: reinstall Python from python.org and make sure **Add python.exe to
  PATH** is ticked.
- **`R` is not recognized on Windows**: this is common, because the R installer doesn't add R to the PATH. Check
  that R opens from the Start menu instead.

If you're still stuck, please contact the course instructors before the course begins.

:::

## Web-based alternatives

If you can't install software on your computer, you can still follow along with most of the course in a web browser.
You won't be able to build and publish the documentation website, though, as that needs Python installed locally.

- [Google Colab](https://colab.research.google.com/) is a browser-based cloud notebook service.
- [Visual Studio Code for the Web](https://code.visualstudio.com/docs/editor/vscode-web) is a browser-based
  development environment, available at [vscode.dev](https://vscode.dev/).
