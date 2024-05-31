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

A documentation site bring all your user guidance into one place. This kind of resource may be prepared for research software and will usually contain an introduction, installation instructions, a user guide, troubleshooting tips, and an in-depth reference section.

To get an idea of this, here are some links documentation websites for widely-used data analysis and research software packages:

- [pandas](https://pandas.pydata.org/docs/) is a data processing library for the Python programming language.
- [ggplot2](https://ggplot2.tidyverse.org/index.html) is a plotting package for the R statistical language.
- [scikit-learn](https://scikit-learn.org/stable/user_guide.html) is a machine learning library for the Python programming language.

### Advantages

There are many advantages to building a documentation site to provide a information-rich resource for researchers who use your code at institutions all around the world. These sites can work as hubs for collaboration, sharing the latest updates, and encouraging people to take up your system and get involved in improving it. The effort of setting one up will be rewarded in the long run because you will have created a valuable asset that will foster collaboration and knowledge sharing in your research community.

A key foundation stone of modern digital research practices is the ability to replicate results by reproducing analysis workflows.  Clear, thorough documentation of the research code ensures that researchers can repeat processes and verify results and other people's outputs.

Documementation sites are really useful for introducing new users to your software. It makes it much easier and faster for new users to get started using your software to boost their research. It's one of the most effective ways to create a user base that has a sophisticated understanding of the research code, which is essential for them to adapt it to the complex problems that often raise in research contexts.

They're also a valuable resource for your existing user base, enabling them to look up reference material or search the manual to find new capabilities they weren't aware of before. This will increase the potential for your software to accellerate the productivity of other research teams and boost scientific progress.

### When to use one

Although the advantages are numerous, not all software packages require a comprehensive documentation website. However, for any code project that is growing in the number of collaborators, users, and technicala complexity, consider coordinating the team to write one as soon as possible to help the project grow in a healthy manner.

### Writing style

Strive to use everyday, jargon-free language. It helps to set an approachable tone that encourages others to use the software and get involved with the project. This will en sure that the code is accesible to the widest possible layers of the research community and foster collaboration.

Always consider the target audience of your documentation, because your user base may be unaware of some of the unstated assumptions and technical backgroud knowledge that you take for granted.

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

This prevents a situation where potential solutions to common issues do exist, but are scattered around the internet are the exclusive knowledge of a few individuals and are hard to find.

### FAQs

An appendix containing frequently asked questions (FAQs) is very useful to save yourself time in responding to common queries from the users of your code.

## Docsite tools

There are various tools available to build documentation sites for your research software.

### GitHub Wiki

If you are publishing your code on GitHub, which is a web service that hosts costs repositories, then one of the easiest ways to create a documentation site is to use the wiki feature on that platform. This is a great way to write detailed, structured documents containing long-form content that describes aspects of your software. What's more, it's available alongside your code so your documentation and software are located in one place.

As with readme files, the text that appears on GitHub is [formatted using Markdown syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github).

#### Getting started

To create a wiki, go to the main page of your code repository on GitHub and click on the Wiki button on the top menu. For a detailed walkthrough of this process, please read [adding or editing wiki pages](https://docs.github.com/en/communities/documenting-your-project-with-wikis/adding-or-editing-wiki-pages) on the GitHub documentation.

::: callout

For more information about the wiki feature on GitHub, see [Documenting your project with wikis](https://docs.github.com/en/communities/documenting-your-project-with-wikis) on the GitHub documentation.

:::

### Sphinx

TODO

### MkDocs

TODO

## Publishing your docsite

### GitHub pages

TODO

[GitHub Pages documentation](https://docs.github.com/en/pages)

### Read the Docs

TODO

::::::::::::::::::::::::::::::::::::: keypoints 

- Structured documentation websites are very useful for users to learn to use all kinds of digital systems.
- Documentation sites contain comprehensive installation instructions, user guides, and troubleshooting tips.
- There are several libraries that may be used to generate documentation sites.
- Documentation websites may be deployed to a hosting platform.

::::::::::::::::::::::::::::::::::::::::::::::::
