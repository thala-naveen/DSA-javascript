## Problem Name:
Reverse Linked List

## Problem Statement:
Given a singly linked list, write a function to reverse the list.


## Input Format:
The user will be prompted to enter the elements of the linked list, separated by spaces.

## Output Format:
The reversed linked list will be printed.


## Test Case 1:
Sample Input:
1 2 3 4 5

Sample Output:
5 -> 4 -> 3 -> 2 -> 1

Input and Output Explanation:
The given linked list [1 -> 2 -> 3 -> 4 -> 5] is reversed to [5 -> 4 -> 3 -> 2 -> 1].


## Test Case 2:
Sample Input:
10 20 30 40 50

Sample Output:
50 -> 40 -> 30 -> 20 -> 10

## Level: Hard

## Hints:
- Use three pointers to keep track of the current, previous, and next nodes.

- Iterate through the linked list and update the pointers accordingly.
Take care of handling the first and last nodes of the list.

## Approach:
- Initialize three pointers: current pointing to the head of the list, previous initially set to null, and next pointing to null.
- Iterate through the list:
- Update next to the next node of the current node.
- Set the next pointer of the current node to the previous node.
- Update previous to the current node.
- Update current to the next node.
- Finally, update the head of the list to the last node visited, which will be the previous node.
- Print the reversed linked list.