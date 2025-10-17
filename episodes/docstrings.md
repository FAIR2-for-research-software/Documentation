---
title: 'Documentation strings'
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions

- How do we **describe our code**?
- How can we **annotate functions** in our research code?
- Why are documentation strings useful for **research software**?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Understand the **purpose** of documentation strings
- Learn **how to write** documentation strings that will be useful for other researchers
- Introduce ways to describe the **parameters** and **return values** of functions

::::::::::::::::::::::::::::::::::::::::::::::::

## How do we describe our code?

### Describing functions

If you’re publishing a research software package, one of the most common ways that its users will learn to interact with the code is by reading the documentation **for each individual function**. We learned about _functions_ in an earlier [module on software design principles](https://fair2-for-research-software.github.io/FAIR_Code_design/). Functions help us to break our code into smaller units that have a single purpose.

By documenting those functions effectively, we aim to **explain their purpose** to future users and maintainers of that code. We also need to describe all the expected inputs and outputs of the functions.

## Documentation strings

We describe functions by using a feature of many programming languages called **documentation strings**, which is sometimes abbreviated to "docstring". A documentation string is a piece of text that describes a part of your code and helps other people to use it effectively.

To make a docstring, we write special comments in our code using syntax which is specific to each programming language, although the principle is the same.

::: group-tab

### Python

In Python, we put a string as the first line of a function (or other object.) For example, for a simple Python function that calculates the sum of two numbers:

```python
def add(x, y):
    """
    Calculate the sum of two numbers.
    """
    return x + y
```

### R

In R, we use the [roxygen2](https://roxygen2.r-lib.org/) package, where a comment with a single quote `#'` specifies a documentation string for a function.

```R
#' Calculate the sum of two numbers.
add <- function(x, y) {
  return(x + y)
}
```

:::

Whenever you add functionality to a code project, consider wrapping it up into a function.
It may help to **write the docstring first** to help work through what the purpose of your new code is before you start!

::::::::::::::::::::::::::::::::: challenge

Write a documentation string for a function.
Create a script called `oddsong` and define a function named `identify()` that will be used to identify bird songs by inspecting an audio file to provide the name of that species.

::::::::::::::::: solution

::: group-tab

### Python

1. Create a new Python script by creating a file called `oddsong.py`
2. Open the file for editing
3. Create a new function called `identify()`
4. Write a string that describes the code

```python
def identify(audio_file):
    """
    Identify a bird based on the sound of its call.
    """

    print("Identifying bird vocalisation...")

    return "Hirundo atrocaerulea"
```

### R

1. Create a new R script by creating a file called `R/identify.R`
2. Open the file for editing
3. Create a new function called `identify()`
4. Write a string that describes the code

```R
#' Identify a bird based on the sound of its call.
identify <- function(audio_file) {

    print("Identifying bird vocalisation...")

    return("Hirundo atrocaerulea")
}
```

See also the [example R script](https://github.com/Joe-Heffer-Shef/oddsong/blob/main/R/identify.R).

:::

::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::

### Viewing docstrings

We can view documentation strings for a function by using the `?` operator or `help()` function in R and the  [`help` built-in function](https://docs.python.org/3/library/functions.html#help) in Python.

::: group-tab

### Python

The contents of that string will be displayed to users in their development environment or by running the `help` function like so:

```python
help(sum)
```

```
Help on built-in function sum in module builtins:

sum(iterable, /, start=0)
    Return the sum of a 'start' value (default: 0) plus an iterable of numbers

    When the iterable is empty, return the start value.
    This function is intended specifically for use with numeric values and may
    reject non-numeric types.
```

For more help with specific Python functions, check the documentation for the [Python Standard library](https://docs.python.org/3/library/) or for the particular package you're using.

### R

In R, we use the `help()` function to display the user manual for a function. For example, to view the documentation for the [in-built `sum()` function](https://www.rdocumentation.org/packages/base/versions/3.6.2/topics/sum), we would call:

```R
help(sum)
```

```
sum                    package:base                    R Documentation

Sum of Vector Elements

Description:

     ‘sum’ returns the sum of all the values present in its arguments.

Usage:

     sum(..., na.rm = FALSE)

Arguments:

     ...: numeric or complex or logical vectors.

   na.rm: logical.  Should missing values (including ‘NaN’) be removed?

Details:

     This is a generic function: methods can be defined for it directly
...
```

If the content is too big to fit on the screen then you'll need to press the space bar to proceed through the pages of text.

For more information, see [Getting Help with R](https://www.r-project.org/help.html) in the R documentation.

:::

::::::::::::::::::::::::::::::::: challenge

Use the `help()` function to view the documentation string for a function.

::::::::::::::::: solution

Let's view the help text for an in-built [function `abs()`](https://docs.python.org/3/library/functions.html#abs) that finds the absolute value of a number.

::: group-tab

### Python

```python
help(abs)
```

The following text will be printed to the screen

```output
Help on built-in function abs in module builtins:

abs(x, /)
    Return the absolute value of the argument.
```

### R

```R
help(abs)
```

The following text will be printed to the screen

```output
abs                    package:base                    R Documentation

Miscellaneous Mathematical Functions

Description:

     ‘abs(x)’ computes the absolute value of x, ‘sqrt(x)’ computes the
     (principal) square root of x, sqrt{x}.

     The naming follows the standard for computer languages such as C
     or Fortran.

Usage:

     abs(x)
     sqrt(x)

Arguments:

       x: a numeric or ‘complex’ vector or array.

Details:

     These are internal generic primitive functions: methods can be
     defined for them individually or via the ‘Math’ group generic.
     For complex arguments (and the default method), ‘z’, ‘abs(z) ==
     Mod(z)’ and ‘sqrt(z) == z^0.5’.

     ‘abs(x)’ returns an ‘integer’ vector when ‘x’ is ‘integer’ or
...
```

If the content is too big to fit on the screen then you'll need to press the space bar to proceed through the pages of text.

:::

::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::

The most important thing to include in a docstring is an explanation of the **purpose** of this piece of code.
To write a useful docstring, put yourself in the shoes of someone who encounters your code for the first time. They need a simple introduction that doesn’t assume too much implied knowledge. The explanation may seem obvious to you, but it may help a new user greatly.

::: discussion

How can we **tailor** our documentation strings to **different audiences**, such as new users and experienced developers?

:::

### Arguments

Next, we must describe the inputs to the function, its _arguments_ or ***parameters***.

We list the input parameters in the code examples below.
Each argument has a name and a brief description.

::: group-tab

### Python

The argument name matches the variable name in the function signature, such as `add(x, y)` in this case.

```python
def add(x, y):
    """
    Calculate the sum of two numbers.

    Args:
        x: The first number to add.
        y: The second number to add.
    """
    return x + y
```

### R

The argument name matches the variable name in the function signature, such as `function(x, y)` in this case.

```R
#' Calculate the sum of two numbers.
#'
#' @param x The first number to add.
#' @param y The second number to add.
add <- function(x, y) {
  return(x + y)
}
```

:::

We have added an “arguments” (abbreviated to “args”) section to our docstring which lists the input parameters of the function and describes each one.

::::::::::::::::::::::::::::::::: challenge

Add a description of each argument to a function in your code.

Run `help()` and evaluate the output.

:::: solution

::: group-tab

### Python

```python
def identify(audio_file: str) -> str:
    """
    Identify a bird based on the sound of its call.

    Args:
        audio_file: The path of an audio file.
    """
    print("Identifying bird vocalisation...")
    return "Hirundo atrocaerulea"
```

### R

```R
#' Identify a bird based on the sound of its call.
#'
#' @param audio_file The path of the sound file
identify <- function(audio_file) {
    print("Identifying bird vocalisation...")
    return("Hirundo atrocaerulea")
}
```

:::

::::

:::::::::::::::::::::::::::::::::

### Return values

Finally, we describe the output of the function. The **return value** is defined by the `return` statement in our function code block.

::: group-tab

### Python

In the Python programming language, we conventionally use the "Returns:" section to describe the function output.

```python
def add(x, y):
    """
    Calculate the sum of two numbers.

    Args:
        x: The first number to add.
        y: The second number to add.

    Returns:
        The sum of x and y.
    """
    return x + y
```

### R

In R, when using [roxygen2](https://roxygen2.r-lib.org/), the "@return" section describes the function output.

```R
#' Calculate the sum of two numbers.
#'
#' @param x The first number to add.
#' @param y The second number to add.
#' @return The sum of x and y.
add <- function(x, y) {
  return(x + y)
}
```

:::

This will help the user to understand what the function does and what they can expect to receive back when they call it.

It can also be useful to explain any potential errors or exceptions that the function will raise if the inputs aren’t as expected, and how to deal with them.

::::::::::::::::::::::::::::::::: challenge

Describe the return value of a function in a documentation string.

Run `help()` and evaluate the output.

:::: solution

::: group-tab

### Python

```python
def identify(audio_file: str) -> str:
    """
    Identify a bird based on the sound of its call.

    Args:
        audio_file: The path of an audio file.

    Returns:
        The name of the bird species.
    """
    print("Identifying bird vocalisation...")
    return "Hirundo atrocaerulea"
```

### R

```R
#' Identify a bird based on the sound of its call.
#'
#' @param audio_file The path of the sound file
#' @returns The name of the bird species.
identify <- function(audio_file) {

    print("Identifying bird vocalisation...")

    return("Hirundo atrocaerulea")
}
```

:::

::::

:::::::::::::::::::::::::::::::::

### Usage examples

We can also include demonstrations of how to use our code by providing code snippets. To do this, we write a collection of sample code that demonstrate how to use functions effectively in different scenarios.

To do this, let's add an **examples section** to our documentation string.

::: group-tab

### Python

Each code example has a prefix of `>>>` which represents the input prompt on the Python interpreter. Some code editors will provide syntax highlighting of these code snippets.

```python
def add(x, y):
    """
    Calculate the sum of two numbers.

    Args:
        x: The first number to add.
        y: The second number to add.

    Returns:
        The sum of x and y.

    Examples:
    >>> add(1, 1)
    2
    >>> add(1.3, 5.3)
    6.6
    """
    return x + y
```

For more information about including code examples and test cases in docstrings, please read about the [doctest](https://docs.python.org/3/library/doctest.html) module  in the Python documentation.

### R

The code examples section of the docstring is prefixed by `@examples`.

```R
#' Add two numbers.
#'
#' @param x The first number to add.
#' @param y The second number to add.
#' @return The sum of `x` and `y`.
#'
#' @examples
#' add(1, 1)
#' add(1.3, 5.3)
add <- function(x, y) {
  return(x + y)
}
```

For more information about writing R code examples within function documentation, please see the [Examples](https://r-pkgs.org/man.html#sec-man-examples) section in the book _R Packages_ by Hadley Wickham.

:::

::::::::::::::::::::::::::::::::: challenge

Write a brief code example within the documentation string in a function in your code.

:::: solution

::: group-tab

### Python

```python
def identify(audio_file: str) -> str:
    """
    Identify a bird based on the sound of its call.

	Examples:
	>>> identify("~/recordings/hirundo.wav")
	"Hirundo atrocaerulea"
    """
    print("Identifying bird vocalisation...")
    return "Hirundo atrocaerulea"
```

### R

```R
#' Identify a bird based on the sound of its call.
#'
#' @examples
#' identify("~/recordings/hirundo.wav")
identify <- function(audio_file) {

    print("Identifying bird vocalisation...")

    return("Hirundo atrocaerulea")
}
```

:::

::::

:::::::::::::::::::::::::::::::::

:::: spoiler

### Using docstrings to create automatic tests

We can use the code examples inside docstrings to define test cases that are used in automatic software testing.

::: group-tab

### Python

These code examples can be used as automatic tests using the [doctest](https://docs.python.org/3/library/doctest.html) module which is built into Python.

### R

In the R ecosystem, we can automatically test the examples in our documentation strings using the [doctest](https://cran.r-project.org/web/packages/doctest/vignettes/doctest.html) package.

:::

::::

## Best practices

This section contains some **tips** for writing useful documentation strings.

### Prioritisation

Focus on the **purpose and functionality** of the code, rather than getting bogged down in the details of how it works. Explain what the function **does**, rather then the specific implementation, because this might change over time. A function encapsulates an isolated part of a system, which can be used as a black box by other parts of the system or the end user, who in many cases only needs to understand its inputs and outputs.

Tips:

- It's a good idea to start your docstring with a **high-level summary** of the function.
- If the function is a major one, include a **simple introduction** for the new user.

::: discussion

Consider this documentation string:

```python
def identify(audio_file):
    """
    Process sound recording.
    """
    ...
```

What problems do you notice? How could we improve this?

:::

### Clarity is key

Be **concise**. Describe the essential information that user needs to know first and be brief but clear.

As with any software documentation, **avoid jargon** where possible.

::: discussion

Read the following documentation string, which is very wordy:

```python
def add(x, y):
    """
    Adds two numbers together, which are the x and y arguments of this function.

    This function takes two numbers as input and returns their sum.
    The addition is performed using the built-in `+` operator.

    Args:
        x: The first number to add to the second number, y.
        y: The second number to add to the first number, x.

    Returns:
        The sum of x and y, which are summed using the addition operator.
    """
    return x + y
```

**Discuss** how can we effectively convey the purpose and functionality of a function in a docstring, without going into excessive detail about its implementation?

:::

Don't reinvent the wheel. **Provide links** to further resources for users to take a deep dive into more complicated topics.

::: discussion

How can we link to external resources that can provide more in-depth information?

:::

Be **consistent**. Decide a style of docstring and use that everywhere across your software project. If you're working on a larger project with multiple developers, refer to the coding conventions and, if in doubt, follow the style of existing code.

:::: spoiler

### Docstring conventions

There are several different **standards** for documentation strings. A standard is a convention that determines how the docstrings will be organised and the syntax that is used to represent the arguments, data types, etc.

A list of documentation string standards in Python:

 - The [PEP 257](https://peps.python.org/pep-0257/) docstring standard was designed by the maintainers of the Python
   programming language.
 - The [Google Style Guide](https://google.github.io/styleguide/pyguide.html#381-docstrings) sets out a docstring format.
 - [Sphinx docstring format](https://www.sphinx-doc.org/en/master/), which has a [NumpyDoc extension](https://numpydoc.readthedocs.io/en/latest/format.html) designed for scientific use.

It doesn't matter which one you select, as long as it's used consistently across a project and it's clear what the syntax means. Some standards are better-supported by other tools such as <abbr title="Integrated development environments">IDEs</abbr> and documentation generators.

::::

## Automatically generate docstrings

Generative large language model (LLM) services such as [Google Gemini](https://gemini.google.com/) can read your code and write docstrings automatically, to a certain extent.

To do this, ask the system to create a docstring and copy your code into the prompt text box.
Below is an example prompt and the reply generated by the Google Gemini algorithm:

```
Please generate a docstring for this Python function:

def calculate_rectangle_area(width, height):
    area = width * height
    return area
```

The result is the following docstring, in addition to some helpful descriptions of the content that it generated.

```python
def calculate_rectangle_area(width, height):
  """
  This function calculates the area of a rectangle.

  Args:
      width (float): The width of the rectangle. Must be a positive number.
      height (float): The height of the rectangle. Must be a positive number.

  Returns:
      float: The area of the rectangle. This will be a positive number.
  """

  # Calculate the area
  area = width * height

  return area
```

This <abbr title="artificial intelligence">AI</abbr>-generated content contains a function summary, argument descriptions, and explains the return value as we discussed previously.

::::::::::::::::::::::::::::::::::::: challenge

Try asking a generative artificial intelligence service such as [Google Gemini](https://gemini.google.com/) to read your code.

- Ask it to generate documentation of different kinds.
- Request a review of your code. What does the bot think?
- Can the chatbot create a diagram to illustrate a concept that is relevant to your research software?

:::::::::::::::::::::::::::::::::::::

This can save you a lot of time, but as with any <abbr title="Large language model">LLM</abbr>-generated content, **always check the output** and ensure it's correct!

::::::::::::::::::::::::::::::::::::: discussion

What are the benefits and risks of using a Large Language Model (LLM) service such as Google Gemini or OpenAI ChatGPT to interpret your code and produce content that you use in your research?

How should we critically evaluate this material so that it can be used appropriately to improve the productivity of our research teams without jeopardising our ethics or integrity or causing security risks?

:::::::::::::::::::::::::::::::::::::

## Conclusion

Documentation strings make your code **clearer to read** and easier for other researchers to use.
Also, they make your research software **easier to maintain** in the long run, saving time and resources.
Good docstrings use a clear writing style and **everyday language**.

Well-documented, **reusable research code** depends upon good documentation strings.
Research collaborators will benefit from **clear explanations** of the purpose of each function.

::::::::::::::::::::::::::::::::::::: keypoints

- Docstrings are special comments that describe the **purpose of a function** and its inputs and outputs.
- **Structure your docstrings** to convey more information, with a concise introduction.
- Documentation strings allow you to break your documentation into **bite-size chunks**, with one overview comment per function.

::::::::::::::::::::::::::::::::::::::::::::::::

## Further resources

To find out more about documentation strings, please refer to the following resources:

Python

- Python [PEP 8 Documentation Strings](https://peps.python.org/pep-0008/#documentation-strings)
- [NumPy style guide](https://numpydoc.readthedocs.io/en/latest/format.html) describes the syntax and best practices for docstrings in the NumPy project.

R

* [Function documentation](https://r-pkgs.org/man.html) in *R Packages* by Hadley Wickham
