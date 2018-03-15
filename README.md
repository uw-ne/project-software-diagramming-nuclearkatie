## EP476: Introduction to Scientific Computing for Engineering Physics

Spring 2018

**Due: Thursday, Mar 22, 1:00 PM**

# Software Diagram

An important part of any software development plan is to break the problem
down into individual functions and define the expected input, output and
behavior of those functions.  This can be done in many forms, whether its
pseudo-code in text files or a graphical respresentation.

At the highest level, both projects this year have the following structure:

* read input
* solve physics
  * setup problem
  * loop over time steps
     * build matrix
     * (possibly solve matrix equation A.x=b)
     * update time step
* write output

Many of the items above can be broken down into additional substeps, possibly
with some hierarchy.  When complete, nearly every bullet will represent a
distinct function that must be called.  (Some bullets may represent loops
within functions, as seen above.)

This assignment is to complete the diagram for your software.  When complete,
you should have a more detailed outline, based on the one above.  For each
entry, you should also have a detailed function signature, including a
docstring.

```
def perform_a_task(useful_data, more_data):
    """This function will extract entries from `useful_data` and apply
    some operation based on `more_data` to calculate a result.

    inputs
    ------
    - useful_data : list of strings (or whatever, as appropriate) containing some data
    - more_data   : dictionary (or list or integer or whatever)

    outputs
    -------
    - result : numpy array (or whatever) containing the results
    """
```

Each team will prepare their repository to outline a project plan that
includes the elements below.  When complete, these elements should communicate
a strong vision for how your project will proceed, but will be subject to
refinement.

Each team member will also submit a response to individual questions found
below.

For all parts, you may want to consult the
[Github markdown](https://guides.github.com/features/mastering-markdown/)
guide.

## Plan Elements

### README.md

A detailed description of the project requirements:
 * What problem will it solve?
 * What is the scope of the project in terms of fidelity and complexity?
 * What is considered out of scope for your project?

### Elements of a Health Community

Complete the checklist of items considered necessary for a healthy community
by Github:

* Description
* README (see above)
* Code of Conduct
* Contributing guidelines (including a style guide)
* License

_Note: Issue or Pull Request templates are not important at this point as your
project is too new._

### Github Project

Establish (at least) a top-level project in your Github repo.  Use projects to
manage the dependency and flow of small tasks.  Consider at least four columns:

* Backlog - items that will eventually need to be completed
* On-Deck - items that should be completed next
* In Progress - items that are being actively worked on by someone
* Complete - items that have been completed

You may be interested in other columns to indicate status, but these four are
a good starting point.

### Github Milestones

Create Milestones for your project that provide a way to measure progress
towards the ultimate goal.  Each milestone should have a reasonable
description of what will constitute completion of that milestone.  Do not get
paralyzed by selecting dates, as you will be able to modify milestones as you
go.  They should help you judge your progress and rate of progress, however.

### Github Issues

Create some issues to populate the project and milestones.  Assigning issues
to both a project and milestone allows you to take advantage of both concepts:
managing their "flow" and counting them against a deadline.

## Individual Questions

Reflect on the dynamics of your group so far.

1. Is the group interacting in a healthy way that will allow everyone to make
   meaningful contributions?  Describe why you believe this is the case?

1. Do you feel safe expressing your opinions and ideas within the group?
   Describe why you believe this is the case?

Your answers are not anonymous but will be held confidential.

### Submission Process for Individual Questions

This submission process will rely on `git` and `github` as a way to test some
of your skills.

1. By visiting this repository you have claimed your fork of this repo

1. Clone the repo to your local filespace (at CAE or elsewhere)

1. Make a branch to start your proposal named `timeline_reflection`

1. create a new file and answer the first question above

1. add and commit that file

1. push your `timeline_reflection` branch to your github repository

1. create a pull request to request that `timeline_reflection` is merged into `master`, but do NOT merge

1. request a review from me in the pull request to complete the submission

