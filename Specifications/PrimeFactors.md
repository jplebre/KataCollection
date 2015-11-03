Explanation

Write a method that takes in an integer and returns all prime factors for that number. For example, passing in the number 4 would return a list containing 2,2. Notice I said method...don't go creating a complicated class or project structure. Just create a test fixture and put a method right in there ;-).

Goals

Start with the simplest implementation possible. Don't try to find a solution all at once. This kata will help you create the muscle memory to start with the most naive solution first. In fact, I'm recommending you write your tests in this order (again, only write enough code to make each test pass):

given 0, should return empty list
given 1, should return empty list
given 2, should return 2
given 3, should return 3
given 4, should return 2,2
given 5, should return 5
given 6, should return 2,3
given 9, should return 3,3
given int.max, should return int.max
En-passe

With this kata, you'll also learn the concept of an en-passe. Were there instances in this kata where your algorithm had to completely change? Your implementation should evolve as make more tests pass...if you find that your implementation changes drastically with each new test, repeat the kata until it evolves smoothly.

Get Up and Running. Fast.

This was the first kata I tackled, and did it many many times. 
Every time you do this kata, think about how long it takes you to get your first failing test going (i.e. setting up the project/sln/folder structure and getting your test runner to execute the first failing test). Work at getting that first failing test up and running quickly. I would recommend using [WarmuP] and create a project template to decrease that start up time. Here is my WarmuP template for [C#/NSpec Katas], [Ruby Katas], and [JavaScript/CoffeeScript katas]. 
I'm up and running in literally 15 seconds.
