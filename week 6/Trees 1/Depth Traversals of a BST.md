## Problem Statement:
Depth Traversals of a BST

## Problem Statement:
Given a binary search tree (BST), write a function to print all three depth traversals: Inorder, Postorder, and Preorder.

## Input Format:
The user will be prompted to enter the elements of the BST, separated by spaces.


## Output Format:
The three depth traversals, Inorder, Postorder, and Preorder, will be printed.

## Test Case 1:
Sample Input:
4 2 6 1 3 5 7

Sample Output:
Inorder traversal: 1 2 3 4 5 6 7
Postorder traversal: 1 3 2 5 7 6 4
Preorder traversal: 4 2 1 3 6 5 7

Input and Output Explanation:
The BST is constructed with the elements [4, 2, 6, 1, 3, 5, 7]. The depth traversals are as follows:

Inorder traversal: Traverse the left subtree, visit the root, traverse the right subtree. (1 2 3 4 5 6 7)
Postorder traversal: Traverse the left subtree, traverse the right subtree, visit the root. (1 3 2 5 7 6 4)
Preorder traversal: Visit the root, traverse the left subtree, traverse the right subtree. (4 2 1 3 6 5 7)


## Test Case 2:
Sample Input:
5 3 8 2 4 7 9

Sample Output:
Inorder traversal: 2 3 4 5 7 8 9
Postorder traversal: 2 4 3 7 9 8 5
Preorder traversal: 5 3 2 4 8 7 9

Input and Output Explanation:
The BST is constructed with the elements [5, 3, 8, 2, 4, 7, 9]. The depth traversals are as explained earlier.


## Level: Hard

## Hints:
- Depth traversals are common ways to visit the nodes of a binary tree.
Implement recursive functions for each traversal type.
- Use the BST properties to determine the order of traversing the left and right subtrees.

## Approach:
- Define three functions for each depth traversal type: inorder, postorder, and preorder.
- For each traversal type:
- Traverse the left subtree recursively.
- Visit the root node.
- Traverse the right subtree recursively.
- Call the three functions to print the depth traversals.