## Problem Statement:
0/1 Knapsack

## Problem Statement:
Given a list of items, each with a weight and a value, and a maximum weight capacity of a knapsack, write a function to determine the maximum value that can be obtained by selecting items in such a way that the total weight does not exceed the knapsack capacity.

## Input Format:
The user will be prompted to enter the number of items and the maximum weight capacity of the knapsack.
Then, for each item, the user will be prompted to enter its weight and value, separated by spaces.


## Output Format:
The maximum value that can be obtained from the items will be printed.


## Test Case 1:
Sample Input:
4
5
2 3
1 2
3 4
2 2

Sample Output:
7

Input and Output Explanation:
In this example, there are 4 items and the maximum weight capacity of the knapsack is 5.

Item 1 has a weight of 2 and a value of 3.
Item 2 has a weight of 1 and a value of 2.
Item 3 has a weight of 3 and a value of 4.
Item 4 has a weight of 2 and a value of 2.
The goal is to maximize the total value of the selected items without exceeding the knapsack capacity.
By selecting item 2 (weight: 1, value: 2) and item 4 (weight: 2, value: 2), the total weight is 1 + 2 = 3 and the total value is 2 + 2 = 4, which is the maximum value that can be obtained.

## Test Case 2:
Sample Input:
3
10
5 10
4 40
6 30

Sample Output:
70

Input and Output Explanation:
By selecting all three items, we can achieve the maximum value of 70

## Level: Medium

## Hints:
- This problem can be solved using Dynamic Programming.
Consider using a 2D array to store the maximum values for different combinations of items and knapsack weights.
- Start with a base case and build the solution incrementally by considering each item.

## Approach:
- Prompt the user to enter the number of items and the maximum weight capacity of the knapsack.
- Create two arrays, one for the weights of the items and another for the values of the items.
- Create a 2D array of size (number of items + 1) x (knapsack capacity + 1) to store the maximum values.
- Initialize the first row and column of the 2D array to 0, as there are no items or knapsack capacity.
- Iterate through each item and knapsack weight combination:
- If the weight of the current item is less than or equal to the current knapsack weight, consider including the item in the knapsack.
- Calculate the value that can be obtained by including the item, which is the sum of the value of the current item and the maximum - value for the remaining weight (current knapsack weight - item weight) from the previous row in the 2D array.
- Compare this value with the maximum value obtained so far for the same knapsack weight without including the current item, and store the maximum value in the 2D array.
- If the weight of the current item is greater than the current knapsack weight, the item cannot be included, so the maximum value remains the same as the maximum value for the same knapsack weight without including the current item from the previous row.
- The maximum value that can be obtained is stored in the last cell of the 2D array.
- Print the maximum value.
