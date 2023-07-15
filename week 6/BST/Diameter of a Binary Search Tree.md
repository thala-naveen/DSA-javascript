## Problem Statement:
Diameter of a Binary Search Tree

## Problem Statement:
Given a binary search tree (BST), write a function to find the diameter of the tree. The diameter of a binary tree is defined as the length of the longest path between any two nodes in the tree.

## Input Format:
The user will be prompted to enter the elements of the BST, separated by spaces.

## Output Format:
The value of the lowest common ancestor of the two nodesThe diameter of the BST will be printed.

## Test Case 1:
Sample Input:
4 2 6 1 3 5 7

Sample Output:
4

Input and Output Explanation:
The BST is constructed with the elements [4, 2, 6, 1, 3, 5, 7]. The longest path between any two nodes in the tree is from node 1 to node 7, which has a length of 4. Therefore, the diameter of the BST is 4.


Sample Output:
The lowest common ancestor of nodes 5 and 1 is 3.


## Test Case 2:
Sample Input:
8 4 12 2 6 10 14

Sample Output:
5

Input and Output Explanation:
The BST is constructed with the elements [8, 4, 12, 2, 6, 10, 14]. The longest path between any two nodes in the tree is from node 2 to node 10, which has a length of 5. Therefore, the diameter of the BST is 5.

## Level: Easy

## Hints:
- The diameter of a binary tree can be calculated using the heights of its left and right subtrees.
- The longest path between any two nodes can be found by calculating the height of each node's left and right subtrees and taking their sum.

## Approach:
- Create a class TreeNode with properties val, left, and right to represent a node in the BST.
- Create a function insertNode to insert a new node in the BST.
- Create a function getHeight to calculate the height of a node.
- If the node is null, return 0.
- Otherwise, return the maximum height of its left and right subtrees, plus 1.
- Create a function diameter to find the diameter of the BST.
- If the node is null, return 0.
- Calculate the height of the left subtree and store it in the variable leftHeight.
- Calculate the height of the right subtree and store it in the variable rightHeight.
- Calculate the diameter of the left subtree recursively using the diameter function and store it in the variable leftDiameter.
- Calculate the diameter of the right subtree recursively using the diameter function and store it in the variable rightDiameter.
- Return the maximum value among leftHeight + rightHeight + 1, leftDiameter, and rightDiameter.
- Call the diameter function on the root node of the BST.
