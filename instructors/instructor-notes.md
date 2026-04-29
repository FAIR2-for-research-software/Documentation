---
title: 'Instructor Notes'
---

The presentation of this course should be adapted to the target audience. Beginner researchers may not
need advanced topics such as automatically generating and deploying documentation websites; those episodes
can be skipped, but the material is included here if required.

## Slides

The slides for this lesson are available on [Google Slides](https://docs.google.com/presentation/d/1XFIGfwBwOAxAW1strp3riXYyqFfw7AoQhg1LLKKvT8k/edit?usp=sharing).

## System Setup

Run through the following pre-flight checks with learners at the start of the session.
The learner-facing [Setup page](../learners/setup.md) has full installation instructions.

### GitHub

Ensure all learners are logged into [GitHub](https://github.com).
This is needed to access the [example repository](https://github.com/Joe-Heffer-Shef/oddsong) and to raise
questions or issues during the workshop.
Learners without an account can [sign up for free](https://github.com/signup).

### Visual Studio Code

Verify that [Visual Studio Code](https://code.visualstudio.com/) opens and that the appropriate language extension
is installed and active:

- **Python**: the [Python extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python) by Microsoft.
- **R**: the [R extension](https://marketplace.visualstudio.com/items?itemName=REditorSupport.r) by REditorSupport.

Show learners how to open a project folder via **File → Open Folder**.

### Virtual Environment (Python)

For Python learners, verify they can create and activate a virtual environment before installing any packages.

```bash
python -m venv .venv
```

Activation command by platform:

| Platform | Command |
| -------- | ------- |
| macOS / Linux | `source .venv/bin/activate` |
| Windows (Command Prompt) | `.venv\Scripts\activate.bat` |
| Windows (PowerShell) | `.venv\Scripts\Activate.ps1` |

The shell prompt should show `(.venv)` once the environment is active.

**Note:** Python must be available (any distribution, including Anaconda) for learners who will use
`mkdocs` to build documentation websites. Confirm this early — learners without Python cannot complete
that episode.

### Package Installation (R)

R learners do not need a virtual environment. Confirm that R and the R extension for VS Code are
working, then check that learners can install packages with `install.packages()`.

If the workshop uses `renv` for reproducible environments, verify that learners can run:

```r
renv::restore()
```
