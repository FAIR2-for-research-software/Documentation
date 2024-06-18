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

## Contribution guides

Contribution guidelines help users and understand how they can help to improve the software, whether that’s by submitting bug reports, suggesting new features, or writing better code and documentation. All of these aspects are vital to produce reusable research software.

Potential collaborators should be able to easily find out how to take part and contribute. Developers should be encouraged to use appropriate communication channels to ask questions and inform others of proposed software changes. The contact details for the project administrator or committee should be available and they should be welcome and responsive to any queries.

It’s important to explain how the project is managed so the process for evaluating new features and getting them implemented is clear, such as the code review and approval process. For many projects, a ticket system may be used to raise issues and suggest new features. Software developers often propose new code by creating a branch on the version control system (such as Git) and requesting for those changes to be merged into the main codebase.

## Developer notes

System documentation is important for new contributors to familiarise themselves with the codebase and as a reference for existing engineers. There should be a concise description of how the system works from a more technical perspective, with the intended audience being software developers, rather than the research users.

An architecture diagram is an efficient way to provide a “map” to help developers to understand and navigate a complex system.

A coding style guide will help to ensure consistency across all the code written as part of a collaborative project, which helps others to read and interpret the code, making it easier to maintain in the long run. The code style rules should cover things like the way to describe functions, how to indent code, and naming conventions for variables.

This might include guidance and advice, or more strict rules as standards that are checked by a code linter. A code linter is an analysis tool that inspects code and checks for common errors and problems, producing a report for the developer to read and act upon. Common coding style standards include the PEP 8 style guide for the Python programming language and the tidyverse style guide in the R statistical language.

::::::::::::::::::::::::::::::::::::: keypoints 

- **Encourage collaboration:** There are **many ways to contribute** to a research software project, including bug reoprts, feature suggests, design discussions, documentation, and software engineering.
- **Clear processes:** Explain the process for making changes and having them included into the code
- **Bug reports:** Create simple ways for users to report issues and have these problems resolved in a timely manner.
- **Communication:** Create appropriate communication channels so that design discussions and proposed changes may be worked through transparently.

::::::::::::::::::::::::::::::::::::::::::::::::
