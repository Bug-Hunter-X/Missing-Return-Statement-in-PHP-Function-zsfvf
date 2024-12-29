# Missing Return Statement Bug in PHP

This repository demonstrates a common yet easily overlooked bug in PHP: missing return statements in functions.  This seemingly small omission can cause significant problems, especially when the function's output is relied upon elsewhere in your code.

The `bug.php` file contains the problematic code. The `bugSolution.php` file shows the corrected version.

## Bug Description

When a PHP function is declared to return a value, it *must* include a `return` statement to actually return that value.  Failure to do so results in the function implicitly returning `null`. This can lead to unexpected results in conditional statements, assignments, or other parts of the code that depend on the function's intended output.

## How to Reproduce

1. Clone this repository.
2. Run `bug.php`. Observe the unexpected output.
3. Run `bugSolution.php`. Observe the corrected output.

## Solution

Ensure that every function that is declared to return a value includes a `return` statement. Always explicitly specify the return value.