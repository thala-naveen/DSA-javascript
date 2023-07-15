## Problem Statement:
Floyd Warshall Algorithm

## Problem Statement:
Given a weighted directed graph, find the shortest distance between all pairs of vertices.

## Input Format:
- The number of vertices (n) in the graph.
- The number of edges (m) in the graph.
- For each edge, the source vertex, destination vertex, and edge weight are provided.

## Output Format:
The shortest distance matrix, representing the minimum distance between all pairs of vertices.

## Test Case 1:
Sample Output:
4
5
0 1 3
0 2 8
1 0 2
2 3 2
3 1 1

Sample Output:
0 3 5 Infinity
2 0 4 Infinity
Infinity Infinity 0 2
Infinity 1 Infinity 0

Explanation:
In the given sample, the graph has 4 vertices and 5 edges.
The shortest distance matrix represents the minimum distance between each pair of vertices.
For example, the shortest distance from vertex 0 to vertex 2 is 5, and the shortest distance from vertex 3 to vertex 1 is 1.
The "Infinity" value represents that there is no direct path between the vertices.

## Test Case 2:
Sample Output:
2
1
0 1 3

Sample Output:
0 3
Infinity 0

Explanation:
The shortest distance matrix represents the minimum distance between each pair of vertices.

## Level: Hard

## Hints:
- The Floyd Warshall algorithm computes the shortest distance between all pairs of vertices in a graph.
Initialize the distance matrix with the direct edge weights between vertices. Set the distance between non-connected vertices as "Infinity".
For each intermediate vertex k, update the distance matrix by considering the possibility of going through vertex k to reach the destination vertex.
- Repeat the above step for all vertices as intermediate vertices.
The final distance matrix represents the shortest distance between all pairs of vertices in the graph.

## Approach:
- Initialize the distance matrix with direct edge weights and set the distance between non-connected vertices as "Infinity".
- For each vertex k from 0 to n-1, iterate over all pairs of vertices i and j.
- Update the distance between vertices i and j by considering the possibility of going through vertex k.
- After the iteration, the distance matrix will represent the shortest distance between all pairs of vertices.
- Return the distance matrix as the output.
