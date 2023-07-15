## Problem Name:
Aggressive Cows

## Problem Statement:
You have to place C cows in N stalls, where the stalls are arranged in a line. Each stall can have at most one cow. The goal is to minimize the largest distance between any two cows. Determine the maximum possible distance that can be achieved.


## Input Format:
- The first line of input contains the number of stalls, N.
- The second line of input contains the number of cows, C.
- The next N lines of input contain the positions of the stalls.

## Output Format:
The output is a single integer representing the maximum possible distance between any two cows.

## Test Case 1:
Sample Input:
- 5
- 3
- 1
2
8
4
9

Sample Output:
3

Exp:
In the given sample case, there are 5 stalls and 3 cows. The stalls are located at positions 1, 2, 8, 4, and 9. The cows can be placed in the stalls as follows:

Place a cow in stall 1 (position 1).
Place a cow in stall 4 (position 4).
Place a cow in stall 8 (position 8).
The maximum distance between any two cows is 3, which is achieved by placing the cows in stalls at positions 1, 4, and 8.

## Test Case 2:
Sample input:
- 3
- 3
- 5
10
15

Sample output:
5   

## Level: Easy

## Hints:
- Use binary search to find the maximum possible distance.

- Define a function to check if it is possible to place the cows with a given distance between them

## Approach:
- Sort the stall positions in ascending order.
- Set the left pointer to the minimum stall position and the right pointer to the maximum stall position.
- Perform binary search on the range between the left and right pointers.
- In each iteration of binary search, calculate the mid position.
- Use a greedy approach to place the cows:
- Start with the first stall and place a cow in it.
- Iterate through the remaining stalls and place cows in the stalls with a distance greater than or equal to the mid - position.
- Keep track of the count of placed cows.
- If the count of placed cows is equal to or greater than the required number of cows, update the left pointer to the mid position.
- If the count of placed cows is less than the required number of cows, update the right pointer to the mid position.
- Repeat steps 3-7 until the left and right pointers converge.
- The final value of the left pointer represents the maximum possible distance between any two cows. Return this value.