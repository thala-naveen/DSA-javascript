## Problem Statement:
Subarray with Sum K Hashing

## Problem Statement:
Given an array of integers and a target sum, find if there exists a subarray with a sum equal to the target.


## Input Format:
The first line contains space-separated integers representing the array elements.
The second line contains a single integer representing the target sum.


## Output Format:
The output is a boolean value indicating whether a subarray with the target sum exists or not.


## Test Case 1:
Sample Input:
3 4 7 2 -3 1 4 2
7

Sample Output:
true

Explanation:
In the given sample input, there exists a subarray [4, 2, 1] whose sum is equal to the target sum 7. Therefore, the output is true.

## Test Case 2:
Sample Input:
1 2 3 4 5
9

Sample Output:
true

Explanation:
The subarray [2, 3, 4] has a sum of 9, which matches the target sum.

## Level: Easy

## Hints:
- Consider using a hash map to store the cumulative sum up to each index along with their frequencies.
Iterate through the array and calculate the cumulative sum at each index.
- Check if the difference between the cumulative sum at the current index and the target sum exists in the hash map.
If the difference exists, it means there is a subarray with the target sum.


## Approach:
- Initialize a hash map to store the cumulative sum and its frequency.
- Initialize a variable sum to keep track of the cumulative sum.
- Iterate through the array elements from left to right.
- Calculate the cumulative sum by adding the current element to sum.
- Check if the difference between sum and the target sum exists in the hash map.
- If it exists, return true.
- Increment the frequency of the cumulative sum in the hash map.
- If the target sum is not found after iterating through all elements, return false.
