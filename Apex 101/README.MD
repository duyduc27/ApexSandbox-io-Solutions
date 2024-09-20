# ApexSandbox io solutions

Duc just wants to solve some puzzles.

## Apex 101
### Teenager
https://www.apexsandbox.io/problem/18

Given a person's age, return  `true`  if the person is a teenager (age 13 - 19).

`isTeenager(5) = false`

`isTeenager(15) = true`

### Number Difference
https://www.apexsandbox.io/problem/4

Implement a function  `diff`  that calculates the absolute difference between two integers.

`diff(5, 2) = 3`

`diff(2, 5) = 3`

### Sum Equals
https://www.apexsandbox.io/problem/14

Given Integers  `a`,  `b`, and  `c`, return  `true`  if  `a`  and  `b`  add up to  `c`.

`sumEquals(5, 5, 10) = true`

`sumEquals(2, 8, 9) = false`

### Ascending Order
https://www.apexsandbox.io/problem/20

Given three Integers  `a`,  `b`, and  `c`, return  `true`  if they are in ascending order. For our purposes, two equal numbers will be considered to be in an ascending order.

`ascendingOrder(10, 10, 15) = true`

`ascendingOrder(15, 14, 13) = false`

### A or An
https://www.apexsandbox.io/problem/21

Given a work, prepend it with the correct indefinite article ("a" or "an") followed by a space based on the following rule: words starting with a vowel (a, e, i, o, or u) are prepended with "an", while words starting with any other letter are prepended with "a".

`aOrAn('apple') = 'an apple'`

`aOrAn('banana') = 'a banana'`

### Largest of Three
https://www.apexsandbox.io/problem/3

Given three Integers, return the largest

### Tip Calculator
https://www.apexsandbox.io/problem/137

Create a function that given a total bill, and an integer percentage value between 0 and 100, computes the tip at the specified percentage. You can assume the percentage specified will be an integer within the valid range.

For an example,  `computeTip(200.0, 50)`  evaluates to  `100.0`, because 50% of 200 is 100.

### Passing Students
https://www.apexsandbox.io/problem/19

A student passes a course if  any  **two**  of the following three_  conditions are true: they have passed the exam, they have passed assignments, and they have passed the course project.

Implement the function  `isPassed`  that takes in three parameters  `passedExam`,  `passedAssignments`, and  `passedProject`, and returns  `true`  of at least two of the passed variables are true.

`isPassed(true, false, true) = true`. Student did not pass assignments, but passes overall because they passed the exam and the project.

`isPassed(false, false, true) = false`. Student only passed the project, and therefore does not pass overall.

### Ends With 0
https://www.apexsandbox.io/problem/90

Given an integer, return  `true`  if the integer ends with 0, otherwise return  `false`.

`isEndWithZero(12) == false`

`isEndWithZero(1230) == true`

### Which Two
https://www.apexsandbox.io/problem/15

Given Integers  `a`,  `b`, and  `c`, determine if any two of them add up to the third and return  `'a'`,  `'b'`,  `'c'`  depending on which the sum is. If no two numbers add up to a third number, return an empty string. Assume that multiple solutions do not exist.

`whichTwo(5, 10, 5) = 'b'`

`whichTwo(2, 0, 3) = ''`

### Even or Odd
https://www.apexsandbox.io/problem/5

Given an Integer, return  `'even'`  if the Integer is even, or  `'odd'`  if the Integer is odd. Remember to use the  `Math.mod`  function.

`evenOrOdd(15) = 'odd'`

`evenOrOdd(-64) = 'even'`

### Rock Paper Scissors
https://www.apexsandbox.io/problem/12

Rock beats scissors, scissors beats paper, paper beats rock. Implement the method  `rockPaperScissors`  that takes as parameters two strings  `player1`  and  `player2`  representing the moves played by player 1 and player 2, valid moves being  `'rock'`,  `'paper'`, and  `'scissors'`. Return 1 if player 1 wins, 2 if player 2 wins, and 0 if no one wins.

`rockPaperScissors('rock', 'paper') = 2`

`rockPaperScissors('scissors', 'paper') = 1`

`rockPaperScissors('paper', 'paper') = 0`

### Age Group
https://www.apexsandbox.io/problem/17

Given a person's age, return their age group as a string: 'Infant' for ages 0-1, 'Child' for ages 2 - 14, 'Youth' for ages 15 - 21, and 'Adult' for ages 22+.

`ageGroup(5) = 'Child'`

`ageGroup(15) = 'Youth'`

### Companion Plants
https://www.apexsandbox.io/problem/54

Some plants are considered companion plants. They grow better when planted next to each other. For the purpose of this problem, we consider the following plants to be companions: lettuce and cucumbers, lettuce and onions, onions and carrots, and onions and tomatoes.

Write a function  `isCompanion`  that takes as input two strings  `plant1`  and  `plant2`. If the two plants are companion plants based on the criteria described above, return true. Otherwise, return false.

`companionPlants('onions', 'lettuce') = true`

`companionPlants('lettuce', 'tomatoes') = false`

### Leap Year
https://www.apexsandbox.io/problem/6

A year is considered a leap year if it is evenly divisible by 4, with the exception of years that are also evenly divisible by 100. Years evenly divisible by 100 must also be evenly evenly divisible by 400 to by considered leap years. Implement a method  `isLeapYear`  that takes as input an Integer  `year`  and returns  `true`  if the year is a leap year, and  `false`  otherwise.

`isLeapYear(1900) = false`. Year 1900 is evenly divisible by 4, but it is also evenly divisible by 100 which means it additionally needs to be evenly divisible by 400 to qualify as a leap year. 1900 is not evenly divisible by 400.

`isLeapYear(2000) = true`. Year 2000 is evenly divisible by 4. It is also evenly divisibly by 100, which means it additionally needs to be evenly divisible by 400, which it is. Therefore, it is a leap year.

`isLeapYear(2004) = true`. Year 2004 is evenly divisible by 4. It is not divisible by 100, and therefore a leap year.

`isLeapYear(1933) = false`. Year 1933 is not evenly divisible by 4, and therefore not a leap year.

### Prime Number
https://www.apexsandbox.io/problem/7

A prime number is a number greater than 1 that is not evenly divisible by any number greater than one and smaller than itself. For example, 13 is a prime number because it is not evenly divisible by any number between 1 and 13.

Implement the function  `isPrime`  that takes as input an integer greater than 1, returns  `true`  if the integer is a prime number, and returns  `false`  otherwise. Assume that the input will always be greater than 1.

`isPrime(10) = false`. 10 is not a prime number because it is evenly divisible by 2 and 5.

`isPrime(23) = true`. 23 is a prime number because it is not evenly divisible by any number from 2 to 22.

### Sum 1 to N
https://www.apexsandbox.io/problem/16

Implement the method  `sumToN`  that calculates and returns the sum of all numbers (inclusive) from 1 to  `n`. Assume that  `n`  will be non-zero positive integer.

`sumToN(5) = 15`

`sumToN(2) = 3`

### Full Name
https://www.apexsandbox.io/problem/9

Given two non-empty strings  `firstName`  and  `lastName`, return the name as a single string with a space in between (`firstName lastName`).

`formatName('Jane', 'Doe') = 'Jane Doe'`

### Format Name
https://www.apexsandbox.io/problem/10

Given two strings  `firstName`  and  `lastName`, return the name in the format LastName, FirstName. In case one of the names is null or empty, return only the non-empty part of the name. If both are null or empty, return an empty string.

`formatName('Jane', 'Doe') = 'Doe, Jane'`

`formatName('Jane', '') = 'Jane'`

### Name from Email
https://www.apexsandbox.io/problem/11

Implement a function  `nameFromEmail`  that takes as input a valid email address in the format  `firstname.lastname@example.com`. The function should extract the first name and last name from this email address and return a capitalized full name (i.e. FirstName LastName). Assume that the input will always be a valid email address with both the first name and last name separated by a period (.).

`nameFromEmail('john.doe@apexsandbox.io') = 'John Doe'`

`nameFromEmail('JANE.DOE@GMAIL.COM') = 'Jane Doe'`

### Change Time Format
https://www.apexsandbox.io/problem/79

`13:50`  and  `01:50 PM`  are 24-hour and 12-hour representations of the same time. Implement the method  `changeTimeFormat`  that takes as input a string  `strTime`  formatted as a 24-hour string, and returns the equivalent 12-hour string.

Examples:

`changeTimeFormat('08:05')`  returns  `'08:05 AM'`

`changeTimeFormat('00:05')`  returns  `'12:05 AM'`

`changeTimeFormat('23:15')`  returns  `'11:15 PM'`

### Fibonacci
https://www.apexsandbox.io/problem/13

The first two numbers in the fibonacci sequence are 1, and all other numbers in the sequence are defined as the sum of the last two fibonacci numbers. The first 10 numbers in the fibonacci sequence are 1, 1, 2, 3, 5, 8, 13, 21, 34, and 55.

Implement the function  `fibonacci`  that takes as input an Integer  `n`  and returns the  _nth_  fibonacci number. Assume that  `n`  will always be greater than 0.

`fibonacci(1) = 1`

`fibonacci(2) = 1`

`fibonacci(5) = 5`

### Next Prime
https://www.apexsandbox.io/problem/8

A prime number is a number greater than 1 that is not evenly divisible by any number greater than one and smaller than itself. For example, 13 is a prime number because it is not evenly divisible by any number from 2 to 12.

Implement the function  `nextPrime`  that takes as input an integer  `num`  and returns the smallest prime number greater than  `num`.

`nextPrime(10) = 11`. 11 is the smallest prime number greater than 10

`nextPrime(8) = 11`. 11 is the smallest prime number greater than 8

### Reverse Order of Words
https://www.apexsandbox.io/problem/113

Implement a function  `reverseWordsInASentence`  that will take a String containing words separated by spaces as an argument, and return a string with the order of the words reversed.

Example : If the sentence is  **The quick brown fox jumps over the lazy dog**, then  `reverseWordsInASentence(String sentence)`  should evaluate to  **dog lazy the over jumps fox brown quick The**