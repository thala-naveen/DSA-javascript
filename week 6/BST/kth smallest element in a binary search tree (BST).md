## Problem Statement:
kth smallest element in a binary search tree (BST)

## Problem Statement:
Write a function to find the kth smallest element in a Binary Search Tree (BST)


## Input Format:
The number of elements in the binary search tree (integer)
The elements of the binary search tree (space-separated integers)
The value of k (integer)

## Output Format:
The kth smallest element in the binary search tree (integer)

## Test Case 1:
Sample Input:
- 7
- 4 2 6 1 3 5 7
- 3

Sample Output:
3

## Test Case 2:
sample input: 
- 5
- 10 7 15 5 12
- 1

sample output:
5


## Level: Hard

## Hints:
- Perform an in-order traversal of the binary search tree to get the elements in sorted order.
- Keep track of the count of visited nodes while traversing the tree.
When the count becomes equal to k, return the current node's value.

## Approach:
- Use an iterative in-order traversal using a stack to simulate the recursion.
- Keep a count variable to track the number of visited nodes.
- When the count becomes equal to k, return the value of the current node.
- If the count exceeds k, terminate the traversal and return -1 as the tree does not have k elements.
