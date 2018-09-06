# Numbers to Words Kata

## Getting setup
Have python & [pipenv](https://github.com/kennethreitz/pipenv) and install the deps:

```bash
pipenv install
```

Run the tests so you know your env works:

```bash
pipenv run pytest
```

## The Kata

Create a program which given an integer produces the english words representing that number.

* 1 -> One
* 13 -> Thirteen
* 105 -> One hundred and five.
* 2103 -> Two thousand one hundred and three

### Extension 1
With the above working extend the input so floats are covered using fractions

* 1.5 -> One and a half
* 12.75 -> Twelve and three quarters
* 5.05 -> Five and five hundredths

### Extension 2
Add additional functionality to produce a number from english words. The reverse of the above.

* One -> 1
* Thirteen -> 13


## Credits

http://codingdojo.org/kata/NumbersInWords/