## Problem Statement:
Minimum Jumps with Dynamic Programming

## Problem Statement:
Given an array of integers where each element represents the maximum number of steps that can be jumped going forward from that element, write a function to find the minimum number of jumps required to reach the end of the array, starting from the first element.

## Input Format:
The input consists of a single line containing space-separated integers representing the elements of the array.


## Output Format:
The output is a single line containing an integer representing the minimum number of jumps required.


## Test Case 1:
Sample Input:
2 3 1 1 4

Sample Output:
3

Explanation:
In the given sample input, the array is [2, 3, 1, 1, 4].
By taking 2 jumps (from index 0 to index 1 and from index 1 to index 4), we can reach the end of the array.
Therefore, the minimum number of jumps required is 2.

## Test Case 2:
Sample Input:
5 4 3 2 1

Sample Output:
-1


## Level: Medium

## Hints:
- Use dynamic programming to solve the problem efficiently.
Create an array jumps of the same length as the input array to store the minimum jumps required to reach each index.
Initialize jumps[0] to 0.
Consider using a 2D array to store the maximum values for different combinations of items and knapsack weights.
- Iterate through each index of the array starting from the second index.
For each index, iterate through all the previous indices.
If the previous index plus its value is greater than or equal to the current index and the number of jumps required to reach the previous index is not Infinity, update jumps[i] with the minimum of its current value and the number of jumps required to reach the previous index plus 1.
Return jumps[n-1] if it is not Infinity, otherwise return -1.

## Approach:
- Initialize the array jumps with length n, where n is the length of the input array.
- If the length of the array is less than or equal to 1, return 0.
- If the first element of the array is 0, return -1 since it is not possible to make any jumps.
- Initialize jumps[0] to 0.
- Iterate through each index of the array starting from the second index.
- For each index, iterate through all the previous indices.
- Check if the previous index plus its value is greater than or equal to the current index and the number of jumps required to reach the previous index is not Infinity.
- If the condition is satisfied, update jumps[i] with the minimum of its current value and the number of jumps required to reach the previous index plus 1.
- After iterating through all the indices, check if jumps[n-1] is not Infinity. If it is not, return jumps[n-1], otherwise return -1.
