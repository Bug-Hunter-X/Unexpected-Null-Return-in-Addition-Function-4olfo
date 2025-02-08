# Unexpected Null Return in JavaScript Addition Function

This repository demonstrates a subtle bug in a JavaScript function designed to add two numbers. The function unexpectedly returns `null` if either of the input arguments is `null`, even if the other argument is a valid number.  This behavior might be unexpected and could lead to errors in applications that rely on the function's output.

The `bug.js` file contains the buggy code, and `bugSolution.js` provides a corrected version that addresses this issue.

The bug is demonstrated by the use of the strict equality operator (===) in the null checks. This results in null being returned even if only one argument is null.

## How to Reproduce

1. Clone this repository.
2. Open `bug.js`.
3. Run the code using a JavaScript runtime (Node.js, browser's console, etc.).
4. Observe the unexpected `null` outputs when one or both input are `null`.

## Solution

The solution involves modifying the null check to handle the case where only one argument might be null, allowing addition to proceed if at least one argument is a number.