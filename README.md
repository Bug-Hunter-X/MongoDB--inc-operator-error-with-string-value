# MongoDB $inc Operator Error
This repository demonstrates a common error when using the `$inc` operator in MongoDB updates.  The error occurs when attempting to increment a field with a string value instead of a numeric value.

## Bug Description
The `$inc` operator in MongoDB is designed to increment numeric fields. Providing a string value leads to unexpected string concatenation, instead of the expected numeric increment.

## Bug Reproduction
1. Create a MongoDB collection.
2. Insert a document with a numeric field.
3. Attempt to update the document using `$inc` with a string value.
4. Observe that the field is not incremented as expected but is instead modified by string concatenation.

## Solution
Ensure that the value provided to the `$inc` operator is a number. Correct the value provided to `$inc` to be a numeric type.