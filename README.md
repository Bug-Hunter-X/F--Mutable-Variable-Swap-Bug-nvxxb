# F# Mutable Variable Swap Bug

This repository demonstrates a common error in F# when working with mutable variables within functions. The `swap` function attempts to swap the values of two mutable variables, but it fails to do so correctly.

## The Bug

The issue lies in how F# handles mutable variables passed as arguments to functions.  When you pass mutable variables to a function, they are passed by value, meaning a copy of the variable's reference is passed, not a copy of the data itself. The `swap` function modifies these copies, but it does not affect the original variables. 

## The Solution

The solution is to pass the variables by reference or use techniques that directly modify the mutable variables outside the function's scope.  We also show how to achieve swapping using tuples without mutable variables, demonstrating a more functional approach. 

## Running the Code

1. Clone this repository.
2. Open the `.fs` files in a F# IDE (like Visual Studio, VS Code with Ionide, etc.).
3. Compile and run the code. You'll see that the original values of `x` and `y` are unchanged in `bug.fs`, while the `bugSolution.fs` will demonstrate both corrected mutable swap and immutable solution.