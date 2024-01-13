
# LeetCode Challenge D28

## Overview

Welcome to my LeetCode solution repository! This project addresses the coding challenge presented by [1608. Special Array With X Elements Greater Than or Equal X](https://leetcode.com/problems/special-array-with-x-elements-greater-than-or-equal-x/). Below, you'll find details about the problem, my approach to solving it, and the implemented solution.

## Problem Statement


You are given an array  `nums`  of non-negative integers.  `nums`  is considered  *special*  if there exists a number  `x`  such that there are  *exactly*  `x`  numbers in  `nums`  that are  *greater than or equal to*  `x`.

Notice that  `x`  *does not*  have to be an element in  `nums`.

Return  `x`  _if the array is  *special*, otherwise, return_ `-1`. It can be proven that if  `nums`  is special, the value for  `x`  is  *unique*.

**Example**
> **Input:** nums = [0,0]
> 
> **Output:** -1
> 
> **Explanation:**
> No numbers fit the criteria for x. If x = 0, there should be 0 numbers >= x, but there are 2. 
> If x = 1, there should be 1 number >= x, but there are 0. 
> If x = 2, there should be 2 numbers >= x, but there are 0. x cannot be greater since there are only 2 numbers in nums.

**Language Used**
> Java

**Difficulty**
> Easy

## Solution Overview
The code starts by sorting the input array `nums` in ascending order using `Arrays.sort(nums)`. It then iterates through possible values of 'x', ranging from 0 to the length of the array (`n`). This represents the condition that there should be exactly 'x' numbers in the array greater than or equal to 'x'. Inside the outer loop, there is an inner loop that iterates through the sorted array to count how many numbers are greater than or equal to the current 'x'. After counting, it checks whether the count is equal to 'x'. If so, it means that there are exactly 'x' numbers in the array greater than or equal to 'x', and it returns 'x' as the result. If no such 'x' is found that satisfies the condition, the function returns -1.
