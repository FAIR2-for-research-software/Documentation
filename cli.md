---
title: 'Command line interfaces'
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 

- What is a command-line interface (CLI)?
- Why are they useful for making software easier to use for researchers?
- How do I create a <acronym title="command-line interface">CLI</acronym> for my research code?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Learn what a command-line interface is
- Understand the benefits of <acronym title="command-line interfaces">CLIs</acronym>  for making research code more accessible?
- Gain a basic familiarity with the `argparse` module in Python

::::::::::::::::::::::::::::::::::::::::::::::::

## Command line interfaces

A command-line interface, usually abbreviated to CLI, is a terminal or prompt that accepts text input that instructs a computer what to do. They are used to start programs and perform actions within the computer's operating system.

In this section, we'll introduce the concept of providing a command-line interface to our research code to make it easier to use and provide a well-documented "entry point" to our software.

### Advantages

Command lines are a way of interacting with a digital system that go back to the early history of computing. They might seem old-fashioned because typing out commands means that there is no graphical component. It may seem restrictive because your mouse isn't used, but terminals have a lot of power because we can formulate our instructions to the computer by writing commands. We have a direct line to control our computer's operating system.

It's a great way to talk to your computer because you can record the commands that you've run to provide a documented history of a research process. (We could record a video screen capture of your working procedure, but that's much less efficient.)

Terminals are more efficient for running repetitive tasks and provide extra functionality for advanced users. They are an cost-effective way to provide a user interface for research software, as research teams often lack the resources and know-how to produce sophisticated graphical user interfaces.

## Using the terminal

There's a lot of powerful commands that can be learned to take full advantage of the command line, but here we'll just address the basics to help us make our research software easier to use by providing a well-documented CLI.

### How to open the command line

Each operating system has a slightly different terminal interface, but they work in basically the same way.

::: group-tab

### Windows

On Windows operating systems, press the Windows key and type in "command". The start menu will find the "Command Prompt" app. Press <kbd>Enter</kbd> or click on the Command Prompt icon to launch the terminal.

You can also launch the command prompt by pressing <kbd>Windows + R</kbd> and typing `cmd`.

The command prompt tool will open a black terminal window that looks something like this:

```bash
Microsoft Windows [Version 10.0.19045.4412]
(c) Microsoft Corporation. All rights reserved.

C:\Users\bob>
```

For more information, see the [Windows Commands](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands) page on the Windows Server documentation.

### Linux

On Ubuntu, press <kbd>Ctrl + Alt + T</kbd> to open a terminal.

You can also open Dash and search for "Terminal". For detailed instructions, please read [Opening a terminal](https://ubuntu.com/tutorials/command-line-for-beginners#3-opening-a-terminal) section in the [The Linux command line for beginners](https://ubuntu.com/tutorials/command-line-for-beginners#1-overview) tutorial in the official Ubuntu documentation.

The terminal on an Ubuntu computer will look something like this, where the dollar sign `$` means "type here".

```bash
bob@myUbuntuPC:~$
```

### Mac OS

Please read [Open or quit Terminal on Mac](https://support.apple.com/en-gb/guide/terminal/apd5265185d-f365-44cb-8b09-71a064a42125/mac) on the [Terminal User Guide](https://support.apple.com/en-gb/guide/terminal/welcome/mac) for macOS.

:::

### Example commands

An example of a CLI command is a simple text command that performs some action or interacts with the computer operating system. 

Let's examine a simple one-word command that lists the files in the current directory.

::: group-tab

Test sentence goes here.

### Windows

On Windows, the [dir](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/dir) command is used to list the contents of a directory. When you enter this command and press <kbd>Enter</kbd>

```bash
> dir
```

The result of this command will be printed to the screen.

```output
C:\temp\my_data>dir
 Volume in drive C has no label.
 Volume Serial Number is Y72W-9DA1

 Directory of C:\temp\my_data

30/05/2024  14:06    <DIR>          .
30/05/2024  14:06    <DIR>          ..
30/05/2024  14:06                12 README.txt
               1 File(s)             12 bytes
               2 Dir(s)  171,395,805,184 bytes free
```

This means that in the folder `C:\temp\my_data` there is a single file called `README.txt`. The date and time that each file was last modified is shown, along with the file size, which is 12 bytes in this case.

### Linux

To show the contents of a directory on a Linux system, we use the [`ls` command](https://manpages.ubuntu.com/manpages/noble/man1/ls.1plan9.html) which lists information about the files in the current location.

```bash
bob@myUbuntuPC:/tmp/my_data$ ls
```

The output is a simple list of the names of all the files in that folder.

```output
README.txt
```

### Mac OS

The macOS terminal is very similar to the Linux one. To show the contents of a directory on a Linux system, we use the [`ls` command](https://support.apple.com/en-gb/guide/terminal/apdb66b5242-0d18-49fc-9c47-a2498b7c91d5/2.14/mac/14.0) which lists information about the files in the current location.

```bash
ls
```

The output is a simple list of the names of all the files in that folder.

```output
README.txt
```

For more information, please read [Get started with Terminal on Mac](https://support.apple.com/en-gb/guide/terminal/pht23b129fed/mac)

:::

```bash
date /T
```

```bash
date
```

```bash
echo Hello world
```

### Advantages of CLIs

### CLIs for research code

## CLIs in Python

### argparse

#### Description

#### Usage

#### options

Help text

#### Using CLIs



::::::::::::::::::::::::::::::::::::: keypoints 

- Command line interfaces (CLIs) are terminal commands that provide an easy-to-use entry point to a software package.
- Researchers can use CLIs to make their research code easier to use by providing well-documented options, hiding the complexity of the software.
- Most programming languages offer frameworks for creating CLIs. In Python, we do this using the `argparse` library.

::::::::::::::::::::::::::::::::::::::::::::::::
