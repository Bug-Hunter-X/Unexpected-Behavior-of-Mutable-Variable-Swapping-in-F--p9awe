# Unexpected Mutable Variable Swap in F#

This example demonstrates a common pitfall when working with mutable variables in F#.  Because F# passes mutable variables by reference, directly swapping them within a function modifies the original variables, not creating local copies.

The `bug.fs` file contains code that attempts to swap two mutable variables, while `bugSolution.fs` provides a corrected approach.

## How to Reproduce
1. Run `bug.fs`. Observe that the output is unexpected. The variables are modified in-place within the swap function.
2. Run `bugSolution.fs`. Observe that the output is now correct. Using tuples prevents the original variables from being modified.