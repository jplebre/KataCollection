# Binary Chop

## Background info

A binary chop/binary search finds the position of value in a sorted array of values. 
It finds the middle index of the array and establishes if the value is above or below the split point.
It stops when it finds the value it is looking for, or when it runs out of array to search.

Implement in the language/technique of choice.
Repeat it using totally different techniques until you have five totally unique implementations of a binary chop.

Example:
* Iterative approach 
* Recursive approach
* Functional style passing array slices around
* etc.

## Tips
1. Keep track of errors you encounter (“off by one”, etc.)
2. Compare the techniques chose.
  * Which is the most likely to make it in to production code? 
  * Which was the most fun to write? 
  * Which was the hardest to get working? 
  * etc.
3. It’s hard to come up with five unique approaches to a binary chop.

## Specification
* Binary chop method that takes an integer search target and a sorted array of integers. 
* Should return the integer index of the target in the array, or -1 if the target is not in the array.
* You can assume that the array has less than 100,000 elements.
* The signature will logically be:

```Ruby
chop(int, array_of_int)  -> int
```

## Test Data
Example of the Test::Unit code (in Ruby) I used when developing my methods. Feel free to add to it. 
The tests assume that array indices start at zero.

```Ruby
def test_chop
  assert_equal(-1, chop(3, []))
  assert_equal(-1, chop(3, [1]))
  assert_equal(0,  chop(1, [1]))
  #
  assert_equal(0,  chop(1, [1, 3, 5]))
  assert_equal(1,  chop(3, [1, 3, 5]))
  assert_equal(2,  chop(5, [1, 3, 5]))
  assert_equal(-1, chop(0, [1, 3, 5]))
  assert_equal(-1, chop(2, [1, 3, 5]))
  assert_equal(-1, chop(4, [1, 3, 5]))
  assert_equal(-1, chop(6, [1, 3, 5]))
  #
  assert_equal(0,  chop(1, [1, 3, 5, 7]))
  assert_equal(1,  chop(3, [1, 3, 5, 7]))
  assert_equal(2,  chop(5, [1, 3, 5, 7]))
  assert_equal(3,  chop(7, [1, 3, 5, 7]))
  assert_equal(-1, chop(0, [1, 3, 5, 7]))
  assert_equal(-1, chop(2, [1, 3, 5, 7]))
  assert_equal(-1, chop(4, [1, 3, 5, 7]))
  assert_equal(-1, chop(6, [1, 3, 5, 7]))
  assert_equal(-1, chop(8, [1, 3, 5, 7]))
end
```
