# Fibonacci Sequence Generator

## Background Info

Create a program that outputs the Fibonnacci sequence;


## Specification
* Fibonacci sequence starts with the number `0`, followed by the number `1`;
* Each number is the addition of the 2 previous numbers;
* Meaning, number 3 is `0 + 1 = 1`, number 4 is `1 + 1 = 2`;
* There should be a facility that allows the program to print the fibonacci sequence up to a predefined length (eg. 100).

## Tips
Don't focus on the outputed list, focus on what should come out of the program first.  
Eg. what is the very first thing the program should do? and the second? and the third?  
Output format is not important, specially if you are practicing unit tests or TDD.  

Also, depending on what you start testing, the outcome can be quite different.  
Eg. One of my approaches led me to use recursive methods. This was a problem if you tried to generate a sequence larger than 45 numbers long.

## Test Data
Sample output:

```
0
1
1
2
3
5
8
13
21
34
55
89
...
```

## Use Case Scenarios