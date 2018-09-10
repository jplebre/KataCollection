# How Big How Fast

## Background Info

Rough estimation is a useful talent to possess, calculating size and time requirements to process information.

## Specification

## Test Data

## Use Case Scenarios

## Specification

A series of questions, each asking for a rough answer. Try to work each out in your head. I’ll post my answers (and how I got them) in a week or so.

1. How Big? 
  Roughly, how many binary digits (bit) are required for the unsigned representation of:

  * 1,000
  * 1,000,000
  * 1,000,000,000
  * 1,000,000,000,000
  * 8,000,000,000,000
  * 20,000 residences, each with names, addresses, and a phone number (as characters)
  * 1,000,000 integers in a binary tree. Roughly how many nodes and levels can I expect the tree to have? Roughly how much space will it occupy on a 32-bit architecture?

2. How Fast?<br>
  * My copy of Meyer’s Object Oriented Software Construction has about 1,200 body pages. Assuming no flow control or protocol overhead, about how long would it take to send it over an async 56k baud modem line?

  * My binary search algorithm takes about 4.5mS to search a 10,000 entry array, and about 6mS to search 100,000 elements. How long would I expect it to take to search 10,000,000 elements (assuming I have sufficient memory to prevent paging).

  * Unix passwords are stored using a one-way hash function: the original string is converted to the ‘encrypted’ password string, which cannot be converted back to the original string. One way to attack the password file is to generate all possible cleartext passwords, applying the password hash to each in turn and checking to see if the result matches the password you’re trying to crack. If the hashes match, then the string you used to generate the hash is the original password (or at least, it’s as good as the original password as far as logging in is concerned). In our particular system, passwords can be up to 16 characters long, and there are 96 possible characters at each position. If it takes 1mS to generate the password hash, is this a viable approach to attacking a password?
