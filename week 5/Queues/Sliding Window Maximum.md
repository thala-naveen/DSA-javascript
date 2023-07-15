## Problem Name:
Sliding Window Maximum

## Problem Statement:
Given an array and a window size, find the maximum element in each sliding window of the array.


## Input Format:
The input consists of two lines:

The user will be prompted to enter the elements of the array, separated by spaces.
The user will also be prompted to enter the window size.

## Output Format:
The maximum element in each sliding window will be printed

## Test Case 1:
Sample Input:
1 3 -1 -3 5 3 6 7
3

Sample Output:
3 3 5 5 6 7

Input and Output Explanation:
The array is [1, 3, -1, -3, 5, 3, 6, 7] and the window size is3.

The first window is [1, 3, -1] and the maximum element is 3.
The second window is [3, -1, -3] and the maximum element is 3.
The third window is [-1, -3, 5] and the maximum element is 5.
The fourth window is [-3, 5, 3] and the maximum element is 5.
The fifth window is [5, 3, 6] and the maximum element is 6.
The sixth window is [3, 6, 7] and the maximum element is 7.

## Test Case 2:
Sample Input:
4 6 8 2 9 10
2

Sample Output:
6 8 8 9 10

Input and Output Explanation:
Explanation: The array is [4, 6, 8, 2, 9, 10] and the window size is 2. The maximum elements in each sliding window are: 6 (from [4, 6]), 8 (from [6, 8]), 8 (from [8, 2]), 9 (from [2, 9]), 10 (from [9, 10]).

## Level: Medium

## Hints:
- Use a deque (double-ended queue) to efficiently maintain the maximum elements in the sliding window.
Initialize the deque with the indexes of the elements in the first window.
Process the remaining elements of the array one by one and maintain the deque in a decreasing order of elements.

- At each step, the maximum element in the current window can be obtained from the front of the deque.
Remove the elements from the deque that are outside the current window range or smaller than the current element.
Add the index of the current element to the rear of the deque.
Print the maximum element of each window.


## Approach:
- Create an empty deque to store the indexes of elements.
- Iterate through the array and perform the following steps:
- Remove the indexes from the front of the deque that are outside the current window range.
- Remove the indexes from the rear of the deque that correspond to elements smaller than the current element.
- Add the index of the current element to the rear of the deque.
- If the index at the front of the deque is outside the current window range, print the element at that index as the maximum element of the window.
- Print the maximum element of the last window.