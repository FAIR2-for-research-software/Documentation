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

Research software comes in many forms, such as:

- data processing workflows with multiple steps;
- a library of functions used within a research team for a particular kind of analysis;
- tools designed to collect raw data in the field.

Code is rarely self-explanatory. It is a tool we design and extend over time, often alongside colleagues. To explain
how our code works we write **software documentation**.

Documentation **provides information** about our programs for everyone involved in their development, use, and future
reuse. It can take the form of written text, tips embedded in a computer environment, or diagrams that guide the user
through a (potentially complex) software tool. Good documentation explains both *how* the software works and *why* it
behaves the way it does.

## Why document our code?

We have all encountered software — whether written by ourselves, a colleague, or a stranger — that is hard to use
because it is unclear what it does or how it works. Reading the source code may not help; sometimes it seems that only
the original author can use it. And sometimes that author is you, six months ago, with no memory of what you were
thinking at the time.

### Advantages of good documentation

There are many **advantages to writing guidance** alongside your research software. Documentation helps you and others
to use the code successfully in the future, and it ensures that the value of your work is sustained.

Research outputs often **depend upon the code** used to generate them, so clarity and confidence are essential when
that code performs calculations, simulations, or data analysis. Clear context and instructions make research processes
and analysis pipelines more **reproducible**.

There are also benefits to making your **code more readable**. Well-written software is easier to maintain and has
greater **sustainability**, meaning it can continue to be used and modified for longer despite changes in technology.
Reusable software encourages others to apply it to their own research, increasing its visibility and **research
impact**.

:::: challenge

Think of a time you picked up unfamiliar research code — your own from months ago, or someone else's.

- What made it easy or hard to use?
- What documentation was available, and what was missing?
- If you had written that code, what documentation would have helped future users most?

::::

In the long run, writing documentation also helps you to develop your own software engineering practice. It builds the
habit of reflecting on the **purpose of the software** and **articulating** what each component or module is for.

A well-documented, reusable software package can take on a life of its own, with benefits extending beyond yourself to
your collaborators and other researchers in the future.

High-quality documentation is a key part of a healthy **software lifecycle**. It can make the difference between an
abandoned piece of code (sometimes called *gradware*, code a former student wrote that nobody else can use) and a
successful long-term software project with lasting impact.

## When should I write documentation?

Now! Start writing and sharing documentation for your research code **from the beginning** of your project. A first
draft does not need to be perfect: anything is more useful than nothing.

The best practice for modern, collaborative research is to document your processes **early and often**. Notes about
your code help other people read and use it, and they clarify your own thinking as you design the system, focussing
your work on the important parts of the task at hand.

This might include any of the kinds of software documentation we will discuss in this module, such as:

- design notes and diagrams;
- a step-by-step tutorial for beginners;
- code comments.

Documentation should also be a consideration in your *software management plan*, a concept covered in Module 1a on
[Software Lifecycle Planning](https://fair2-for-research-software.github.io/Software_Lifecycle_Planning/). And it is
never too late to start documenting an older code project.

**Keep in touch** with other developers and users of the research code, and note their feedback. Recurring questions
and problems often signal areas that need to be covered more clearly or in greater depth. **Incorporate this feedback**
into your documentation as the project evolves.

## Research software papers

Some researchers choose to publish a description of their code as a **software paper** in an academic journal, a kind
of [methods paper](https://book.the-turing-way.org/communication/dif-articles/methods.html) that improves the
transparency and replicability of computational results.

This is beyond the scope of this module. The FAIR² programme covers it separately in the **Publishing software papers**
module. See the [FAIR² course page](https://rse.shef.ac.uk/training/fair4rs/) for details and registration.

:::::: keypoints

- **Reproducibility:** Well-documented software is easier for other researchers to understand and use with confidence,
  enabling them to **reproduce your results**, validate findings, and build trust in your research outputs.
- **Collaboration:** Clear instructions enable other researchers to use and **collaborate** with your software and
  research projects.
- **Knowledge transfer:** Your software will be easier to maintain in the long term if others can learn about it and
  take it on after the original developers move on.
- **Sustainability:** Readable, documented code is easier to maintain and reuse, extending the useful life of your
  software.

::::::
