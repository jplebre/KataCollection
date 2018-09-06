# KataCollection
Collection of Kata Descriptions.  
Disclaimer: None of these are mine. Taken from several git repos and blog posts or books. I aim to rewrite them into exercises as I work with them and as I do katas at our code dojo sessions or at home to better suit my purpose.

Hopefully they'll be useful to you.

I've tried my best to put the source next to each Kata in the line below. If you feel I'm breaching some copyright please let me know and I'll remove it ASAP.

## What is Code Kata

A Code Kata is a time reserved for a developer to practice solving a specific programming problem. By repeatedly solving that problem the developer becomes better at it. By practicing TDD the developer becomes better at it. That practice has a few characteristics that differentiates it from normal day-to-day practice: It is uninterrupted, simple but challenging enough, you are comfortable making mistakes, no project or environment pressure, make steps forward as small as you can.

In the Code Clubs a Kata session will take about 1 hour. The session is broken down into 3 rounds. At the first round each individual will try and solve the problem themselves. The next 2 rounds they will pair with different developers to solve the problem. The problem is solved using TDD.

Kata, term borrowed from martial arts, literally traslanted as "form", refers to a series of choreographed patterns of movements that are practiced repeatedly by martial arts learners, as a way to develop strong techniques and mastery. It can't be enough reinforced that one will not learn by picking up fights in the street, but by practice in the presence of a master, or sensei, until the kata movements becomes one's own.

This is not common only to martial arts. [Malcolm Gladwell](http://www.amazon.co.uk/Outliers-Story-Success-Malcolm-Gladwell/dp/1846141214) reports that a study of students at the Berlin Academy of Music shows that 10,000 hours of practice is what it takes to make an elite performer. But remember "It's not practice that makes it perfect. It's perfect practice".

[Dave Thomas](http://codekata.com/) was the first to use the term Code Kata in terms of software engineering deliberate practice.

# Conducting a Kata

### To have a good kata session you need:
* **Time** without interruptions.
* **A simple** kata theme.
* **Continuous feedback**. A tool like PHP_Autotest is fine.
* **Make sure** attendants have installed PHPUnit, PhpSpec or equivalent before coming to the kata

### Prior to the kata:

* **Select a kata** you want the group for focus on. Practice it yourself, and identify what is it that you are practicing in that specific kata.
* **Setting the environment**. Make sure you have a room with enough tables for all attendees. If possible arrange the tables so you can have 2 developers sitting next to each other.

### During the kata:

* **Introduction**. Explain what kata is and what we will be the focus of the session.
* **Present the rules**. Explain we are using the 3 laws of TDD and the 4 rules of simple design throughout the exercise.
* **Present the kata**. Describe the problem. List some recommended test cases or specs.
* **Hands on**. Ask the participants to solve the problem individually. Give them 15 to 20 minutes, but specify exactly how much.
* **Delete!** At the end of the time, ask the participants to delete their code. Yes, you heard me!
* **Pair Programming**. Now, ask each participant to join another participant. They will solve the same problem in pairs. Only now they can benefit from each other previous experience. At the end of the time limit, ask them to delete again. Ask how did it go (spend a couple of minutes exploring what the group learned). Repeat, but this time make sure whoever didn't have access to the keyboard now do.

### At the end:

* **Wrap it up**. Ask for comments, questions, learning experiences. Remember to keep it within the agreed time. People will not come next time if you are not disciplined to finished on time.

# 3 Laws of TDD

* Don't write any code unless you are making a failing test pass
* Don't add to the test more than enough to get a failure
* Only write enough code to make the one failing test to pass

# 4 Rules of Simple Design

* All tests must run and pass
* Contains no duplication
* Express the intent of the programmer
* Minimise number of classes and methods

## Object Oriented katas
- [BlogWebApp Kata](https://github.com/jplebre/KataCollection/blob/master/Specifications/BlogWebApp.md), from [Colleen Kirtland TDD Problems Blog](https://sites.google.com/site/tddproblems/all-problems-1)
- [ClamCard Kata](https://github.com/jplebre/KataCollection/blob/master/Specifications/ClamCard.md) - do your own OysterCard system - from [Amiralizazabi](https://github.com/amiralibazazi) available [here](https://gist.github.com/amiralibazazi/a9d57d40886604887d8e#file-clamcardkata-txt-L70);
- [MarsRover Kata](https://github.com/jplebre/KataCollection/blob/master/Specifications/MarsRover.md), from [Amirrajan's Blog](http://amirrajan.net/Blog/)
- [Roll your own Unit Test Framework](https://github.com/jplebre/KataCollection/blob/master/Specifications/RollYourOwnUnitTestFramework.md), from [Jason Gorman's SC2016 backlog](http://codemanship.co.uk/parlezuml/blog/?postid=1346)
- [Roll your own Mock Object framework](https://github.com/jplebre/KataCollection/blob/master/Specifications/RollYourOwnMockObjectFramework.md), from [Jason Gorman's SC2016 backlog](http://codemanship.co.uk/parlezuml/blog/?postid=1355) 
- [SocialNetworkExercise](https://github.com/jplebre/KataCollection/blob/master/Specifications/SocialNetwork.md), from [Franziskas](https://github.com/franziskas) available [here](https://github.com/franziskas/social-network-exercise)
- [Towers vs Jelly](https://github.com/jplebre/KataCollection/blob/master/Specifications/JellyVsTower.md), inspired on a mobile game.
- [TransferSmart](https://github.com/jplebre/KataCollection/blob/master/Specifications/TransferSmart.md) - a money transfer system.
- [VendingMachine Kata](https://github.com/jplebre/KataCollection/blob/master/Specifications/VendingMachine.md), from [Amirrajan's Blog](http://amirrajan.net/Blog/)
- [VideoClubRental Kata](https://github.com/jplebre/KataCollection/blob/master/Specifications/VideoClubRental.md), from Jason Gorman's [TDD workshops](http://www.codemanship.co.uk/)


## Algorithms and Tools Katas
- [BinaryChop Kata](https://github.com/jplebre/KataCollection/blob/master/Specifications/BinaryChop.md) - a binary search routine - from [KodeKata.com](www.codekata.com)
- [CodeBreaker](https://github.com/jplebre/KataCollection/blob/master/Specifications/CodeBreaker.md) - did you guess the string?  
- [Conway's Game of Life](https://github.com/jplebre/KataCollection/blob/master/Specifications/ConwayGameOfLife.md) Kata, from [Amirrajan's Blog](http://amirrajan.net/Blog/) and [Wikipedia](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life) 
- [HowBigHowFast Kata](https://github.com/jplebre/KataCollection/blob/master/Specifications/HowBigHowFast.md) - calculating size and time requirements to process information - from [KodeKata.com](www.codekata.com)  
- [NumbersToWords](https://github.com/jplebre/KataCollection/blob/master/Specifications/NumbersToWords.md)
- [RomanCalculator](https://github.com/jplebre/KataCollection/blob/master/Specifications/RomanCalculator.md)
- [StringCalculator](https://github.com/jplebre/KataCollection/blob/master/Specifications/StringCalculator.md)

## TDD Kata
- [ArgumentParser](https://github.com/jplebre/KataCollection/blob/master/Specifications/ArgumentParser.md) - creating CLI flags;
- [BowlingKata](https://github.com/jplebre/KataCollection/blob/master/Specifications/BowlingKata.md) - simulate a bowling game;
- [FizzBuzz](https://github.com/jplebre/KataCollection/blob/master/Specifications/FizzBuzz.md) - a simple social game;
- [Fibonnacci Sequence Generator](https://github.com/jplebre/KataCollection/blob/master/Specifications/FibonacciSequence.md) - create a program that outputs the Fibonnacci sequence;
- [KataPotter](https://github.com/jplebre/KataCollection/blob/master/Specifications/KataPotter.md) - calculating discount for bestselling book franchises - from [codingdojo.org](http://codingdojo.org/)
- [PrimeFactors](https://github.com/jplebre/KataCollection/blob/master/Specifications/PrimeFactors.md) Kata, from [Amirrajan's Blog](http://amirrajan.net/Blog/)  
- [SuperMarket](https://github.com/jplebre/KataCollection/blob/master/Specifications/SupermaketSimplified.md) simplified version kata, from [7Digital Kata Collection](https://github.com/7digital/kata-checkout) adapted from [Dave Thomans Kode Kata](http://codekata.com/kata/kata09-back-to-the-checkout)  
- [ZombieSurvivor](https://github.com/jplebre/KataCollection/blob/master/Specifications/ZombieSurvivor.md)


## Multi-Thread Kata
- [Multi-Threaded Santa Challenge](https://github.com/jplebre/KataCollection/blob/master/Specifications/MultiThreadedSanta.md) - a brilliant funny competition by [Jason Gorman](http://codemanship.co.uk/parlezuml/blog/?postid=1337)
