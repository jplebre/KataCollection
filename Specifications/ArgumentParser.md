# Argument Parser

## Background Info
Read and Parse CLI flags;

## Specification

## Test Data

## Use Case Scenarios

* Converts short options to booleans -a
* Converts many short options into booleans –a -b
* Converts many short options together into booleans -abc
* Converts many separated short options together into booleans –abc -def
* Converts long options into booleans --foo
* Converts many long options into booleans –foo --bar
* Adds the value to equal signed separated long options --foo=”bar”
* Will only parse valid options
* Lets you set short options that take no value
* Lets you set long options that take no value
* Creates aliases
* Sets options with mandatory value
* Sets options separated by a space
* Sets long options separated by a space
* Accepts short option and value to be concatenated
* Lets you set long options separated by space
* Converts multiple cases simultaneously
* Creates an argument list
