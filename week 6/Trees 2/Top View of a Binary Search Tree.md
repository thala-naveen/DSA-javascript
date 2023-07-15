## Problem Statement:
Top View of a Binary Search Tree

## Problem Statement:
Given a binary search tree (BST), write a function to print the top view of the tree. The top view of a tree is defined as the nodes visible when viewed from the top, considering only the vertical order of the nodes.


## Input Format:
- The user will be prompted to enter the elements of the BST, separated by spaces.

## Output Format:
The top view of the BST will be printed.

## Test Case 1:
Sample Input:
Enter the elements of the BST: 4 2 6 1 3 5 7

Sample Output:
Top view of the BST: 1 2 4 6 7

Input and Output Explanation:
The BST is constructed with the elements [4, 2, 6, 1, 3, 5, 7]. The top view of the tree is the nodes visible from the top, considering the vertical order. In this case, the top view is 1 2 4 6 7.


## Test Case 2:
Sample Input:
Enter the elements of the BST:  8 4 12 2 6 10 14

Sample Output:
Top view of the BST: 2 4 8 12 14

Input and Output Explanation:
The BST is constructed with the elements [8, 4, 12, 2, 6, 10, 14]. The top view of the tree is the nodes visible from the top, considering the vertical order. In this case, the top view is 2 4 8 12 14.

## Level: Easy

## Hints:
- The top view of a tree can be obtained using a vertical order traversal.
Maintain a vertical level for each node and track the leftmost and rightmost node at each level.
- Traverse the tree in a level order manner and keep track of the vertical level and the leftmost and rightmost node at each level.

## Approach:
- Create a class TreeNode with properties val, left, and right to represent a node in the BST.
- Create a function insertNode to insert a new node in the BST.
- Create a function topView to print the top view of the BST.
- Initialize an empty object verticalLines to store the nodes at each vertical level.
- Create a queue queue to perform a level order traversal.
- Enqueue the root node along with its vertical level 0 into the queue.
- Perform a level order traversal using the queue:
- Dequeue a node and its vertical level from the queue.
- If the current vertical level is not present in verticalLines, add the node to verticalLines at the current vertical level.
- Enqueue the left child of the dequeued node with a vertical level one less than the current level.
- Enqueue the right child of the dequeued node with a vertical level one more than the current level.
- Print the nodes from the leftmost to the rightmost in each vertical level.
- Call the topView function on the root node of the BST.
