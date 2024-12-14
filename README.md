# JavaScript Loose Comparison Unexpected Behavior with undefined

This repository demonstrates an unexpected behavior in JavaScript's loose comparison (`==`) when dealing with `undefined` values. The function `foo` is designed to return 0 if the input `x` is null, but surprisingly returns NaN when `undefined` is passed as an argument.

## Bug Description
The `foo` function uses loose comparison (`==`) to check if `x` is null.  While this works correctly for null, it does not handle `undefined` as expected due to type coercion during the comparison.  Loose comparison does not always provide reliable results, especially when comparing values of different types.

## Solution
The solution involves using strict equality (`===`) to explicitly check if `x` is null or undefined. Strict equality does not perform type coercion, hence the issue is resolved.