# Prep exercise - Cat walk with Promises

In the Browsers module you made an exercise to make a cat walk on the screen until it was halfway, then do a dance for 5 seconds after which it will continue walking until the end of the screen. In this exercise the result should be the same, but this time we want to use `Promise`s to write it in a different way.

Have a look [here](https://github.com/HackYourFuture/Assignments/tree/main/2-Browsers/Week1#exercise-5-the-cat-walk) to remind yourself what the goal of the code was and then do the steps written in `index.js`. We have already provided a couple of functions for you.

## Things to think about

- What do you think the advantages are of having the constants in the global scope? Are there any disadvantages?
  Advantages:
They are accessible from any part of the code, which means constants do not need to be redefined multiple times.
Since the values of constants do not change once defined, the chances of making mistakes are reduced.
Disadvantages:
They can cause naming conflicts because they are available throughout the entire code.
The global scope can be hard to manage in large projects, potentially reducing code readability.

- To make the code loop we cannot use a standard JavaScript loop (`for` or `while`). Why is that?
  Standard loops ('for' or 'while') execute synchronously and complete all iterations immediately. However, walking and dancing are asynchronous operations, and we need to wait for each step to complete before proceeding to the next. Therefore, we use 'Promise' to handle these asynchronous operations effectively.

- Do you feel this version is easier to read than the version you made in the Browsers module?
  This version is easier to read because using 'Promise' makes asynchronous operations more understandable and manageable. This is especially helpful when dealing with a series of asynchronous tasks.

- Is this version more efficient or not or does it not matter?
  In terms of performance, there is no significant difference because both versions perform the same tasks. However, using 'Promise' makes the code cleaner and easier to maintain, which can indirectly lead to more efficient development processes.