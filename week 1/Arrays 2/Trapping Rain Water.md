## Problem Name:
Trapping Rain Water

## Problem Statement:
Given an array representing the heights of bars, find the total amount of rainwater that can be trapped between the bars.



## Input Format:
- The first line of input contains the number of bars, N.
- The second line of input contains the heights of the bars separated by spaces.

## Output Format:
The output should be the total amount of rainwater that can be trapped.

## Test Case 1:
Sample Input:
- 8
- 0 1 0 2 1 0 1 3

Sample Output:
- 5

Explanation:
- By analyzing the heights of the bars, we can observe that water can be trapped between the bars at indices 2, 5, and 6. The total amount of trapped rainwater is 5 units.

## Test Case 2:
Sample Input:
- 6
- 3 0 0 2 0 4

Sample Output:
- 20

Explanation:
- Only one unit of water can be trapped between bars at index 2.

## Level: Medium

## Hints:
- To trap rainwater, each bar needs to be bordered by taller bars on both sides.
Calculate the maximum height on the left side and the maximum height on the right side of each bar to determine the amount of water it can trap.

- The amount of water trapped at each bar is the minimum of the maximum heights on both sides minus its own height.

## Approach:
- Initialize variables to keep track of the maximum height on the left and right side.
- Traverse the array from left to right and update the maximum height on the left side for each bar.
- Traverse the array from right to left and update the maximum height on the right side for each bar.
- Traverse the array again and calculate the trapped water for each bar using the minimum of the maximum heights on both sides.
- Sum up the trapped water for all bars and return the total amount of trapped rainwater.
