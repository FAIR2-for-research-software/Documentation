---
title: 'Documentation strings'
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 

- What is a documentation string?
- Why are documentation strings useful for research software?
- How do we write documentation strings?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Understand the purpose of documentation strings
- Learn to write documentation strings that will be useful for other researchers
- Introduce ways to describe the parameters and return values of functions

::::::::::::::::::::::::::::::::::::::::::::::::

## Introduction

If you’re publishing a research software package, one of the most common ways that its users will learn to interact with the code is by reading the documentation for each individual function.

We learned about functions in an earlier module. Functions help us to break our code into smaller units that have a single purpose. By documenting those functions effectively, we aim to explain that purpose to future users and maintainers of that code. We also need to describe all the expected inputs and outputs of the function.

We describe functions by using a feature of many programming languages called documentation strings, usually abbreviated to **docstring**. A documentation string is a piece of text that describes that piece of code and helps people to use it.

To make a docstring, we put a string as the first line of a function (or other object.) For example, for a simple Python function that calculates the sum of two numbers:

TODO R examples

```python
def add(x, y):
    """
    Calculate the sum of two numbers.
    """
    return x + y
```

::::::::::::::::::::::::::::::::: challenge

Write a documentation string for a function.

::::::::::::::::: solution

TODO

::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::

In this code, the function uses the normal Python syntax, except a string has been included below the function definition. The contents of that string will be displayed to users in their development environment or by running the help function like so:

```output
>>> help(add)
Help on function add in module __main__:

add(x, y)
    Calculate the sum of two numbers.
```

::::::::::::::::::::::::::::::::: challenge

Use the `help()` function to view the documentation string for a function.

::::::::::::::::: solution

TODO

::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::

The most important thing to include in a docstrings is an explanation of the purpose of this piece of code. To write a useful docstring, put yourself in the shoes of someone who encounters your code for the first time and needs a simple introduction that doesn’t assume any implied knowledge. The explanation will be very basic and seem obvious to you, but it may help a new user greatly.

Next, we must describe the inputs and outputs of the function.

We list all the input parameters, or arguments, like so:

```python
def add(x, y):
    """
    Calculate the sum of two numbers.

    Args:
        x: The first number to add. (float or int)
        y: The second number to add. (float or int)
    """
    return x + y
```

We have added an “arguments” (abbreviated to “args”) section to our docstring which lists the input parameters of the function and describes each one.

Finally, we describe the result of the function that is output by the return statement.

```python
def add(x, y):
    """
    Calculate the sum of two numbers.

    Args:
        x: The first number to add. (float or int)
        y: The second number to add. (float or int)

    Returns:
        The sum of x and y. (float or int)
    """
    return x + y
```

This will help the user to understand what the function does and what they can expect to receive back when they call it. It can also be useful to explain any potential errors or exceptions that the function will raise if the inputs aren’t as expected, and how to deal with them.

Help function in R and Python e.g.

```python
help(print)
```

TODO Usage examples for functions.

Code snippets: comprehensive collections of code examples that demonstrate how to use functions effectively in different scenarios.

## Best practices

Focus on the **purpose and functionality** of the code, rather than getting bogged down in the details of how it works. Explain what the function **does**, rather then the specific implementation, because this might change over time. A function encapsulates an isolated part of a system, which can be used as a black box by other parts of the system or the end user, who in many cases only needs to understand its inputs and outputs. It's a good idea to start your docstring with a high-level summary of the function and, if the function is a major one, an introduction for the new user.

Clarity is key. Be **concise**. Describe the essential information that user needs to know first and be brief but clear. As with any software documentation, **avoid jargon** where possible, and provide links to further resources for users to take a deep dive into more complicated topics.

Be **consistent**. Decide a style of docstring and use that everywhere across your software project. If you're working on a larger project with multiple developers, refer to the coding conventions and, if in doubt, follow the style of existing code.


## Automatically generate docstrings

Generative AI services such as Google Gemini can write docstrings automatically.

To do this, ask the system to create a docstring and copy your code into the prompt text box. Below is an example prompt and the reply generated by the Google Gemini algorithm:

```
Please generate a docstring for this Python function:

def calculate_rectangle_area(width, height):
    area = width * height
    return area
```

The result is the follow docstring, in addition to some helpful descriptions of the content that it generated.

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

This can save you a lot of time, but as with any AI-generated content, always check the output and ensure it's correct!

## Conclusion

Docstrings are special comments that describe the purpose of a function and its inputs and outputs, making your code clearer, easier for other researchers to use, and more maintainable in the long run.

## Further reading

To find out more about documentation strings, please refer to the following resources:

- Python [PEP 8 Documentation Strings](https://peps.python.org/pep-0008/#documentation-strings)
- [Numpy style guide](https://numpydoc.readthedocs.io/en/latest/format.html) describes the syntax and best practices for docstrings in the Numpy project.

::::::::::::::::::::::::::::::::::::: keypoints 

- Well-documented, reusable research code depends upon good documentation strings
- Research collaborators will benefit from clear explanataions of the purpose of each function
- Structure your docstrings to convey more information, with a concise introduction
- Good docstrings are clear and use everyday language

::::::::::::::::::::::::::::::::::::::::::::::::
