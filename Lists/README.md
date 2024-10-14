# ApexSandbox io solutions

Duc just wants to solve some puzzles.

## Lists

### Sorting a List
https://www.apexsandbox.io/problem/92

Implement the method  `getNamesInAscOrder()`, which accepts a list of fullnames as input and returns the list sorted in ascending order. Use the standard library method to sort.

Given the following test code:

`List<String> fullNames = new List<String> { 'Blake Howard', 'Adrienne Copeland'};`

`List<String> result = getNamesInAscOrder(fullNames);`

The expressions  `result[0] == 'Adrienne Copeland', result[1] == 'Blake Howard'`, and  `result.size() == 2`  should be true.

### Array Sum
https://www.apexsandbox.io/problem/1

Implement the method  `arraySum`  that takes as input a non-empty list of Integers  `numbers`, and returns the sum of all numbers in the list.

Example:  `arraySum(new List  {5, 2, 3})`  evaluates to  `10`.

### Count Target in List
https://www.apexsandbox.io/problem/138

Given a list of Integers `nums` and an Integer `target`, count number of times `target` is found in `nums`. If the target is not in the list, simply return 0.

### Last Occurrence
https://www.apexsandbox.io/problem/139

Find the last occurrence of Integer  `target`  in a list of integers  `nums`  and return its index. If the target is not found, return -1

For instance, in the list of integers  `{4, 6, 1, 9, 7, 9, 2}`, the function would return index 0 for the target 4, index 5 for target 9 (occurs twice), and -1 for target 3 (not found).

### Even Numbers
https://www.apexsandbox.io/problem/70

Given a non-zero positive integer  `n`, return a list of the first  `n`  non-zero positive even numbers, ordered ascending.

Example:  `evenNumbers(5)`  returns a list containing the numbers 2, 4, 6, 8, 10.

### Largest Element
https://www.apexsandbox.io/problem/2

Implement the method  `findLargest`  that takes as input a non-empty list of Integers  `nums`, and returns the largest Integer in the list.

Example:  `findLargest(new List  {5, 2, 8, 4, 2, 1})`  evaluates to  `8`  because 8 is the largest Integer in the list.

### Positive Integers
https://www.apexsandbox.io/problem/71

A positive integer is defined as an integer greater than zero. Implement the method  `positiveIntegers`  that takes as input a list of integers  `numbers`, and returns a new list with non-positive integers removed.

Example:  `positiveIntegers(new List  {2, -3, 6, 2})`  returns a list containing the numbers 2, 6, 2.

### Consecutive Ones
https://www.apexsandbox.io/problem/119

Given a List of Integers containing only binary numbers (0 and 1), return the maximum number of consecutive 1s appearing in the List.

**Example :**  **Input:**  `[1,1,0,1,1,1,1]`  **Output:** 4. The array has 2 consecutive 1s starting index 0, and 4 consecutive 1s starting index 3.

### Number Average
https://www.apexsandbox.io/problem/136

Given a list of decimals, return the average rounded to two decimal places.

Example:

`List  numbers = new List{10.5, 20, 45, 89}`

`average(numbers) = 41.12`

The average computes to 41.125, which is rounded to 41.12 using the default "half even" rounding method.