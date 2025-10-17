---
title: "Introduction"
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions

- How do we **provide information** to users of our research software?
- Why is documenting code useful for researchers?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Understand the basic purpose of this course
- Learn the **motivation** for learning to document software

::::::::::::::::::::::::::::::::::::::::::::::::

## Introduction

There are many kinds of research software, such as:

* Data processing workflows with multiple steps;
* A library of functions used within a research team to perform certain kinds of analysis;
* Tools designed to collect raw data in the field.

No code is self-explanatory. It’s a tool we design, or, more often, a complex organism that develops as we use it with our colleagues. To explain our code we must write **software documentation**.

This **provides information** about our programs for everyone involved in its development, use, and future reuse. Documentation may consist of text, tips within a computer environment, and diagrams that guide the user in using a (potentially complex) software tool. It explains *how* the software works *why* it behaves the way it does.

## Why document our code?

We often encounter software packages, whether written by ourselves, a colleague, or someone else, that’s difficult to use because it’s unclear what it does and how it works. Maybe we try to read the source code itself, but we can’t make head-nor-tail of it. Sometimes it seems like the only person who can use this software is the person who wrote it. Other times, you wrote the code forgot what you were thinking when you did!

:::: challenge

**Discuss positive and negative experiences** with using research software. Think of times when you've used unfamiliar code or tools in your research projects in the past.

- What challenges did you have picking up a new tool?
- What documentation was available?
- What useful instruction manuals or reference guides do you often refer to in your research projects?

::::

### Advantages of good documentation

There are many **advantages to writing guidance** to go along with your research software. Software documentation helps yourself and others to use it successfully in the future. If others can read your code then that ensures that its value is sustained.

Research outputs often **depend upon the code** used to generate them. Clarity and confidence are essential in using code to perform calculations, simulations, or data analysis. All kinds of research processes and analysis pipelines can be made more **reproducible** by providing clear context and instructions for using it.

There are many advantages to making your **code more readable**, too. Well-written software is easier to maintain and has greater **sustainability**. This means it can continue to be used and modified for a longer period of time, despite changes in technology. If software is more reusable then it encourages others to use it for their research, increasing the number of citations of that software and its overall **research impact**.

:::: challenge

Discuss the benefits of writing documentation for your research software.

- How will it help you and your work?
- What benefits will it provide to your collaborators?
- In what ways does documentation contribute to the wider research community?

::::

In the long run, it can also help you to develop your own software engineering practice by getting into the habit of reflecting on what the **purpose of the software** is and to **articulate** what each component or module is for.

Writing a useful software package that is well-documented and can be reused in the future means that your code could take on a life of its own. The benefits can extend beyond yourself, to your collaborators and other researchers in the future.

High-quality documentation is a key part of ensuring a healthy **software lifecycle**. It can make the different between accidentally creating an abandoned piece of "gradware" (a colloquial term for mysterious code that a former student wrote and nobody else can use) and a successful long-term software project with lasting impact.

## When should I write documentation?

Now! Start writing and sharing documentation for your research code **from the beginning** of your project. It doesn't have to be perfect straight away, but a first draft is more useful than nothing.

The best practice for modern, collaborative research involving digital methods and tools is to document your processes **early and often**. Not only will writing notes about your code help other people to read and use that code, it will clarify your thought process as you design your system, focussing your work on the important parts of the task at hand.

This might include any of the various kinds of software documentation we'll discuss in this module, including:

* design notes and diagrams;
* a step-by-step tutorial for beginners;
* code comments.

It should be a consideration in your _software management plan_, which is a concept discussed in the Module 1a on [Software Lifecycle Planning](https://fair2-for-research-software.github.io/Software_Lifecycle_Planning/). Also, it's never too late to start documenting an old code project.

**Keep in touch** with other developers and users of the research code and make a note of their feedback. Common questions and problems may indicate that there are issues that must be covered more clearly and in greater depth in the software documentation. **Incorporate this feedback** into your software documentation.

## Research software papers

You may decide to publish your code and a description of your **software as a paper** in an academic journal. This is a kind of [methods paper](https://book.the-turing-way.org/communication/dif-articles/methods.html), which provides more detail on your digital research processes than is possible in your main paper. This provides transparency to other researchers and improves the replicability of your results.

A research software paper should provide:

- a concise **introduction** to your code;
- explain the **motivation** for creating the tool;
- describe **how** it was written;
- detail how **algorithms** are implemented;
- **citations** for other software libraries and methods that were used.

It may also contain a detailed description of the technical design.

For more information about writing these papers, which is beyond the scope of this course, please consider starting to explore this subject by reading [Ten simple rules for writing a paper about scientific software](https://doi.org/10.1371/journal.pcbi.1008390) by Joseph Romano.

:::: spoiler

### Software journals

An increasing number of journals allow and encourage the publication of research software and open data. Some journals focus on a specific field, while others primarily publish research software of any kind. Some relevant journals include:

- [*The Journal of Open Source Software*](https://joss.theoj.org/) is a peer-reviewed publications that provides academic citations for research code;
- [*Nature*](https://www.nature.com/) has a category of [Toolbox articles](https://www.nature.com/nature/articles?type=toolbox) that cover the technical side of research;
- [*Journal of Open Research Software*](https://openresearchsoftware.metajnl.com/) is a peer-reviewed repository run by the [Software Sustainability Institute](https://www.software.ac.uk/).

For more information, please read [In which journals should I publish my software?](https://www.software.ac.uk/top-tip/which-journals-should-i-publish-my-software) by Neil Chue Hong, the Director of the [Software Sustainability Institute](https://www.software.ac.uk/).

::::

:::::: keypoints

 - **Reproducibility:** Well-documented software is easier for other researchers to understand and use with confidence. It enables them to **reproduce your results** to replicate research findings, enabling others to validate them and building trust in your research outputs.
 - **Collaboration:** Clear instructions enable other researchers to use and **collaborate** with your software and research projects.
 - **Knowledge transfer:** Your software package will be easier to maintain in the long term if others are able to learn about it and look after it after the original developers move on.

::::::

[roxygen2]: https://roxygen2.r-lib.org/index.html
