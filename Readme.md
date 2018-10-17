[![Build Status](https://travis-ci.com/StratfordHS-CS2/lab-07-guessing-game-username.svg)](https://travis-ci.com/StratfordHS-CS2/lab-07-guessing-game-username)

# Lab 07 - Guessing Game

## Lab Goal
**This lab is a major grade** that will allow you to demonstrate mastery of many of the concepts we have learned so far.  Those include loops, conditionals, integers, characters, and strings.

## Instructions
You are making a guessing game where you ask the user for the number of digits in the number you are going to guess.  You will come up with a random number of the appropriate length and ask the user to guess the number.  With each guess you will report back to the user how many digits are correct, and how many are in the number, but are in the wrong place.  For example, if the answer is 1234 and the guess is 2243 you would report back that 1 digit is in the correct and 2 digits are in the wrong place.  Once the user guesses the answer correctly you will tell them how many tries it took to win.

The main part of the code will be in the `main` method, but you may write any supporting methods you wish to use.

There are no unit tests for this class, but it still needs to pass Checkstyle.

## Requirements
You must follow these requirements for input/output.  Beyond these you have freedom to make it your own.
* The first input must be the number of digits in the answer number.
* Each input after that must only be the next guess from the user.

## Hints/Tips
* You must account for leading zeros.  For example, 0123 is a valid 4 digit number.
* To force a `double` to be an `int` (dropping the part after the decimal) you can "cast" the `double` to an `int`.  For example,
```
double dnum = 17.5;
int inum = dnum;         // ERROR
```
```
double dnum = 17.5;
int inum = (int)dnum;    // SUCCESS.
```
You have to put the `(int)` before the `double` to tell Java that you really want to make the `double` an `int` even though you're losing precision (something Java tries to protect you from).  This is called "casting".  You cast the `double` to an `int`.
* Make sure you account for numbers appearing in the answer or the guess more than once.

## Relevant ThinkJava Section
* [Strings](http://greenteapress.com/thinkjava6/html/thinkjava6010.html)

## Potentially Helpful Methods or Topics
* Scanner - from `java.util.Scanner`
* `Math.random()`
* `Integer.toString()`
* `Character.toString()`
* `String.trim()` - removes all whitespace from the front and back of the string.
* `String.indexOf()`
* `String.substring()`
* [All String methods](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)
* [All Character methods](https://docs.oracle.com/javase/8/docs/api/java/lang/Character.html)
* [All Integer methods](https://docs.oracle.com/javase/8/docs/api/java/lang/Integer.html)

## Sample Output
```
How many digits? 4
```
(let’s say the computer chose the 4 digit number 4467)
```
Guess the 4 digit number: 1234
You have 0 numbers in the right place and 1 number in the wrong place.
Guess the 4 digit number: 4753
You have 1 number in the right place and 1 number in the wrong place.
Guess the 4 digit number:
```
(continue until…)
```
Guess the 4 digit number: 4467
Congratulations! You have guessed the number!  It took you 37 guesses.
```

## Notes
* The Checkstyle config url is http://www.daveavis.com/cs/checkstyle_SHS.xml
* Make sure you modify the link at the top of your **Readme.md** to reflect your username if you want the badge at the top to represent the status of your code.

## Grading
* 20 - Create the random number with the correct number of digits.
* 25 - Correctly identify how many digits are in the right place.
* 25 - Correctly identify how many digits are in the wrong place.
* 15 - Good output.
* 10 - style
* -15 if leading zeros break your program.

Note that these are potential maximums; the computer can only check so much.  If your code passes Checkstyle, but I see non-descriptive variable names, then your style grade will go down.  If your code passes all tests, but I see code that was copied off of the internet or from another student your grade will go *way* down.
