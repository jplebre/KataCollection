Roll Your Own Mock Objects Framework


Estimated Duration: 2-4 hours

Author: Jason Gorman, Codemanship

Language(s)/stacks: Any

Summary:


Create a simple framework for writing tests that fail because of interactions between objects.

It should have the following basic features:

1. Allow you to instantiate a mock object derived from an interface (or a class in languages that don't support pure interfaces/abstractions)

2. Optionally verify expectations that certain methods on the mock instance should be invoked, with specific parameter values

3. Specify a return value from a method invocation if one is required

4. Cause a unit test to fail - with a meaningful/helpful message - when an expectation about a method invocation is not satisfied

If time and inclination allows, it could have more advanced features:

1. Specify how many times (or not at all) a method should be invoked

2. Specify general (property-based) rules for method parameter values



See my own basic attempt at https://github.com/jasongorman/BecauseMock
