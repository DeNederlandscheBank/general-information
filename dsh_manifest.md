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

## Rule 1
Version control helps you to keep track of changes in your code. It is particularly useful when working together in a 
team on the same project. Without having some sort of version control system in place, you probably work together 
in a folder on the same files, often with confusing names (v1, v2, final, ...). To make sure you do not accidentally 
overwrite someone else's code, you constantly have to make sure you are not working on a file a colleague is working 
on. At some point, you will inadvertently overwrite code. A version control system offers a solution that allows for 
everyone in your team to work on any file and merge the changes later. Even when working on a project on your 
own, version control helps keep track of changes and allows you revert back to previous versions of your code, 
essentially providing a backup.

The most popular version control system today is Git. If you are not familiar with Git, you can find a good 
introduction [here](https://www.atlassian.com/git). Within your team, agree upon a workflow. Depending on the project and what you are comfortable with, use a 
simple workflow such as using one main branch and developing features on separate branches. When you finish a 
feature, the feature branch is merged back into the master branch by submitting a pull request. In the pull request,
one or more team members can be assigned to review the code you want to merge back into the main branch. For 
more information on code reviews see Section 4.

Finally, make sure to double check which information you are committing to Git. Use a .gitignore file in your 
repository to exclude files you do not want checked into version control. For example, make sure you do not 
include any files that contain confidential data, passwords, keys and/or secrets. Keep in mind that once you 
commit and push your changes, it will be very hard to erase them from your version history. In other words, think 
carefully about which files you store in version control.

### Recommendations
* **Agree upon a Git workflow** that fits your project, team size and keeps overhead to a minimum. Start
simple and add complexity as you need it. Not sure where to begin? We recommend either of two popular 
flows: [Gitflow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) or [GitHub Flow](https://guides.github.com/introduction/flow/).
* Make sure you **do not check in confidential information to Git at any cost**.

## Rule 2

## Rule 3

## Rule 4

## Rule 5

## Rule 6

## Rule 7

## Rule 8

## Rule 9

## Rule 10
