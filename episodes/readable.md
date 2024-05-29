---
title: 'Code readability'
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 

- What is code readability?
- How do I make my code easier to interpret?
- How do I explain the purpose of my code?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Understand the common ways to make code easy to read
- Learn how to write code comments
- Learn to document data types in Python

::::::::::::::::::::::::::::::::::::::::::::::::

It’s a common trope in the software engineering world that code is **read much more often than it is written**. It’s important that our code is **approachable** for new people to use with confidence, as they might want to review the code itself to understand what it does. Also, when you maintain your code, or come back to it in the future, you’ll be grateful for the effort you made in making it easy to interpret and follow its logic.

## Syntax highlighting

Many text editors use syntax highlighting to display parts of your source code using different colours or fonts to signify the meaning of each word or symbol.
For example, variable names may be given a bright blue colour, strings highighted in green, and numbers shown in a red font.

Let's take a look to see its benefits:

::: group-tab

### Python

Without syntax highlighting:

```output
def count_word_occurrences(filename, word_to_count):
  """
  This function counts the number of times a specific word appears in a text file.
  """
  word_count = 0
  # Read the file line by line
  with open(filename, "r") as text_file:
    for line in text_file:
        # Convert the line to lowercase for case-insensitive counting
        line = line.lower()
        words = line.split()

        # Count the occurrences of the word in the current line
        word_count += words.count(word_to_count)

  return word_count
```

With syntax highlighting:

```python
def count_word_occurrences(filename, word_to_count):
  """
  This function counts the number of times a specific word appears in a text file.
  """
  word_count = 0
  # Read the file line by line
  with open(filename, "r") as text_file:
    for line in text_file:
        # Convert the line to lowercase for case-insensitive counting
        line = line.lower()
        words = line.split()

        # Count the occurrences of the word in the current line
        word_count += words.count(word_to_count)

  return word_count
```

### R

Without syntax highlighting:

```output
# Function to count word occurrences in a text file
count_word_occurrences <- function(filename, word_to_count) {
  text_file <- file(filename, "r")
  word_count <- 0
  
  # Read the file line by line using a loop
  for (line in readLines(text_file)) {
    # Convert the line to lowercase for case-insensitive counting
    line <- tolower(line)
    
    # Split the line into words
    words <- strsplit(line, split = " ")[[1]]  # Extract the first element (vector of words)
    
    # Count the occurrences of the word in the current line
    word_count <- word_count + sum(words == word_to_count)
  }
  close(text_file)
  return(word_count)
}

```

With syntax highlighting:

```R
# Function to count word occurrences in a text file
count_word_occurrences <- function(filename, word_to_count) {
  text_file <- file(filename, "r")
  word_count <- 0
  
  # Read the file line by line using a loop
  for (line in readLines(text_file)) {
    # Convert the line to lowercase for case-insensitive counting
    line <- tolower(line)
    
    # Split the line into words
    words <- strsplit(line, split = " ")[[1]]  # Extract the first element (vector of words)
    
    # Count the occurrences of the word in the current line
    word_count <- word_count + sum(words == word_to_count)
  }
  close(text_file)
  return(word_count)
}
```

:::

Which bit of code is easier to read? What a difference a splash of colour makes! I know which development environment I'd rather work in.

To work with our source code in a colourised way like this, use a text editor or IDE with a syntax highlighting feature such as Notepad++, VSCode, PyCharm, or RStudio.

## Meaningful names

Our code should convey as much **meaning** as possible to the user or developer that's trying to interpret it.

### Variable naming

Every variable has a *name* and a *value*.
For example, the code `x = 42` creates a variable named `x` that has the numerical value of four.
But what does `x` mean? Is it the number of swallows required to carry a coconut? In this case, we have no idea.

That's where **meaningful variable names** come in. Always try to name variables using a noun that describes its contents.
For example, in our case we'd use `laden_coconut_capacity = 42` which is much clearer.

### Function names

A function contains code that defines the performance of an **action**. As with variables, the name of a function should **describe its behaviour** so that the user of that code can anticipate what it will do when they run it.
A vague function name, such as `calc(a, b)` will be mysterious without any more explanation.
Name your functions using a **simple verb phrase** such as `calculate_area(width, height)` so it's easy to interpret their purpose.

::: group-tab

### Python

```python
def calculate_area(width, height):
    """
    Work out the surface area of a rectangle with the specified dimensions.
    """
    area = width * height
    return area
```

### R

```R
calculate_area <- function(width, height) {
  """
  Work out the surface area of a rectangle with the specified dimensions.
  """
  area <- width * height
  return(area)
}
```

:::

### Naming conventions

The communities of developers that use each programming language usually follow a conventional approach when naming objects in their code.

It's also a good idea not to use single-letter names such as `x` or `T` because it may not be clear to someone else what these represent. Also, avoid the common pitfall of naming a variable with the same name as an inbuilt function such as `sum()`.

::: group-tab

### Python

Classes use capitalised words

```python
class VectorSpace:
    pass
```

Variables use lower case with underscores

```python
my_user_name = "Joe"
```

Constants are named using upper case with underscores

```python
NEGATIVE_ONE = -1
```

 the [Naming Conventions](https://peps.python.org/pep-0008/#naming-conventions) section of <acronym title="Python Enhancement Proposals">PEP</acronym> 8.

### R

Classes use capitalised words

```R
setClass("VectorSpace", representation = character())
```

Variables use lower case with underscores

```R
my_user_name <- "Joe"
```

Constants are named using upper case with underscores

```R
NEGATIVE_ONE <- -1
```

For more information about this aspect of coding style, please read the [Style Guide](http://adv-r.had.co.nz/Style.html) in *Advanced R* by Hadley Wickham.

:::

Although these rules aren't strict, because your code will still run without error, it does help clarify your intentions by describing what type of variable or object is being referred to. Whatever you do, please try to follow a consistent style with your collaborators to avoid confusion.

## Code comments

Code **comments** allow us to annotate any part of our software with a human-readable description of the expected behaviour of the code or our general intentions to aid the reader in their interpretation.

To add comments to your code, use the `#` symbol at the start of a new line, like so:

::: group-tab

### Python

```python
# Add three to my age
age = 21
age =+ 3
```

### R

```R
# Add three to my age
age <- 21
age = age + 3
```

:::

It's best practice to use a very concise style when writing code comments. I recommend using active tense verbs.

## Coding convnetions

Proper curly brace structure, indentation, whitespace.

### Block comments

https://peps.python.org/pep-0008/#block-comments

### Inline comments

https://peps.python.org/pep-0008/#inline-comments

## Type hints

Type hints to improve code clarity and enable static type checking for catching errors early in the development process.

https://docs.google.com/presentation/d/1mFgQOG4zIZJW-Kl-STi8VnbekVgxzNF_JSO-UOzjHnU/edit?usp=sharing

### Variable annotations

https://peps.python.org/pep-0526/

::::::::::::::::::::::::::::::::::::: keypoints 

- TODO

::::::::::::::::::::::::::::::::::::::::::::::::
