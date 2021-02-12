# Coding Conventions & Style Guides
This markdown document describes the coding conventions and style guide we strongly advise you to use. Adherring to a style guide improves readability and consistency of your code and demonstrates professionalism. After all, as Guido van Rossum (creator of Python) said, code is read much more often than it is written. 

In addition to conventions, this page suggests packages that can help you follow the guides and style your code.

**NB: This is a work in progress. The most important points for now:**

**- For Python: use [PEP8](https://realpython.com/python-pep8/) as a guideline to style your Python code. Use [linters](https://code.visualstudio.com/docs/python/linting) to check your code. VSCode is arguably the best and [most used](https://www.datacamp.com/community/tutorials/top-python-ides-for-2019) editor right now. 
- For R: use [The Tidyverse Style Guide](https://style.tidyverse.org/) and R packages `lintr` and `styler` to check and style your code according to a style guide.
**

# Table of Contents
- [Python](#Python)
- [R](#R)


## Python
### Style Guide
One of the most used styled guides for Python is the PEP8 (PEP = Python Enhancement Proposals) Style Guide for Python Code. Find it **[here](https://www.python.org/dev/peps/pep-0008/)**. 

A number of highlights:

- Naming Conventions

  :point_up: **Consistency is key!**
  | Type     | Examples                                      |
  |----------|-----------------------------------------------|
  | Function | `function`, `my_function`                     |
  | Variable | `x`, `var`, `my_variable`                     |
  | Class    | `Model`, `MyClass`                            |
  | Method   | `class_method`, `method `                     |
  | Constant | `CONSTANT`, `MY_CONSTANT`, `MY_LONG_CONSTANT` |
  | Module   | `module.py`, `my_module.py`                   |
  | Package  | `package`, `mypackage`                        |
- Write docstrings for all public modules, functions, classes, and methods. The recommended way of doing it is using the reStructuredText (reST) format, because it allows you to easily generate documentation based on these docstrings with [Sphinx](https://sphinx-rtd-tutorial.readthedocs.io/en/latest/docstrings.html).
  ```python
  def func(arg1, arg2):
    """Summary line.

    Extended description of function.

    :param int arg1: Description of arg1.
    :param str arg2: Description of arg2.
    :raise: ValueError if arg1 is equal to arg2
    :return: Description of return value
    :rtype: bool

    :example:

    >>> a=1
    >>> b=2
    >>> func(a,b)
    True
    """

    if arg1 == arg2:
        raise ValueError('arg1 must not be equal to arg2')

    return True
  ```
- Limit all lines to a maximum of 79 characters. This is, among other things, useful to be able to have multiple files open side-by-side, e.g. to do a code review. Use parentheses to break lines:


  ```python
    income = (gross_wages
            + taxable_interest
            + (dividends - qualified_dividends)
            - ira_deduction
            - student_loan_interest)
  ```
- ...

### Useful packages to help you with formatting your code
- flake8

## R
### Style Guide
[The Tidyverse Style Guide](https://style.tidyverse.org/)

### Useful packages to help you with formatting your code
- `styler` and `lintr`
