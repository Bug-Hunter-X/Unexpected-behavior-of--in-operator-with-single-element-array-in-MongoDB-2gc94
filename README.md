# MongoDB $in operator with single element array
This example demonstrates an uncommon error related to the usage of the `$in` operator in MongoDB queries. Specifically, it highlights the unexpected behavior when using `$in` with a single-element array containing a string value.

## Problem
The `$in` operator is typically used to query for documents where a field's value is present in a specified array. However, when using `$in` with a single-element array, especially if that element is a string, the query might not produce the expected results.

## Solution
To correctly query for a document with a specific field value, use the equality operator `$eq` instead of `$in`. If you're dealing with multiple possible values, then use `$in` with an array of multiple values. For example, to check for the value 'value', you should replace the code in `bug.js` with the one in `bugSolution.js`.
