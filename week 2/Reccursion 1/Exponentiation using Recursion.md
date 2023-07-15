## Problem Statement:
Exponentiation using Recursion

## Problem Statement:
 Write a recursive function to calculate the value of x raised to the power of p (x^p).


## Input Format:
The user will be prompted to enter two numbers: x (base) and p (exponent). Both numbers should be positive integers.

## Output Format:
The function should return the result of x^p as a number.

## Test Case 1:
Sample Input:
2
3

Sample Output:
8

Exp : In the sample input, the base is 2 and the exponent is 3. Therefore, the function should calculate 2 raised to the power of 3, which equals 8. The output is the result of the exponentiation operation.


## Test Case 2:
Sample Input:
5
0

Sample Output:
1

Explanation: Any number raised to the power of 0 is equal to 1.


## Level: Medium

## Hints:
- The base case for the recursion is when the exponent is 0. In this case, the result is always 1.
If the exponent is greater than 0, you can recursively calculate the result by multiplying the base (x) with the result of raising x to the power of p-1.
- If the exponent is negative, you can recursively calculate the result by dividing 1 by the result of raising x to the power of -p.

## Approach:
- Prompt the user to enter the base (x) and exponent (p) as positive integers.
- Implement a recursive function that takes x and p as parameters.
- Define the base case:
- If p is 0, return 1.
- If p is greater than 0, recursively calculate the result by multiplying x with the result of calling the function with x and p-1.
- If p is negative, recursively calculate the result by dividing 1 by the result of calling the function with x and -p.
- Print the result obtained from the recursive function call.
