# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common JavaScript error related to closures within `setTimeout` loops. The example shows how the variable `i` is not captured correctly in each iteration, leading to unexpected output.

## Bug Description
The code uses a `for` loop to schedule multiple `setTimeout` calls.  However, because of how closures work in JavaScript, the value of `i` is not captured as expected for each iteration.  Instead, it logs the final value of `i` (10) for every call.

## Solution
The issue is solved by using an immediately invoked function expression (IIFE) to create a separate scope for each iteration, effectively capturing the value of `i` correctly for each `setTimeout` call.