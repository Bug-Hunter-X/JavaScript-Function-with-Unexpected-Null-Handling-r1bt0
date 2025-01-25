# JavaScript Function with Unexpected Null Handling

This repository demonstrates a common error in JavaScript involving null value handling in functions. The `foo` function intends to add two numbers but returns 0 immediately if either input is null, even though this might not always be the correct behavior.  The solution improves handling for null or undefined values by converting them to 0 before performing the addition.

## Bug

The bug lies in the `foo` function's handling of null values.  It immediately returns 0 if either `a` or `b` is null. This is problematic if null represents a valid, albeit absent, numerical value; returning 0 might not accurately reflect the desired outcome.

## Solution

The improved function in `bugSolution.js` uses the nullish coalescing operator (`??`) to convert null and undefined values to 0 before performing the addition. This ensures that even when one or both inputs are null, the computation produces a more reasonable result.