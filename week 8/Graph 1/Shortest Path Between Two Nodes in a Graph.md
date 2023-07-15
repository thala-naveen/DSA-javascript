## Problem Statement:
Shortest Path Between Two Nodes in a Graph

## Problem Statement:
Given an undirected graph and two nodes, find the shortest path between the two nodes.

## Input Format:
The user will provide the number of nodes in the graph and the number of edges.
Then, the user will provide the details of each edge (node1, node2) representing an edge between the two nodes.
Finally, the user will provide the two nodes for which the shortest path is to be found.

## Output Format:
The output will be the shortest path between the two nodes.
If there is no path between the two nodes, the output will indicate that there is no path.


## Test Case 1:
Sample Input:
6
8
0 1
0 2
1 2
1 3
2 3
2 4
3 4
4 5
0
5

Sample Output:
0 -> 2 -> 4 -> 5

Input and Output Explanation:
In the given input, there are 6 nodes and 8 edges in the graph.
The edge details are provided, including the nodes that form an edge.
The source node is 0 and the destination node is 5.
The output shows the shortest path from node 0 to node 5, which is 0 -> 2 -> 4 -> 5.

## Test Case 2:
sample input: 
5
6
0 1
0 2
1 3
2 3
2 4
3 4
0
4

sample output:
0 -> 2 -> 4

Input and Output Explanation:
The graph has 5 nodes and 6 edges. The shortest path from node 0 to node 4 is 0 -> 2 -> 4.

## Level: Hard

## Hints:
- The problem can be solved using graph traversal algorithms such as Breadth-First Search (BFS) or Depth-First Search (DFS).
BFS is commonly used to find the shortest path in unweighted graphs.
- Consider using a queue or stack data structure to perform the traversal and keep track of visited nodes and the path.
Take care of handling cases where there is no path between the given nodes.

## Approach:
- Create a graph representation based on the provided input, including nodes and edges.
- Implement Breadth-First Search (BFS) or Depth-First Search (DFS) to find the shortest path between the source and destination nodes.
- Keep track of visited nodes and the path from the source to the current node while traversing the graph.
- Once the destination node is reached, backtrack from the destination to the source using the recorded path to obtain the shortest path.
- If there is no path from the source to the destination, indicate that there is no path in the output.
