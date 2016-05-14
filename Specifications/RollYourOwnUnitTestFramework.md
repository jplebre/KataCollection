Roll Your Own Testing Unit Testing Framework


Estimated Duration: 2-4 hours

Author: Jason Gorman, Codemanship

Language(s)/stacks: Any

Summary:


Bootstrap a framework for TDD by TDD-ing a unit testing tool for your chosen programming language.

Write a framework, with a command line application for runing tests, that will allow you to write and execute unit tests in your chosen programming language.

It should have the following basic features:

1. Allow you declare test methods/functions using some convention (e.g., attributes in Java, or a naming convention like "test*" for method names.

2. Find all test methods in a project and execute them using a command line application

3. Allow you to write Boolean test assertions, with an optional failure message

4. Record results of test executions (PASS, FAIL, UNHANDLED EXCEPTION) and print them to screen

If time and inclination allows, it could have more advanced features:

1. Reuse test methods by parameterising them, and treating each set of parameter values as a test when executed

2. Allow for more targeted assertions, like asserting that two values are equal, or two objects are the same object.

3. Runs from inside your IDE with a simple menu item

4. Can draw test parameter values from text files for customer testing
