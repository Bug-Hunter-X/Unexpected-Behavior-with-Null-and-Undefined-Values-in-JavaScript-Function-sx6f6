# JavaScript Function Bug: Null and Undefined Handling

This repository demonstrates a common yet subtle bug in JavaScript functions related to the handling of `null` and `undefined` values. The original code attempts to handle `null` values gracefully, but it fails to address the case where a parameter is `undefined`.

## Bug Description

The `foo` function is designed to add two numbers. It explicitly checks for `null` values in both parameters.  However, if either `a` or `b` is `undefined` instead of `null`, the addition will lead to unexpected results (NaN).  The solution improves upon this by checking for both `null` and `undefined` values.

## How to Reproduce

1. Clone the repository.
2. Open `bug.js` to see the buggy code.
3. Run `node bug.js` in your terminal.  You'll see the unexpected behavior when calling the function with undefined arguments.
4. Open `bugSolution.js` to see how to fix the bug.
5. Run `node bugSolution.js` to observe the correct handling of null and undefined values.

## Solution

The solution addresses the bug by using the loose equality operator (`==`) to compare both `null` and `undefined` values. Alternatively, a more strict approach would be to use typeof to explicitly check for undefined and null.