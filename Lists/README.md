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
