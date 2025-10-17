---
title: 'Writing README files'
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions

- How do we **introduce** our software to new researchers and developers?
- How do I structure the basic notes for my research code?
- What are the contents of good documentation?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Explain why and how to write a **README file** for research software
- Learn how to **structure** documentation into sections
- Understand the important components of a good README

::::::::::::::::::::::::::::::::::::::::::::::::

## What is a README file?

A README file is the **first thing a user sees** when they find your software. It should give them an approachable overview of the package, define what’s possible to achieve with this code, and get them started on the right track to use the software effectively for their research.

A README contains a **brief introduction** to the code and shows them how to get started using it. For larger packages, the README forms a concise beginner guide and might link to a more detailed user guide that is located elsewhere.

:::: spoiler

### The etymology of the "Read Me"

The tradition of including a "Read Me" file [originated with](https://medium.com/@NSomar/readme-md-history-and-components-a365aff07f10) computer programming in the 1970s and, particularly with the rise of open source software, has become a *de facto* standard in code documentation.

The term "Read Me" recalls the potion that Alice finds in *Alice in Wonderland* by Lewis Carroll. In Chapter 1, Alice found a bottle labelled "Drink Me" and thinks to herself:

> It was all very well to say “Drink me,” but the wise little Alice was not going to do that in a hurry. “No, I’ll look first,” she said, “and see whether it’s marked ‘poison’ or not”; for she had read several nice little histories about children who had got burnt, and eaten up by wild beasts and other unpleasant things, all because they would not remember the simple rules their friends had taught them: such as, that a red-hot poker will burn you if you hold it too long; and that if you cut your finger very deeply with a knife, it usually bleeds; and she had never forgotten that, if you drink much from a bottle marked “poison,” it is almost certain to disagree with you, sooner or later.

It is wise to follow's Alice's advice and check the "Read Me" before risking being eaten by wild beasts or other hazards of working with poorly documented research software.

::::

The **audience** for a README file is the _end user_, such as a researcher. It's important to consider _the person_ will read your documentation, and to see things from their point of view. It may be someone who is unfamiliar with certain technical terms, or a researcher will less experience of advanced computing. A suitable approach is to imagine writing a manual for a new user who has never seen this software before.

## How to write a README

To start writing a README file, the simplest way is to **create an empty text file** called `README.txt` and start writing. This file should be located in the directory that contains your software project.

::::::::::::::::::::::::::::::::: challenge

Let's create a new code project. Create a new, empty directory to contain your work. Then, start writing your README!

::::::::::::::::: solution

Follow these general steps to create a README file.
The specific details for each operating system are detailed below.

1. Create a directory to contain your project. We call this the _root directory_;
2. In that directory, create a new text file;
3. Name the file `README.txt`;
4. Open the file for editing&mdash;start writing your documentation!

::: group-tab

### Windows

1. Open [File Explorer](https://support.microsoft.com/en-gb/windows/find-and-open-file-explorer-ef370130-1cca-9dc5-e0df-2f7416fe1cb1) to browse the file system;
2. In a folder, right click and select New &rightarrow; Folder;
3. Name the folder `oddsong`;
4. Open that new folder, then right click and select New &rightarrow; Text Document;
5. Name the file `README.txt`;
6. Double-click on the file to open it for editing.

### Linux

Use the [File Manager](https://help.ubuntu.com/stable/ubuntu-help/files-browse.html.en) to create a new directory called `oddsong`. Inside that folder, create a new text file called `README.txt`.

These steps may be achieved using the terminal as follows:

```bash
mkdir oddsong
touch oddsong/README.txt
echo "This is my code" >> my_project/oddsong.txt
nano oddsong/README.txt
```

### MacOS

Use the [Finder](https://support.apple.com/en-gb/guide/mac-help/mchlp2605/mac) file manager to create a new directory called `oddsong`. Inside that folder, create a new text file called `README.txt`.

These steps may be achieved using the terminal as follows:

```bash
mkdir oddsong
touch oddsong/README.txt
echo "This is my code" >> my_project/oddsong.txt
nano oddsong/README.txt
```

:::

::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::

### README contents

The essentials contents of a README document are:

- The **name of the software**. This seems trivial, but a clear title and description of a piece of software will be essential for others to identify your software and differentiate it from others.
- A **brief introduction** to your code, including links to relevant websites.
- **Contact details** for the authors and maintainers.
- A clear statement of who the **target audience** is for the software package.
- **Installation instructions** or a link to further information published elsewhere.
- **Usage instructions**, ideally including a “quick start” guide with a few simple examples to get people up and running with your software package.

It can be useful to **signpost** to related useful methods and software tools by providing links and explaining how other software is related or different to this project when it comes to addressing these kinds of research problems.

You might also describe the contents of your project by giving an overview of the purpose of each file and directory. This is called a **manifest**.

::: callout

## Walk a mile in the user's shoes

Put yourself in the position of a researcher who has encountered your software for the first time.
Imagine that you had to start from square one, how would you like the code to be introduced to you?

:::

::: discussion

Consider your field of research and the technologies you commonly use.

- What things are obvious to you that may not be clear to others?
- What **assumed knowledge** must you explain to new colleagues to get them up to speed?

:::

For research code, it’s often important to **explain the context** in which the software was written and the theory behind it. For example, many researchers write analysis packages or workflows that are based on previously-published research, statistical methods, or theoretical models for which **citations** can be provided. By including references to research papers we better help the users to understand the methods that are implemented by our software, which enables its users to properly cite their sources and increases the users’ confidence that you have applied those methods correctly.

### Installation instructions

Good READMEs provide instructions for getting and setting up your research software. This guidance should be laid out in simple, clear language and organised in a step-by-step manner.

::: discussion

Consider a research project you've worked on.
Discuss the technical prerequisites for that software, tool, or system.
What would someone need to do, when starting from a blank slate, to recreate that environment?

Think about:

- What hardware and software did you need?
- What drivers and libraries were required?
- What software setup, calibration, and configuration is required?

:::

#### Installing prerequisites

Most research code has several **dependencies**, which are other software packages that are required for that tool to work. The user will often need to install the programming language onto their computer, such as R, MATLAB, or Python. It's useful to link to the download pages and provide a link to the package manager tools that are commonly used in those ecosystems. This might also include listing any prerequisites such as hardware or software that must be installed first, such as device drivers.

:::: spoiler

### Software libraries

In software development, a **library** is a collection of resources that can be used to help build a new tool. This might include other people's code that is used to achieve commons tasks, such as displaying output or communicating over the internet.

::::

Consider how the installation method might differ for users of other common **operating systems**, such as Windows, Linux, and Mac OS.

### User guide

All software should include some **short guidance on how to use it** and what the main options and features are. This might be a “quick start” guide with simple examples of common use-cases, or a walkthrough that uses a sample data set.

Explain how the software can be **configured or customised**, including examples of commonly-used options. If the software integrates with other tools or uses specific file formats for its input and output, it’s useful to explain this here too. It’s a good idea to include links to further references if available.

Many users will benefit from a **frequently asked questions** (FAQs) or troubleshooting notes, which describes common error messages, explains why they occur, and suggests ways to resolve them.

::: callout

## Writing style

The writing style should be concise, jargon-free, consistent, and pitched at the appropriate level to the intended target audience.
All technical terms and acronyms should be explained.
However, don’t reinvent the wheel by defining all the terms used, instead link to a reliable external source or journal article.

For more information about the broad topic of improving your writing style, please review these [style guides](https://www.writethedocs.org/guide/writing/style-guides/#traditional-writing-style-guide-resources).

:::

**Diagrams** can be particularly useful to explain complex concepts and workflows. **Screenshots** may also provide a "show and tell" demonstration of how the software will work. Consider recording a screen-cast of someone setting up and using the software. This can be particularly beneficial for visual learners.

::::::::::::::::::::::::::::::::: discussion

Discuss with the group:

- Reflecting on your past experiences, what software or systems have you used that included excellent diagrams and illustrations to help you learn to use them as a new user?
- Have you ever watched a tutorial video online that explained a software tool or process? What did you like and dislike about the walkthrough?

:::::::::::::::::::::::::::::::::

Not all READMEs must follow this structure.
Always adapt the format of your documentation to suit the **specific needs** of your audience.

## Accessibility

Accessibility means **reducing barriers to use** of your research software. There should be no avoidable blockers for participation in the development community for those experiencing a disability or other social factors. When writing documentation for your code, consider how you can adapt your writing style and present information in a way that means that everyone can interact with it by expending the same amount of time and energy, regardless of their relative abilities.

While this is a broad topic, some general tips to consider when authoring software documentation in a research context are:

- **Global audience:** Explain ideas in a way that can be understood by people anywhere in the world, regardless of background. Be sensitive to cultural differences and avoid offensive language;
- **Inclusivity:** Avoid biased language and value diversity e.g. when writing examples;
- **Navigation:** Ensure that the documentation is compatible with assistive technologies like screen readers and keyboard navigation.

:::: spoiler

### More about Accessibility

For more information on this topic, please see the following resources:

- Alistair Duggin, [What we mean when we talk about accessibility](https://accessibility.blog.gov.uk/2016/05/16/what-we-mean-when-we-talk-about-accessibility-2/) defines the core concepts of accessibility.
- Google developer documentation style guide, [Write accessible documentation](https://developers.google.com/style/accessibility) provides helpful examples.
- Write the Docs, [Accessibility guidelines: for writing and beyond](https://www.writethedocs.org/guide/writing/accessibility/) lists many useful materials.

::::

## Text formatting

Using a file format that allows you to format text and create headers makes the content more **comprehensible** for the reader. Organising a document into sections or chapters makes it easier to navigate and find the relevant information.

In the software world, **[Markdown](https://daringfireball.net/projects/markdown/) documents** are a commonly-used file format for writing READMEs.
Markdown is a simple _markup language_ that lets us apply **semantic labelling** such as emphasis and structure to our text. These are displayed using visual styles that make your documentation more aesthetically pleasing and more navigable. It allows you to format your text using symbols to represent headers, bold text, bullet lists, etc. These are displayed to the user using their screen or other device, depending upon accessibility requirements.

:::: spoiler

## What is a markup language?

A [markup language](https://en.wikipedia.org/wiki/Markup_language) is a system of special characters that are used to decorate or format pieces of plain text.
The syntax normally consists of symbols or _tags_ that are used to _encode_ text, that **implies meaning** to make it more information-rich.
It can be used to structure a documented into sections to provide logical organisation so that it's easier to navigate.

Typically, a markup language is edited in a similar way to a computer programming language, and is **rendered** into a document with various rich text formatting such as headers, bold face fonts, etc.

::::

::::::::::::::::::::::::::::::::: challenge

Convert your README file to Markdown format to enable more formatting options.

::::::::::::::::: solution

Follow these steps to rename `README.txt` to `README.md`.

::: group-tab

### Windows

Use [File Explorer](https://support.microsoft.com/en-gb/windows/find-and-open-file-explorer-ef370130-1cca-9dc5-e0df-2f7416fe1cb1) to [rename the file](https://support.microsoft.com/en-gb/office/rename-a-file-baea7aab-760b-4ee0-af58-06e940d505a4) from `README.txt` to `README.md`.

1. Open the `oddsong` directory;
2. Right-click on `README.txt` and select "Rename";
3. Type `README.md`.

### Linux

Use the [File Manager](https://help.ubuntu.com/stable/ubuntu-help/files-browse.html.en) to [rename the file](https://help.ubuntu.com/stable/ubuntu-help/files-rename.html.en) from `README.txt` to `README.md`.

This step may be achieved using the terminal as follows:

```bash
mv README.txt README.md
```

### MacOS

Use the [Finder](https://support.apple.com/en-gb/guide/mac-help/mchlp2605/mac) to [rename the file](https://support.apple.com/en-gb/guide/mac-help/mchlp1144/mac) from `README.txt` to `README.md`.

This step may be achieved using the terminal as follows:

```bash
mv README.txt README.md
```

:::

::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::

An example README file in Markdown format is shown below, in a file called `README.md` where ".md" suffix is the filename extension for Markdown files.

### Section headers

You can separate your document into **hierarchical sections** with headings using the `#` symbol. This makes your README easier to navigate. For example:

```markdown
# Birdsong identification tool

This user guide provides instructions on how to use this birdsong
identifier. The software is designed to assist users in
identifying bird species based on their vocalisations.

# Installation

To install this software, follow the steps below...

# Usage

To use this package, start by configuring...
```

The hash `#` symbol means that line will be converted into a header and displayed to the reader in a large, bold font. This makes it easier for the reader to find the part of your text they're looking for, just like having chapters in a book.

::::::::::::::::::::::::::::::::: challenge

Create suitable headers in your document.

How would you organise your document by dividing up the text into subsections by adding further subheadings?

::::::::::::::::: solution

We can create the commonly-used headers used in READMEs by using the Markdown syntax shown below

```markdown
# Title

Brief introduction to the tool...

# Installation

To get started...

# Usage

To use this tool...
```

This gives some basic structure to the document, which we'll flesh out later.

We can further subdivide the content by using _header levels_, where each subheading uses an additional `#` symbol. For example, `#` is a top-level heading, `##` is a section header, `###` is a subsection header, etc.

```markdown
# Title

Brief introduction to the tool...

# Installation

To get started...

## Prerequisites
...

## Drivers
...

# Usage

To use this tool...

## Quick start
...

## Examples
...
```

These subheadings help the users to navigate the document.

:::::::::::::::::

:::::::::::::::::::::::::::::::::

### Viewing Markdown documents

There are several ways to view the formatted Markdown document, where the syntax is rendered into a rich text document.

* Many code editors have an in-built Markdown viewer;
  * For Notepad++, the Markdown Panel [plugin may be installed](https://npp-user-manual.org/docs/plugins/).
* [Markdown Live Preview](https://markdownlivepreview.com/) is a web-based tool. Input your Markdown syntax in the left panel and the result will be displayed on the right-hand side.
* In [Google Colab](https://colab.research.google.com/), the Text cells use Markdown syntax for formatting.

If your code is published on [GitHub](https://github.com), the home page of your code repository will [display the README file](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes), including a [table of contents](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes#auto-generated-table-of-contents-for-readme-files) that is automatically created to easily select the section of the document to view.

![This repository has a README file with chapters, making navigation easier.](fig/bootstrap-readme-chapters.png){alt="A screenshot of a GitHub repository with a drop-down navigation menu on the readme text box."}

### Text formatting

Here are some commonly-used text formatting options that can be used with Markdown syntax:

| Meaning   | Example      | Syntax              |
| ------- | ---------- | ------------------- |
| Strong text  | **Eastern towhee**     | `**Eastern towhee**`     |
| Emphasised text  | *Pipilo erythrophthalmus*     | `*Pipilo erythrophthalmus*`     |
| Code block  | `name = "Pipilo erythrophthalmus"`      | ``` `name = "Pipilo erythrophthalmus"` ``` |
| Hyperlink   |  [Eastern towhee](https://en.wikipedia.org/wiki/Eastern_towhee) | `[Eastern towhee](https://w.wiki/DHi2)` |

These may be used to add emphasis to parts of the text or highlight key words and phrases.
Using text formatting makes your software documentation easier to **skim-read**, so researchers can quickly find the part of the text that's relevant for what they're working on.

:::::::: challenge

Identify several _key words_ in your README file. Apply the "strong text" syntax so they will be displayed using a bold font face or be given increased stress by a screen-reader.

:::: solution

The Markdown syntax for bold font is to wrap the text in two asterisks `**`.
This may be applied to single words or to phrases.

For example, we can strongly emphasise a single word:

```markdown
Identify a bird based on the **sound** of its call.
```

> Identify a bird based on the **sound** of its call.

Or emphasise a phrase:

```markdown
**Identify a bird** based on the _sound of its call_.
```

> **Identify a bird** based on the *sound of its call*.

::::

::::::::

### Block quotes

We can create a citation with appealing formatting by using the blockquote syntax in Markdown, which is similar to the method used in email.

```markdown
> The eastern towhee (Pipilo erythrophthalmus) is a large New World
> sparrow. The taxonomy of the towhees has been under debate in
> recent decades, and formerly this bird and the spotted towhee
> were considered a single species, the rufous-sided towhee.
```

This will be rendered with the following apperearance:

> The eastern towhee (Pipilo erythrophthalmus) is a large New World sparrow.
> The taxonomy of the towhees has been under debate in recent decades,
> and formerly this bird and the spotted towhee were considered a single species, the rufous-sided towhee.

(This text was retrieved from the *Wikipedia* page on the [Eastern towhee](https://en.wikipedia.org/wiki/Eastern_towhee) bird.)

### Code blocks

If you'd like to present the user with examples of source code, use [code fences](https://www.markdownguide.org/extended-syntax/#fenced-code-blocks) to display the code in a special text box with syntax highlighting. To do this, wrap the code in three backticks `` ` ``. For example:

````markdown
```
genus = "Struthio"
```
````

If you include the name of a programming language then the syntax will be highlighted appropriately, for example:

````markdown
```R
genus <- "Struthio"
```
````

This makes your code examples easier to read.

::: callout

## Markdown

You can learn more about writing documents using Markdown at [Markdown Guide](https://www.markdownguide.org/), a reference for using this syntax.

:::

## Conclusion

Remember, the README file is a **first impression** that research users will receive for your software.
A README contains a brief description of the software, installation instructions, and a usage guide.
Make them informative and user-friendly to enhance the research experience for others and foster collaboration.
The writing style should be concise, clear, and explain technical terms.
Use diagrams and screenshots for clarity.

:::::: keypoints

 - A README file serves as an **introduction** to your software, guiding users on installation, usage, and understanding its capabilities.
 - Consider the user's technical background; write clearly and **avoid jargon**.
 - **Markdown** is a recommended format for creating headers, bold text, bullet points, etc.

::::::

## Further resources

For more information about writing basic software documentation, please review the following materials:

- Raphael Pierzina [Hi, my name is README!](https://www.writethedocs.org/videos/eu/2017/hi-my-name-is-readme-raphael-pierzina/)
- Kira Oakley [The Art of README](https://github.com/hackergrrl/art-of-readme/blob/master/README.md)
- Aleksandra Pawlik [Five top tips on documentation](https://www.software.ac.uk/guide/five-top-tips-documentation)
- Wikipedia [README](https://en.wikipedia.org/wiki/README)
