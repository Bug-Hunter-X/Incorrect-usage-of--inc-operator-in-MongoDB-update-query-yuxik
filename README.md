# Incorrect Usage of $inc Operator in MongoDB Update Query

This example demonstrates an uncommon error that can occur when using the `$inc` operator in MongoDB update queries.  The `$inc` operator is used to increment a numerical field by a specified value. However, if the value provided is not a valid number (e.g., a string), the update operation will fail unexpectedly.

The bug showcases an incorrect usage where a string '1' is provided as the increment value, instead of the integer 1. This will not increment the counter but lead to incorrect results. The solution demonstrates the correct usage using an integer.  This issue can be particularly tricky to debug since it doesn't always throw an explicit error, but instead leads to silently incorrect data.