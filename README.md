# Leetcode-2367.-Number-of-Arithmetic-Triplets

# Description
You are given a 0-indexed, strictly increasing integer array nums and a positive integer diff. A triplet (i, j, k) is an arithmetic triplet if the following conditions are met:

i < j < k,
nums[j] - nums[i] == diff, and
nums[k] - nums[j] == diff.
Return the number of unique arithmetic triplets.
# Solution
In the given problem , we have been given an array nums which contains numbers in increasing order and we have also been given an integer diff.

The problem aims to find the number of arithmetic triplets i,j,k which satisfy the condition:

nums[j] - nums[i] == diff and nums[k] - nums[j] == diff.

Example:
nums = [4,5,6,7,8,9], diff = 2

(0, 2, 4) is an arithmetic triplet with 2-0 = 2 and 4-2 =2
(1, 3, 5) is also a triplet with 3-1 =2 and 5-3 = 2

# Code
class Solution:

    def arithmeticTriplets(self, nums: List[int], diff: int) -> int:
        count=0
        for i in range(0,len(nums)):
            for j in range(i+1,len(nums)):
                for k in range(j+1,len(nums)):
                    if nums[j]-nums[i]==diff and nums[k]-nums[j]==diff:
                        count+=1
        return count

# Algorithm
1. Create a count variable which stores the number of arithmetic triplets found.
2. Use 3 for loops which loops to check for the condition.
3. If the condition is satisfied then increment the count by 1.
4. Return the count.

# Time Complexity
 for i in range(0,len(nums)): Uses O(n) of time complexity
 
for j in range(i+1,len(nums)):Uses O(n) of time complexity
            
for k in range(j+1,len(nums)):Uses O(n) of time complexity

Hence, the total time complexity : O(n^3)

 if nums[j]-nums[i]==diff and nums[k]-nums[j]==diff: This part of the code compares and checks in O(1) time .

 Time complexity : O(n^3)
