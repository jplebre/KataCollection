#FizzBuzz

## The Kata
* Returns 'Fizz' if 3 is passed
* Returns 'Buzz' if 5 is passed
* Returns 'Fizz' if a multiple of 3 is passed
* Returns 'Buzz' if a multiple of 5 is passed
* Returns 'Fizz' if the number passed contains 3
* Returns 'Buzz' if the number passed contains 5
* Returns '' if 0 is passed
* Returns the bare number for all other cases

##Specification

* For multiples of three print 'Fizz' instead of the number.
* For the multiples of five print 'Buzz' instead of the number.
* For numbers which are multiples of both three and five print 'FizzBuzz'. 
* There should be a facility that allows the program to print the numbers from 1 to n (eg. 100).

Sample output:

```
1
2
Fizz
4
Buzz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
16
17
Fizz
19
Buzz

... upto 100.
```

##Tips
Don't focus on the outputed list, focus on what should come out of the program first.
Eg. what is the very first thing the program should do? and the second? and the third?
Output format is not important, specially if you are practicing unit tests or TDD.

##More Variations
Some people on the internet were adding interesting twists like:
* Multiples of Seven Return Pop.
* Multiples of Three and Seven Return Fizz Pop.
* Multiples of Five and Seven Return Buzz Pop.
* Multiples of Three, Five and Seven Return Fizz Buzz Pop.
