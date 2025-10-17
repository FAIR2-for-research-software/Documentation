---
title: "Documentation examples"
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions

- What does well-documented code look like?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Be introduced to good software documentation practices

::::::::::::::::::::::::::::::::::::::::::::::::

## Code examples

In this episode we'll review some examples of research software and evaluate how readable and reusable it is.

Here is some code to perform a geometrical calculation. The first example could be improved in terms of its documentation and readability, while the second one is much clearer.

### Example of no documentation

Here's an example of some code that does... something. It's not clear what this code is for or why it was written.

::: group-tab

### Python

This is some research code that is contained in a Python function.

```python
def run(x):
  weird_num = 1.234
  return x * weird_num - ang**3 / (weird_num * 2)
```

### R

This is some research code that is contained in an R function.

```R
run <- function(x) {
  weird_num = 1.234
  return x * weird_num - ang**3 / (weird_num * 2)
}
```

:::

:::: challenge

Read and evaluate this code.

- What is the purpose of this function?
- What do the variables mean?
- Would you rely on this code in your research? Why, or why not?

::::

This is a function with a name that doesn't explain what the code will do. There are no comments or notes to explain what the author intended to achieve. The variable names don't clarify anything either: what does `x` mean in this context? Where would I go to find out more about `weird_num`? This is effectively a "magic" number that is arbitrarily stated but unexplained.

The logic of the calculation is also... rather cryptic.

Maybe the code works, maybe it doesn't; but it could be made clearer and easier to maintain and modify in the future.

### Well-documented example

Now let's look at an example of best practices in documenting research software. (These code snippets are part of the end-product of this course, so don't worry if they don't make sense yet!)

::: group-tab

### Python

This is a function written in the Python programming language that calculates a mathematical result, the details of which aren't relevant. This code has plenty of documentation to help us read and understand it.

```python
import math

def calculate_sine(angle: float) -> float:
  """
  Calculates the sine of an angle using the first four terms
  of the Taylor series.

  This function uses the first four terms of the Taylor
  series for sine to approximate the value. This is a
  simple and efficient method for most applications.

  Args:
      angle (float): The angle in radians.

  Returns:
      float: The sine of the angle (sin(angle)).
  """
  sine_value = angle

  # Iterate over the first four terms of the Taylor series for sine
  for i in range(1, 5):
    factorial = math.factorial(2 * i)
    sign = (-1) ** (i // 2)  # Alternate signs for sine terms

    # Add terms for sine
    sine_value += sign * (angle ** (2 * i)) / factorial

  return sine_value
```

### R

This is a function written in the R programming language that calculates a mathematical result, the details of which
aren't relevant. This code has plenty of documentation to help us read and understand it. R uses the
[roxygen2][roxygen2] package to format documentation strings into our project documentation.

```R
#' Calculate the sine of an angle
#'
#' @description
#'
#' This function uses the first four terms of the Taylor
#' series for sine to approximate
#' the value. This is a simple and efficient method for
#' most applications.
#'
#' @param angle The angle in radians.
#'
#' @returns The sine of the angle (sun(angle)).
calculate_sine <- function(angle) {
  sine_value <- angle

  # Loop for the first four terms
  for (i in 1:4) {
    factorial <- factorial(2 * i)
    sign <- (-1)^(i %% 2)  # Alternate signs with modulo (%)

    # Add terms for sine
    sine_value <- sine_value + sign * (angle^(2 * i)) / factorial
  }

  return(sin_value)
}
```

:::

:::: discussion

Read and evaluate this code.

- Can you tell what the purpose of the function is?
- What is the meaning of the variables?
- Which code would you prefer to use?

::::

This time, the function name is a verb that describes what the code will attempt to do. The description of the function is also written out clearly in a note for the user. There are comment lines (starting with `#`) that explain the mathematicalal method used. Each variable has a descriptive, human-readable name, making the code more intuitive to read. An existing library is used to calculate the factorial, which means we can look up the usage for the `factorial()` function elsewhere.

This approach means that our code is much **easier to interpret**, maintain, and make changes to in the future.

Of course, there may be some syntax in this example that is unfamiliar to you&mdash;but don't worry, we'll learn the basics in this course!

## Real-world examples

Let's review real-world examples of the documentation for software packages that are used in research.

### NumPy user guide

NumPy is a mathematical package for the Python programming language that's used for quantitative computing and linear algebra.
The [NumPy User Guide](https://numpy.org/doc/2.0/user/index.html#user) is a **thorough website** that organised into sections that cover the different aspects of using that package.

It includes a beginner's guide, tutorials for different use-cases, and in-depth write-ups of technical details of certain aspects of the code.
Some of the content is written for a target audience with no assumed knowledge, while other parts are written as a reference for people with some background in mathematics and computer programming.

If we want to read more about how to use a certain feature, there are documentation pages such as [numpy.array](https://numpy.org/doc/stable/reference/generated/numpy.array.html) that describe purpose and the parameters of each function. If we're in a Python interpreter shell, we can use the [`help()` in-built function](https://docs.python.org/3/library/functions.html#help) to view the documentation:

```python
import numpy
help(numpy.array)
```

```
Help on built-in function array in module numpy:

array(...)
    array(object, dtype=None, *, copy=True, order='K', subok=False, ndmin=0,
          like=None)

    Create an array.

    Parameters
    ----------
    object : array_like
        An array, any object exposing the array interface, an object whose
        ``__array__`` method returns an array, or any (nested) sequence.
        If object is a scalar, a 0-dimensional array containing object is
        returned.
...
```

### ggplot2 documentation site

[ggplot2](https://cloud.r-project.org/web/packages/ggplot2/) is a package for the R statistical language that generates data visualisations and graphics.
The [ggplot2 documentation](https://ggplot2.tidyverse.org/index.html) has a simple, accessible layout and **walks a new user through** installing and getting up-and-running with the tool.
The page provides a "cheat sheet" which is a reference guide that lists commonly-used commands in an attractive two-page layout.
The documentation site is moderate in scope and links to several external resources, such as online courses hosted elsewhere.

In R, we can view the documentation for each function by using the `?` syntax. For example, calling `?ggplot2::ggplot` will show the help text for that function or load the reference information in a web browser. Also, if we ever needed to read it, the source code is neatly organised into [R code files](https://github.com/tidyverse/ggplot2/tree/main/R) in the repository. For example, the function [ggplot()](https://github.com/tidyverse/ggplot2/blob/main/R/plot.R) includes an extensive description of the purpose and operation of that code, including a list of the parameters and examples of how to use it.

```R
install.packages("ggplot2")
library(ggplot2)
?ggplot2:ggplot
```

[roxygen2]: https://roxygen2.r-lib.org/index.html
