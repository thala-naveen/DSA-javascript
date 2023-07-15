## Problem Statement:
Minimum Cost of Combining N Ropes

## Problem Statement:
Given an array of lengths representing N ropes, write a function to find the minimum cost of combining all the ropes into a single rope. The cost of combining two ropes is equal to their sum. Find the minimum cost to combine all the ropes into a single rope.


## Input Format:
The user will be prompted to enter the lengths of the N ropes, separated by spaces.


## Output Format:
The minimum cost to combine all the ropes into a single rope will be printed.



## Test Case 1:
Sample Input:
4 3 2 6

Sample Output:
29

Input and Output Explanation:
The lengths of the ropes are [4, 3, 2, 6]. We can combine the ropes as follows:

Combine ropes of length 2 and 3. Cost = 2 + 3 = 5, new lengths = [4, 5, 6].
Combine ropes of length 4 and 5. Cost = 4 + 5 = 9, new lengths = [9, 6].
Combine ropes of length 6 and 9. Cost = 6 + 9 = 15, new lengths = [15].
The minimum cost to combine all the ropes into a single rope is 29.

## Test Case 2:
Sample Input:
1 2 3 4 5

Sample Output:
33

Input and Output Explanation:
The lengths of the ropes are [1, 2, 3, 4, 5]. We combine ropes of length 1 and 2 (cost = 1 + 2 = 3), then combine ropes of length 3 and 3 (cost = 3 + 3 = 6), then combine ropes of length 4 and 5 (cost = 4 + 5 = 9), and finally combine ropes of length 6 and 9 (cost = 6 + 9 = 15). The minimum cost to combine all the ropes into a single rope is 33. 

## Level: Medium

## Hints:
- Think of using a priority queue or a min heap to keep track of the minimum length ropes.
- The smallest ropes should be combined first to minimize the cost.


## Approach:
- Create a priority queue or min heap to store the lengths of the ropes.
- Insert all the rope lengths into the priority queue.
- While the priority queue has more than one rope:
- Extract the two ropes with the smallest lengths from the priority queue.
- Combine the two ropes by adding their lengths.
- Add the combined rope length back to the priority queue.
- Increment the total cost by the sum of the two rope lengths.
- Print the total cost as the minimum cost to combine all the ropes into a single rope.