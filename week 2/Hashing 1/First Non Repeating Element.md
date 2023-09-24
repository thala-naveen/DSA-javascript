## Problem Statement:
First Non Repeating Element

## Problem Statement:
The task is to find the first non-repeating character in a given string. A non-repeating character is a character that appears only once in the string.


## Input Format:
The input is a single line containing a string.

## Output Format:
The output is the first non-repeating character in the string. If no such character exists, output an empty string.

## Test Case 1:
Sample Input:
abbcadef

Sample Output:
c

Exp:The first non-repeating character in the string is "c".


## Test Case 2:
Sample Input:
xyzyz

Sample Output:
x

Exp:In the input string 'xyzxyz', the first non-repeating character is 'x'.

## Level: Medium

## Hints:
- Use a hash map or hash table to store the count of each character.
Iterate through the string and update the count for each character.

- Iterate through the string again and return the first character with a count of 1.
 

## Approach:
- Create a hash map or hash table to store the count of each character.
- Iterate through the string and update the count for each character in the hash map.
- Iterate through the string again and return the first character with a count of 1.
