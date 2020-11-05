# Coding Conventions & Style Guides
This markdown document describes the coding conventions and style guide we strongly advise you to use. Adherring to a style guide improves readability and consistency of your code and demonstrates professionalism. After all, as Guido van Rossum (creator of Python) said, code is read much more often than it is written. 

In addition to conventions, this page suggests packages that can help you follow the guides and style your code.

# Table of Contents
- [Python](#Python)
- [R](#R)


## Python
One of the most used styled guides for Python is the PEP8 (PEP = Python Enhancement Proposals) Style Guide for Python Code. Find it **[here](https://www.python.org/dev/peps/pep-0008/)**. 

A number of highlights:

- Write docstrings for all public modules, functions, classes, and methods. The recommended way of doing it can be found [here](https://www.python.org/dev/peps/pep-0257/).
- Function names should be lowercase, with words separated: calculate_x_with_y
- Limit all lines to a maximum of 79 characters. This is, among other things, useful to be able to have multiple files open side-by-side, e.g. to do a code review. Use parentheses to break lines:

  ```python
    income = (gross_wages
            + taxable_interest
            + (dividends - qualified_dividends)
            - ira_deduction
            - student_loan_interest)
  ```
## R
