---
title: 'Instructor Notes'
---

## Slides

The slides for this lesson are available on [Google Slides](https://docs.google.com/presentation/d/1XFIGfwBwOAxAW1strp3riXYyqFfw7AoQhg1LLKKvT8k/edit?usp=sharing).

The presentation course of this course should be modified depending on the target audience.

Many beginner coders in the research world will not need to know advanced skills such as how to automatically generate
and deploy documentation websites, but some introductory material on this topic is here if required.

## System Setup

Run through the following pre-flight checks with learners at the start of the session.
The learner-facing [Setup page](../learners/setup.md) has full installation instructions.

### GitHub

Both the instructor and learners should be logged into [GitHub](https://github.com).
This is needed to access the [example repository](https://github.com/Joe-Heffer-Shef/oddsong) and to raise
questions or issues during the workshop.
Learners without an account can [sign up for free](https://github.com/signup).

### Visual Studio Code

Confirm that [Visual Studio Code](https://code.visualstudio.com/) opens and that the appropriate language extension
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
