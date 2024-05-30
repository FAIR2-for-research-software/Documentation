---
title: 'Documentation sites'
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 

- What is a documentation website for research software?
- How do I generate a website containing a user guide to my code?
- What should my documentation site contain?
- How do I publish my software documentation on the internet?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Learn about documentation websites for software packages.
- Gain basic familiarity with some common website generation tools.
- Understand the basics of structuring a documentation website.
- Be able to set up a static site deployment workflow.

::::::::::::::::::::::::::::::::::::::::::::::::

## Documentation sites

A documentation website is a user guide and reference manual for a library of research code. Up to now, we've looked at ways to put helpful notes in our code, but now we'll learn how to write a longer, more complete guide to the research tools you create.

A documentation site for research software usually contains an introduction, installation instructions, a user guide, troubleshooting tips, and an in-depth reference section.

To get an idea of this, here are some links documentation websites for widely-used data analysis and research software packages:

- [pandas](https://pandas.pydata.org/docs/) is a data processing library for the Python programming language.
- [ggplot2](https://ggplot2.tidyverse.org/index.html) is a plotting package for the R statistical language.
- [scikit-learn](https://scikit-learn.org/stable/user_guide.html) is a machine learning library for the Python programming language.

### Advantages

It makes it much easier for new users to get started using your software to boost their research.

### When to use one

TODO

## Docsite contents

Documentation pages contain comphrehensive information about a particular piece of research software. Think of it like a user manual for your car or an instruction guide for building a piece of furniature.

### Research context

For research software, it may be important to explain the theoretical background or statistical methods that are used and explain the domain-specific assumptions that were made when the code was designed and written. It's good practice to provide a concise summary of the relevent concepts and link to external sources such as papers, books, and other websites for users to take a deeper dive into the principles and algorithms used.

### Installation instructions

This section provides a detailed walkthrough of the steps required to install the package onto their computer, with details that are specific to their operating system.

### Tutorials

It can be very useful to include an in-depth "Getting Started" guide that provides step-by-step instructions to introduce a new user to your software package. It might guide the user through each aspect of the tool's functionality and features so they're able to become familiar with it in a more approachable way.

A series of code examples to demonstrate how to use the software in different contexts can be very useful for users to get off the ground in implementing common research workflows to achieve their specific goals.

### User reference

If you have written functions that are intended to be use in other reseachers' code, then an on-depth explaination of these procedures is essential reference material. In the world of software engineering, these detailed appendices are called <acronym title="Application Programming Interfaces">API</acronym> references, which list each function and describe how the arguments may be used to control how the code works. This content may be automatically generated from the documentation strings.

### Troubleshooting

As issues come up with your research code, and are eventually resolved and clarified, make a note of the causes of these troubles and make them available to the entire user base in your documentation site. This will help users to identify and fix common misunderstandings and technical problems they may run into when utilising your code.

### FAQs

An appendix containing frequently asked questions (FAQs) is very useful to save yourself time in responding to common queries from the users of your code.

## Docsite tools

GitHub Wiki

Sphinx

MkDocs

## Publishing your docsite

GitHub pages

Read the Docs

::::::::::::::::::::::::::::::::::::: keypoints 

- Structured documentation websites are very useful for users to learn to use all kinds of digital systems.
- There are several libraries that may be used to generate documentation sites.
- Documentation websites may be deployed to a hosting platform.

::::::::::::::::::::::::::::::::::::::::::::::::
