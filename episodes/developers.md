---
title: 'Developer guidance'
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 

- How do I introduce **new contributors** to my research software project?
- What is the best way to **communicate processes** such as bug reporting?
- Where should I write up the **design and structure** of the system?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Learn to write a **contribution guide** for research code
- Learn about software **coding standards** 
- Implement ways to **facilitate communication** between researchers that are engaged in the project
- Provide a high-level **understanding of an existing codebase**

::::::::::::::::::::::::::::::::::::::::::::::::

## Introduction

Most research software is written in a collaborative manner, involving multiple specialists from within a team or from multiple institutions. For the long-term health of a software package, it’s important to encourage potential contributors to get in touch and feel welcome to take part. Useful research software can take on a life of its own. For more information on planning the development of research software and project governance, see Module 1a.

It’s often published using an open source licence, which means that all the code is publicly available and may be used and modified by anyone, within certain conditions (see module 1b to learn more about software licensing.)

There's a lot more creating and managing a sustainable community aorund a research software project, but having a central piece of documentation for contributors is a great start!

## Contribution guides

Contribution guidelines help users and understand how they can help to improve the software, whether that’s by submitting bug reports, suggesting new features, or writing better code and documentation. All of these aspects are vital to produce reusable research software.

Potential collaborators should be able to easily find out how to take part and contribute. Developers should be encouraged to use appropriate communication channels to ask questions and inform others of proposed software changes. The contact details for the project administrator or committee should be available and they should be welcome and responsive to any queries.

It’s important to explain how the project is managed so the process for evaluating new features and getting them implemented is clear, such as the code review and approval process. For many projects, a ticket system may be used to raise issues and suggest new features. Software developers often propose new code by creating a branch on the version control system (such as Git) and requesting for those changes to be merged into the main codebase.

Contribution guides will save you time in the long run, because it provides an on-ramp for people to get involved, prevents them from getting confused, and reduces the amount of incorrectly-submitted bug reports or requests for change, etc.

### How to write contributor guidance

The stanard practice for authoring a contribution guide for a software project is to create a file called `CONTRIBUTING.md` in the root folder of your project. This is a Markdown file that introduces new people to the project. It lets people know the ways they can take part in the research software project and what to do to get involved.

The specific contents of this file depend upon the kind of research project, but some useful information to provide typically includes:

- An introduction to the organisation and structure of the code, possibly including diagrams.
- Instructions to raising issues, suggesting new features, and proposing code changes.
- Links to additional documentation that's hosted elsewhere, such as a code of conduct or discussion forum.
- A walkthrough to setting up a development environment, such as guidance on installing developer tools or other prerequisites.

On code hosting platforms such as GitHub, the contribution guide will be created automatically using this `CONTRIBUTING.md` Markdown file.

:::: challenge

TODO 

Create a new file called `CONTRIBUTING.md` and populate it with a few sentences.

::::

## Developer notes

System documentation is important for new contributors to familiarise themselves with the codebase and as a reference for existing engineers. There should be a concise description of how the system works from a more technical perspective, with the intended audience being software developers, rather than the research users.

An architecture diagram is an efficient way to provide a “map” to help developers to understand and navigate a complex system.

A coding style guide will help to ensure consistency across all the code written as part of a collaborative project, which helps others to read and interpret the code, making it easier to maintain in the long run. The code style rules should cover things like the way to describe functions, how to indent code, and naming conventions for variables.

This might include guidance and advice, or more strict rules as standards that are checked by a code linter. A code linter is an analysis tool that inspects code and checks for common errors and problems, producing a report for the developer to read and act upon. Common coding style standards include the PEP 8 style guide for the Python programming language and the tidyverse style guide in the R statistical language.

## Further resources

To find out more about creating healthy communities of developers to collaborate on research software engineering projects, please visit the following resources:

- GitHub Docs [Setting guidelines for repository contributors](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/setting-guidelines-for-repository-contributors)
- H. Gruson and H. Turner Software Sustainability Institute [Opening the door to new contributors in open source projects](https://www.software.ac.uk/blog/opening-door-new-contributors-open-source-projects)

::::::::::::::::::::::::::::::::::::: keypoints 

- **Encourage collaboration:** There are **many ways to contribute** to a research software project, including bug reoprts, feature suggests, design discussions, documentation, and software engineering.
- **Clear processes:** Explain the process for making changes and having them included into the code
- **Bug reports:** Create simple ways for users to report issues and have these problems resolved in a timely manner.
- **Communication:** Create appropriate communication channels so that design discussions and proposed changes may be worked through transparently.

::::::::::::::::::::::::::::::::::::::::::::::::
