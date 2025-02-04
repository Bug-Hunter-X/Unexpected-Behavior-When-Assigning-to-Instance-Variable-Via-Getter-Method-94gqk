# Ruby Bug: Unexpected Instance Variable Assignment

This repository demonstrates an uncommon bug in Ruby related to the unexpected behavior of assigning a value to an instance variable using its getter method.  The getter method appears to accept the assignment, but the instance variable remains unchanged.

## Bug Description
The code defines a simple class `MyClass` with an instance variable `@value` and a getter method `value`.  Assigning a new value using `my_object.value = 30` appears to succeed (it returns 30), but the actual value of `@value` remains unchanged. This is counter-intuitive and potentially leads to hard-to-debug errors.

## Bug Reproduction
The `bug.rb` file contains the code demonstrating the issue.  Running this file will show the unexpected output.

## Solution
The `bugSolution.rb` file provides a solution that addresses this issue by explicitly modifying the instance variable within the getter method or using a setter method.