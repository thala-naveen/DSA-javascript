## Problem Name:
Detect Starting Point of Loop in Linked List

## Problem Statement:
Given a linked list that may contain a loop, write a function to detect and return the starting point of the loop if it exists.


## Input Format:
The user will be prompted to enter the elements of the linked list, separated by spaces.
The user will also be prompted to enter the index (0-based) of the node where the loop starts.

## Output Format:
The starting point of the loop will be printed.

## Test Case 1:
Sample Input:
1 2 3 4 5
2

Sample Output:
3

Input and Output Explanation:
The linked list is created as [1 -> 2 -> 3 -> 4 -> 5], and the loop starts at the node with value 3. Hence, the output is "The starting point of the loop is node with value 3".

## Test Case 2:
Sample input:
1 2 0 2 1

Sample output:
0 1 1 2 2

## Level: Easy

## Hints:
- Use the Floyd's Cycle Detection Algorithm (also known as the "Tortoise and Hare Algorithm") to detect the loop in the linked list.

- After detecting the loop, use two pointers: one starting from the head of the list and another starting from the meeting point of the two pointers.
Move both pointers one step at a time until they meet again. The meeting point will be the starting point of the loop.


## Approach:
- Create a linked list using the input elements.
- Identify the node where the loop starts using the input index.
- Connect the last node of the linked list to the identified node to form a loop.
- Use the Floyd's Cycle Detection Algorithm to detect the loop and find the meeting point.
- Reset one of the pointers to the head of the list and move both pointers one step at a time until they meet again. The meeting point will be the starting point of the loop.
- Print the value of the starting point of the loop.