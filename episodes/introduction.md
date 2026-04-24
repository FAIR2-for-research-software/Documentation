---
title: "Introduction"
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions

- How do we **provide information** to users of our research software?
- Why is documenting code **useful for researchers**?
- **When should we start** writing documentation for our code?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Describe at least three **benefits** of documenting research software
- Explain when in the **project lifecycle** documentation should begin
- Identify the **kinds of documentation** this module will cover

::::::::::::::::::::::::::::::::::::::::::::::::

## What is research software documentation?

There are many kinds of research software, such as:

- Data processing workflows with multiple steps;
- A library of functions used within a research team to perform certain kinds of analysis;
- Tools designed to collect raw data in the field.

Code is rarely self-explanatory. It is a tool we design and extend over time, often alongside colleagues. To explain
our code we must write **software documentation**.

Documentation **provides information** about our programs for everyone involved in their development, use, and future
reuse. It may consist of text, tips within a computer environment, and diagrams that guide the user in using a
(potentially complex) software tool. It explains *how* the software works *and* *why* it behaves the way it does.

## Why document our code?

We often encounter software packages, whether written by ourselves, a colleague, or someone else, that's difficult to
use because it's unclear what it does and how it works. Maybe we try to read the source code itself, but we can't make
head-nor-tail of it. Sometimes it seems like the only person who can use this software is the person who wrote it. Other
times, you wrote the code and forgot what you were thinking when you did!

### Advantages of good documentation

There are many **advantages to writing guidance** to go along with your research software. Software documentation helps
yourself and others to use it successfully in the future. If others can read your code then that ensures that its value
is sustained.

Research outputs often **depend upon the code** used to generate them. Clarity and confidence are essential in using
code to perform calculations, simulations, or data analysis. All kinds of research processes and analysis pipelines can
be made more **reproducible** by providing clear context and instructions for using it.

There are many advantages to making your **code more readable**, too. Well-written software is easier to maintain and
has greater **sustainability**. This means it can continue to be used and modified for a longer period of time, despite
changes in technology. If software is more reusable then it encourages others to use it for their research, increasing
its visibility and **research impact**.

:::: challenge

Think of a time you picked up unfamiliar research code — your own from months ago, or someone else's.

- What made it easy or hard to use?
- What documentation was available, and what was missing?
- If you had written that code, what documentation would have helped future users most?

::::

In the long run, it can also help you to develop your own software engineering practice by getting into the habit of
reflecting on what the **purpose of the software** is and to **articulate** what each component or module is for.

Writing a useful software package that is well-documented and can be reused in the future means that your code could
take on a life of its own. The benefits can extend beyond yourself, to your collaborators and other researchers in the
future.

High-quality documentation is a key part of ensuring a healthy **software lifecycle**. It can make the difference
between accidentally creating an abandoned piece of code (sometimes called *gradware* — code a former student wrote
that nobody else can use) and a successful long-term software project with lasting impact.

## When should I write documentation?

Now! Start writing and sharing documentation for your research code **from the beginning** of your project. It doesn't
have to be perfect straight away, but a first draft is more useful than nothing.

The best practice for modern, collaborative research involving digital methods and tools is to document your processes
**early and often**. Not only will writing notes about your code help other people to read and use that code, it will
clarify your thought process as you design your system, focussing your work on the important parts of the task at hand.

This might include any of the various kinds of software documentation we'll discuss in this module, including:

- design notes and diagrams;
- a step-by-step tutorial for beginners;
- code comments.

It should be a consideration in your *software management plan*, which is a concept discussed in the Module 1a on
[Software Lifecycle Planning](https://fair2-for-research-software.github.io/Software_Lifecycle_Planning/). Also, it's
never too late to start documenting an old code project.

**Keep in touch** with other developers and users of the research code and make a note of their feedback. Common
questions and problems may indicate that there are issues that must be covered more clearly and in greater depth in the
software documentation. **Incorporate this feedback** into your software documentation.

## Research software papers

Some researchers choose to publish a description of their code as a **software paper** in an academic journal — a kind
of [methods paper](https://book.the-turing-way.org/communication/dif-articles/methods.html) that improves the
transparency and replicability of computational results.

This is beyond the scope of this module. The FAIR² programme covers it separately in the **Publishing software papers**
module — see the [FAIR² course page](https://rse.shef.ac.uk/training/fair4rs/) for details and registration.

:::::: keypoints

- **Reproducibility:** Well-documented software is easier for other researchers to understand and use with
  confidence. It enables them to **reproduce your results** to replicate research findings, enabling others to validate
  them and building trust in your research outputs.
- **Collaboration:** Clear instructions enable other researchers to use and **collaborate** with your software and
  research projects.
- **Knowledge transfer:** Your software package will be easier to maintain in the long term if others are able to learn
  about it and look after it after the original developers move on.
- **Sustainability:** Readable, documented code is easier to maintain and reuse, extending the useful life of your
  software.

::::::
