## Problem Statement:
Group Anagrams

## Problem Statement:
Given an array of strings, group the anagrams together and return the groups as a 2D array. An anagram is a word formed by rearranging the letters of another word.


## Input Format:
The first line of input contains an integer N, representing the number of strings in the array.
The next N lines contain the strings.

## Output Format:
The output is a 2D array where each inner array represents a group of anagrams.
Each group of anagrams is sorted in lexicographic order.

## Test Case 1:
sample Input
6
eat
tea
tan
ate
nat
bat

Sample Output
[["eat","tea","ate"],["tan,nat"],["bat"]]

The output groups the anagrams together:
The anagrams "ate", "eat", and "tea" are grouped together.
The string "bat" is alone and forms a group by itself.
The anagrams "nat" and "tan" are grouped together.

## Test Case 2:
sample Input
4
abc
bca
xyz
cba

Sample Output
[["abc","bca","cba"],["xyz"]]

The anagrams "abc", "bca", and "cba" are grouped together. The string "xyz" forms a group by itself.

## Level: Hard

## Hints:
- To check if two strings are anagrams, you can compare their sorted versions.
Use a hash table to group the anagrams together.

- Iterate through each string and calculate its hash. Use the hash as the key in the hash table and add the string to the corresponding group.

## Approach:
- Create an empty hash table to store the groups of anagrams.
- Iterate through each string in the input array.
- Sort the current string and use it as a key in the hash table.
- If the key already exists in the hash table, add the current string to the existing group.
- If the key doesn't exist, create a new group with the current string.
- Finally, return the values of the hash table as the output.
