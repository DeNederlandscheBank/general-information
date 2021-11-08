# DNB Data Science Community Manifest
Working with data has always been a core competency at De Nederlandsche Bank (DNB). Given the increased availability of data and new tools becoming available, interest is growing and a community is emerging. Community membership comes with benefits but also with responsibilities. Joining our community implies adhering to the principles laid out in this document.

## High Level Summary
### :star: Version Control
#### **1. Track changes in your code** <br>
For reproducibility, it is vital to keep track of changes in your code. The standard way to do this is using a version control system like Git. If you are not familiar with Git, we strongly encourage you to start learning it. At a minimum, you should archive copies of your code from time to time, to keep a rough record of the various states the code has taken during development.

### :star: Coding Practices
**2. Stick to language guidelines and practices** <br>
Make sure to adhere to language specific guidelines related to naming, long lines, and other best practices. Make sure that you are consistent if you choose a certain style and do not mix and match. Add explanatory documentation strings and comments to help colleagues understand your code.

**3. Give your code some thought** <br>
Before starting to write code, try to define the requirements of your code, i.e. what it needs to do. Which functions or other structures do you need and how are they interacting? This provides guidance, exposes possible bottlenecks early and hence saves time later on. Moreover, writing cleaner, more structured code makes it easier to reuse the code.

**4. Avoid manual steps** <br>
In line with above, avoid manual steps. Whether it is manual data manipulation step or copy pasting certain code to repeat a process, this is not a good practice. Instead, write a function to do the data manipulation or write a function to repeat a process: that is what functions are for!
### :star: Peer Review
**5. Code Review** <br>
Peer reviews are essential in academia, medicine and other work fields. We are no exception. Code reviews are an important aspect of code development. Regular reviews enhance code quality and structure and increases learning effects between colleagues. In general, it is advised that you work with another colleague on a project where code needs to be developed, such that a colleague can review your work. If you work alone, make sure to schedule a review with someone else.
### :star: Test your work
**6. Verify correctness of code** <br>
Testing whether the code you wrote is behaving as expected is of vital importance to avoid bugs. This is usually (partly) done with (automated) unit tests. If you are not familiar with unit testing, we advise you to familiarize yourself with this concept. At a minimum, make sure you manually test your functions with a set of test inputs to see whether the output matches your expectations and keep track of the results.
### :star: Project Management
**7. Project Structure** <br>
When starting a project, take some time to think of an appropriate way on how to structure your files and folders. A logical structure paves the way to a clean and maintainable code base. Furthermore, it makes it easier for others to locate files and to contribute to your project.

**8. Storing Output** <br>
Every project will have one or more outputs. Output can take several forms, ranging from trained/fitted models, figures, processed data, reports etc. Create directories to store these outputs.

**9. Reproducibility: track software versions** <br>
Every project will use certain software. For reproducibility, it is essential to keep track of the exact versions of the software you use in your project. By doing this, the requirements to run the code/execute the program are documented.

### :star: 10.  Celebrate!

## Introduction 
Working with data has always been a core competency at De Nederlandsche Bank. Given the increased availability of data and new tools, interest is growing and a community is emerging. Community membership comes with benefits but also with responsibilities. Joining the data science community means adhering to the principles laid out in this document.

A "paper trail" is the cornerstone of any policy institution. In designing, setting and upholding policy we should be able to explain how the available information has shaped our thinking. Some of this information is soft (e.g., impression, market views) but we aim to be increasingly data driven.

New tools and technologies, massive amounts of data (certainly since the Great Financial Crisis), interdisciplinary approaches, and the complexity of the questions being asked are complicating efforts to follow the “paper trail” that has resulted in policy relevant conclusions.

As full step-by-step replication of analysis – sometimes with ad hoc data – is often not feasible, we should aim for reproducible analysis as an attainable minimum standard for assessing the value of policy conclusions. This requires that analyses describe the results and provide a sufficiently clear protocol to allow successful repetition and extension of analyses based on original data.

The importance of replication and reproducibility is key to being transparent about our policy process, to be consistent over time and across institutions, and be able to reap cross-divisional efficiency benefits.

Reproducibility is not only a moral responsibility with respect to our professional calling, but a lack of reproducibility can also be a burden for you as an individual analyst. As an example, a good practice of reproducibility is necessary in order to allow previously developed methodology to be effectively applied on new data, or to allow reuse of code and results for new projects. In other words, good habits of reproducibility may actually turn out to be a time-saver in the longer run. The challenge is to let these long run benefits get the better of the short run time pressures.

At DNB, with meeting deadlines and Single Supervisory Mechanism (SSM) requests, you may face the need to make a trade-off between the ideals of reproducibility and the need to get the analysis out while it is still relevant. This trade-off becomes more important when considering that a large part of the analyses being tried out never end up yielding any results. However, frequently you will, with the wisdom of hindsight, contemplate the missed opportunity to ensure reproducibility, as it may already be too late to take the necessary notes from memory (or at least much more difficult than to do it while underway). We believe that the rewards of reproducibility will compensate for the risk of having spent valuable time developing an annotated catalogue of analyses that turned out to be blind alleys.

In the following manifest, we lay out the most important aspects of producing reproducible work: making sure you store your code and can work together effectively, writing code that is clean and readable, reviewing each other’s work regularly, writing tests for your code and structuring your project. In addition, each of the sections contain concrete recommendations that we strongly recommend sticking to when working on projects.

## Rule 1 – Version Control
Version control helps you to keep track of changes in your code. It is particularly useful when working together in a team on the same project. Without having some sort of version control system in place, you probably work together in a folder on the same files, often with confusing names (v1, v2, final, ...). To make sure you do not accidentally overwrite someone else's code, you constantly have to make sure you are not working on a file a colleague is working on. At some point, you will inadvertently overwrite code. A version control system offers a solution that allows for 
everyone in your team to work on any file and merge the changes later. Even when working on a project on your own, version control helps keep track of changes and allows you revert back to previous versions of your code, essentially providing a backup.

The most popular version control system today is Git. If you are not familiar with Git, you can find a good introduction [here](https://www.atlassian.com/git). Within your team, agree upon a workflow. Depending on the project and what you are comfortable with, use a simple workflow such as using one main branch and developing features on separate branches. When you finish a feature, the feature branch is merged back into the master branch by submitting a pull request. In the pull request, one or more team members can be assigned to review the code you want to merge back into the main branch. For more information on code reviews see Section 4.

Finally, make sure to double check which information you are committing to Git. Use a .gitignore file in your repository to exclude files you do not want checked into version control. For example, make sure you do not include any files that contain confidential data, passwords, keys and/or secrets. Keep in mind that once you commit and push your changes, it will be very hard to erase them from your version history. In other words, think carefully about which files you store in version control.

### Recommendations
* **Agree upon a Git workflow** that fits your project, team size and keeps overhead to a minimum. Start
simple and add complexity as you need it. Not sure where to begin? We recommend either of two popular 
flows: [Gitflow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) or [GitHub Flow](https://guides.github.com/introduction/flow/).
* Make sure you **do not check in confidential information to Git at any cost**.

## Rule 2,3 & 4 – Code Practices
Clean code means your code is easy to read, easy to understand and easy to maintain, extend or modify. Having clean code minimizes the probability colleagues will have to rewrite the same code entirely and improves the probability your code is actually reused. 

When starting with programming, a common workflow often involves lots of copy pasting of code, using names with little meaning, and writing long functions, to name a few things. As long as it works, there seems to be no need to take another route. At some point, however, you realize that changing the code to implement some additional feature becomes very hard and you quickly lose the overall picture. Even working on a project on your own, you will – more often than you think – return to the inefficient codebase that you had written before. For these reasons, making use of code practices as outlined in this section can make you a better programmer, as well 
as make sure your code is actually used. 

Before getting to the guidelines, keep in mind that one of the most important things when working with code is **consistency**. Pick one set of coding conventions and stick to them and use your best judgment when in doubt. 

Below are some of the guidelines you can use to write better and clean code.

### Recommendations
* Use a **Style Guide** that is commonly used for your language. This guide contains coding conventions 
including which case to use for variables names (camelCase, snake_case etc.), how to deal with long 
lines, whitespace and indentation, and how to pick meaningful names. For Python, we recommend [PEP8](https://www.python.org/dev/peps/pep-0008/). 
For R, [the tidyverse style guide](https://style.tidyverse.org/) is recommended. Moreover also make sure your code is split up into smaller functions which only perform a single task.
* **Document and comment** your code using documentation strings (docstrings) and comments. Docstrings 
describe your functions, modules, classes of methods. Conveniently, they allow you to generate 
documentation and help pages and present a consistent way of what readers can expect from the code 
that is written. Bear in mind comments do not make up for bad code: clean your code instead of adding more comments.

## Rule 5 – Code Reviews
Code reviews are essential for every team involved in the development of code. Regular internal and/or external code reviews are of vital importance for high quality, maintainable code. Design problems and bugs are spotted earlier and more often. Moreover, the increased cooperation that is a result of the code review process leads to an atmosphere in which colleagues can learn from each other. As such, there is much more knowledge exchange and possible cross-fertilization (e.g. maybe someone tries to solve the same problem you are trying to solve). Apart from the fact that code reviews enhance the quality of the code and lead to more cooperation and learning, the dependence of an organization on certain developers is decreased. By utilizing regular code reviews, more developers are up to speed with the code behind a certain project/tool. Having a code review process in place can help with keeping up good coding practices. If you know a team member will look at your code, it also forces you to write code which can be understood by others. Lastly, as an organization, we have the responsibility to take our code seriously. Therefore, the following recommendations should be acted on by every team involved in code development.

### Recommendations
* Internal code reviews should always be in place. When working in a team (using version control), make sure to let one of the team members review your merge/pull request. Take these reviews seriously. If it takes too much time, try to do it more often with smaller chunks of code. 
* Strive to work on a project with at least one other person. If you work on a project alone, or are the only one who can do the coding in a project, make sure to schedule an external review with someone. 

## Rule 6 – Testing
The necessity of writing readable, clean and maintainable code is recognized by most people that write code. However, the importance of code testing is often underestimated. Perfect, bug-free code is an illusion. Every codebase will have bugs/errors. These bugs can have a profound impact on users, organizations or even the society. To give a few well-known examples, in 1999 NASA lost a space craft due to a simple unit-conversion problem. In 2012, Knight Capital lost 440 million dollars due to a human error in trading software that could have easily been avoided. 

Obviously, the impact of bugs depends on what the code is used for. Bugs in code that runs "in production" or will be reused often potentially have more impact. Such code should therefore always be tested thoroughly. But testing is not only restricted to such cases. Indeed, in other cases it is also important to verify the correctness of code. Imagine if an important policy decision is made based on code that contains a bug, without which a differentconclusion would be drawn. 

There are several software testing methods (levels). One of the most basic (fundamental) testing procedures is called unit testing. In unit testing, the behavior of units (most often functions) is tested. Basically, it is tested whether the function behaves as the developer expects it to behave. This is done by providing test cases and asserting that these match the expected outcome. Although unit tests will not guarantee bug-free code, they certainly help eliminating bugs and detect problems early. Apart from detecting problems, unit tests have several other advantages:

* Unit tests force you to write clean and maintainable code (bad code is not easily unit tested)
* Having to write tests forces you to think about the behavior of your functions (up front)
* The tests provide additional documentation for other developers (easy to see what the behavior should 
be)
* Unit tests ensure that after refactoring the behavior is unchanged
* Unit tests can be part of your workflow by running the tests (either automatically or manually) before 
making changes in a code base.

### Recommendations
* Unit tests might not always be needed. If you write code for an ad hoc analysis/task unit tests are probably too much. It is still good practice to verify that your code performs as you expect it to do. In any case, be sure not to disregard testing too quickly. In general, in cases where code is written that is regularly reused, unit tests are recommended. Think of functions that you use to preprocess data, create features, automate processes etc. Such functions are easily unit tested save you time in the long run!

## Rule 7,8 & 9 – Managing Your Project
### Structuring your project
When starting a project – whether it’s in Python, R or any other language – take some time to think of an appropriate way of how to structure your files and folders. Structuring your project in a way that meets the goal of your project paves the way to a clean and effective code base. In addition, it makes it easy for your colleagues to find the code they are looking for and contribute to what you have written. Structuring your project is both about creating a logical folder structure as well as thinking about how to structure your code and leverage [software design patterns](https://en.wikipedia.org/wiki/Software_design_pattern).

Tools that can help you with structuring your project include using tools like [cookiecutter](https://cookiecutter.readthedocs.io/en/1.7.2/), which is a tool that creates project skeletons for you from project templates, depending on the language you plan to work with and 
the type of project. For example, you might want to create a Python package or start a data science project. Cookiecutter will then set you up with a commonly used directory structure.

As an example, at some point you might want to organize your R-scripts in a convenient way such that you can easily share it with others and reuse parts of your code. At that point, it is recommended to organize your code into an [R package](https://r-pkgs.org/index.html). 

### Keeping track of software versions
Every project will use certain software (tools, packages, etc.). For reproducibility it is essential to keep track of the exact versions of the software you use in your project. By doing this, the **requirements** to run the code/execute the program are documented. The importance of logging such information is not to be underestimated. A slightly different version of the software might have very different behavior, or might have a different interface leading to code that cannot execute. Another advantage of documenting this information is that it leads to more efficient reuse of your code. Indeed, a colleague only needs to look at the requirements to quickly identify which software (and the exact version of the software) is needed in order to use your code. 

### Dealing with output
Every project will have one or more outputs. Output can take several forms, ranging from trained/fitted (machine learning) models, figures, processed data, reports etc. Aside from structuring the project itself, structuring the way you create, process and store output is also important. In general, having directories in place to hold output is convenient. Thus it is useful to have folders for figures, reports, processed data etc. However, make sure to exclude such folders from version control (e.g. use a .gitignore file). It is crucial to make sure that output is not pushed to a version control system to avoid leakage of confidential data. Make sure to think about in which cases it is appropriate or convenient to store (intermediate) results/output. When doing so, make sure to use appropriate (traceable) names. 

### Recommendations
* Make an effort to structure your project and make use of tools that can help such as cookiecutter.* Use a readme(.md) file at the root of your project directory to introduce people to your repository, lay out your structure and describe how your code works, among other things. For a curated list of great readme’s, see here.
* Keep track of the exact versions of software you use in your project. This will ensure that your work is reproducible and enhances reuse of your code.
* Create folders to store output of your project, be it figures, trained models or reports. Think carefully when you want to store (intermediate) data. Make sure you do not version control these results blindly as this can lead to leakage of (possible) confidential data.

## Rule 10 – Celebrate!