## Problem Name:
Spiral Order Traversal in Array

## Problem Statement:
Given a 2D array of integers, implement an algorithm to print its elements in spiral order.



## Input Format:
The input should be taken from the user as a prompt. 
- Line 1 - number of rows
- Line 2 - number of columns
- Line 3 - The input should be a 2D array represented as a string, where each row is separated by a newline character ('\n') and each element in a row is separated by a space.

## Output Format:
The output will be a string representing the elements of the array in spiral order, separated by a space.

## Test Case 1:
Sample Input:
3
3
1 2 3
4 5 6
7 8 9

Sample Output
1 2 3 6 9 8 7 4 5

Explanation:
The output is the elements of the array printed in spiral order: 1 2 3 6 9 8 7 4 5. The elements are traversed in the following order: top row from left to right, right column from top to bottom, bottom row from right to left, and left column from bottom to top.

## Test Case 2:
Sample input:
4
1
1
2
3
4


Sample output:
1 2 3 4

Explanation:
The input represents a 4x1 matrix. The elements are traversed in spiral order: top row (1) -> right column (2) -> bottom row (3) -> left column (4).

## Level: Medium

## Hints:
- Consider using four pointers to keep track of the boundaries of the spiral.
Start with the top-left corner as the starting point.

- Iterate through the top row, right column, bottom row, and left column in a clockwise direction.
Adjust the boundaries of the spiral after each iteration.




## Approach:
- Parse the input string to create a 2D array.
- Initialize four pointers: top, bottom, left, and right, to keep track of the boundaries of the spiral.
- Use a while loop to traverse the elements in spiral order:
- a. Iterate from left to right, incrementing the top pointer.
- b. Iterate from top to bottom, incrementing the left pointer.
- c. Iterate from right to left, decrementing the bottom pointer.
- d. Iterate from bottom to top, decrementing the right pointer.
- Append the traversed elements to a result array.
- Join the elements of the result array with a space and return the result as the output.
