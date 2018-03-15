## EP476: Introduction to Scientific Computing for Engineering Physics

Spring 2018

**Due: Thursday, Mar 22, 1:00 PM**

# Software Diagram

An important part of any software development plan is to break the problem
down into individual functions and define the expected input, output and
behavior of those functions.  This can be done in many forms, whether its
pseudo-code in text files or a graphical representation.

At the highest level, both projects this year have the following structure:

* read input
* solve physics
  * setup problem
  * loop over time steps
     * build matrix
     * (possibly solve matrix equation A.x=b)
     * update time step
* write output

Many (most?) of the items above can be broken down into additional sub-steps,
possibly with some hierarchy.  When complete, nearly every bullet will
represent a distinct function that must be called.  (Some bullets may
represent loops within functions, as seen above.)

This assignment is to complete the diagram for your software.  When complete,
you should have a more detailed outline, based on the one above.  In addition,
for each entry, you should also have a detailed function signature, including
a docstring.

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

## Specific Tasks

1. Create an issue for each function that will be need to be created. As your
   project continues, you can use the discussion for that issue to keep track
   of changes that emerge from the implementation process.  Consider if/how
   sets of issues make sense to combine into a project and/or contribute to a
   reaching a milestone.

1. Add a complete outline to your README file that shows the flow among all
   the functions you have defined. Include links to each issue created above.

## Important Considerations

1. Data models: What standard data structures will you use throughout your
   problem? If one function assumes a certain structure to some data in its
   list of arguments, then another function must ensure that it has that
   structure.

1. Interface: What data will each function need to complete its task? How will
   that data be shared with that function? Will you have many arguments? Will
   you "pack" the data into a container of some kind?  Which choice will make
   your code easier to read and maintain?

1. Separation of Concerns: Does each function have a single clear and
   unambiguous task? How easy will it be to test that the function is
   correctly performing its task?  


## Additional Guidance

This stage of the software design process is one of the most important, and
often the most challenging for new software developers.

1. Fail early and fail often. Don't be afraid to be wrong early on in this
   process.  Since you are not actually writing code, the cost of changing
   your plan is low and it is better to pursue a plan until you find a reason
   that it won't work, than to imagine all the flaws before you pursue the
   plan.  In fact, one of the reasons this stage is so important is that it
   is "cheaper" to iterate through design ideas at this stage.

1. Seek assistance and guidance when necessary. This process becomes easier
   with experience because you will start to recognize design patterns that
   crop up repeatedly in many contexts.  As early software developers, you may
   not recognize those patterns yet, making it more challenging to explore
   different options.

1. This may require a single longer-than-one-class-period session to map out
   the entire structure together.  A shared understanding of the problem, how
   it can be decomposed and how that leads to your software design will allow
   everyone to contribute, both in this design process, and ultimately in its
   implementation.

1. Err on the side of too many functions and too much granularity. In my
   experience, new software designers generally do not implement sufficient
   modularity and have functions that are too large with too many concerns. It
   is always easier to combine functions that to break them apart.

## Bonus: pseudo-code

When it comes time to implement each function, you are encouraged to separate
the thought process of designing the algorithm from the process of producing
the correct Python syntax.  Before writing the code, use comments to outline
the steps you will take within the function using any phrasing or language
that makes sense to you.  In particular, don't worry about the details of
Python syntax at this point.  As new python developers, the burden of seeking
the right syntax will distract your thought process from algorithm design.
Once you have a good sense of the algorithm, you can focus on getting the
syntax correct.  Undoubtedly, this will introduce some changes to your
algorithm, but typically in small ways.

If you already have thoughts about algorithm design while completing the
diagramming process, feel free to include pseudo-code with your function
signatures.

## Double-bonus: Strive for Independence

In the ideal, each function should not care how its input data was generated
or how its output data will be used.  Take the example of the interface
between reading the input and solving the problem.  For your problem, there
will be some set of data that must be provided by the user to fully define the
problem.  The "Solve Physics" block of your code, at the highest level of
breakdown, should be agnostic about whether that data was read from a file,
extracted from the command-line, or typed into some python code by a user.
For testing/demonstration purposes, you'll need to implement at least one of
those, but the design should be such that no changes are needed to the "Solve
Physics" block if/when someone implements a different method for providing
input.

The biggest benefit of this kind of independence is that it will allow you to
divide up the effort and work in parallel.
