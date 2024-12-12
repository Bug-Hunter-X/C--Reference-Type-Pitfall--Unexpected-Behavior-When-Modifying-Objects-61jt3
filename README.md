# C# Reference Type Pitfall: Unexpected Behavior When Modifying Objects

This repository demonstrates a common error in C# related to how reference types are handled.  The `bug.cs` file shows code that unexpectedly modifies a variable when a seemingly independent variable is altered. The `bugSolution.cs` file offers a solution.  Understanding reference types is crucial for avoiding this type of error.

## Understanding the Issue

In C#, reference types (like classes) store references to objects in memory, not the objects themselves.  When you assign a reference type variable to another, both variables point to the same object. Therefore, modifying the object through either variable will affect both.

## How to Avoid This Issue

To avoid unintended modifications, create a deep copy of the object when necessary. Several methods exist for creating a deep copy, depending on the complexity of the object.  See the solution file for an example.