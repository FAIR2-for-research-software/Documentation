---
title: 'Writing README files'
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 

- What is a README file?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Explain why and how to write a README file
- Demonstrate how to include pieces of code, figures, and nested challenge blocks

::::::::::::::::::::::::::::::::::::::::::::::::

## Introduction

A README file is the first thing a user sees when they find your software. It should give them an approachable overview of the package, define what’s possible to achieve with this code, and get them started on the right track to use the software effectively for their research.

A README contains a brief introduction to the code and shows them how to get started using it. For larger packages, the README forms a concise beginner guide and might link to a more detailed user guide that is located elsewhere.

## How to write a README

To start writing a README file, the simplest way is to just create an empty text file called README.txt and start writing. This file should be located in the directory (or folder) that contains your software project. 

Most people prefer to use a file format that allows you to create headers to organise the content into sections or chapters, which is much clearer for the reader. In this case, a Markdown document may be used. Markdown is a simple markup language that allows you to format your text using symbols to represent headers, bold text, bullet lists, etc. that are displayed to the user in an appealing way.

An example README file in Markdown format is shown below, in a file called README.md where .md is the file extension for Markdown files.

```md
# My research software

This software is designed to...

# Installation

To install this software...

# Usage

To use this package...
```

The “#” symbol means that line will be converted into a header and displayed to the reader in a large, bold font.

If your code is published on GitHub, the home page of your code repository will display the README.md file, including a navigation menu that is automatically created to easily select the section of the document to view.

!["Imagename"](fig/bootstrap-readme-chapters.png)

