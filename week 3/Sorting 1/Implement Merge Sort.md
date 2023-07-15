## Problem Statement:
Implement Merge Sort

## Problem Statement:
Implement the Merge Sort algorithm to sort an array of numbers in ascending order.


## Input Format:
The input should be taken from the user using the prompt. The user should provide a space-separated list of numbers.

## Output Format:
The output will be the sorted array of numbers, displayed as a comma-separated list.

## Test Case 1:
Sample Input:
Enter the numbers: 8 3 1 7 5

Sample Output:
Sorted array: 1, 3, 5, 7, 8

Explanation:
The input array [8, 3, 1, 7, 5] is sorted using the Merge Sort algorithm, resulting in the output [1, 3, 5, 7, 8].


## Test Case 2:
Sample Input:
Enter the numbers: 5 2 9 1 6

Sample Output:
Sorted array: 1, 2, 5, 6, 9

## Level: Easy

## Hints:
- Merge Sort is a divide-and-conquer algorithm that divides the array into two halves, sorts them separately, and then merges them back together.
- The base case of the recursion is when the array has only one element, which is considered sorted.
The merge step involves comparing elements from the two sorted halves and merging them into a single sorted array.

## Approach:
- Implement a function mergeSort(arr) that takes an array as input.
- Base case: If the array length is less than or equal to 1, return the array as it is already sorted.
- Divide the array into two halves: left and right.
- Recursively call mergeSort on both halves to sort them.
- Merge the sorted left and right halves using a merge function.
- Return the merged array as the final sorted result.
