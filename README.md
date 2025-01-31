# PHP Loose Comparison Pitfall

This repository demonstrates a common, yet subtle, error in PHP related to loose comparisons using the `==` operator.  Loose comparison can lead to unexpected behavior when comparing values of different types, especially strings and numbers.

The `bug.php` file contains the problematic code, while `bugSolution.php` shows the corrected version using strict comparison (`===`).

## Problem

PHP's loose comparison (`==`) performs type juggling before comparison. This means it attempts to convert the operands to a common type before evaluating the equality. This can lead to situations where a string and an integer are considered equal, even though they are not strictly the same.

## Solution

The solution involves using strict comparison (`===`). Strict comparison does not perform type juggling and checks both value and type for equality. This eliminates the possibility of unexpected results due to type coercion.