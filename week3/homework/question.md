Q1. Given a set of unique integers, return all possible subsets.

``` 
# Example:
# Input: [1,2,3]
# Output: [ [3], [1], [2], [1,2,3], [1,3], [2,3], [1,2], [] ]
# Use this format for coding.

def subsets(nums):
    """
    :type nums: List[int]
    :rtype: List[List[int]]
    """
```        


Q2. Suppose an array sorted in ascending order is rotated. (i.e., [0,1,2,4,5,6,7] might become [4,5,6,7,0,1,2]).
    
You are given a target value to search. If found in the array return true, otherwise return false.
```
Example 1:

Input: nums = [4,5,6,7,0,1,2], target = 0
Output: 4
Example 2:

Input: nums = [4,5,6,7,0,1,2], target = 3
Output: -1
```


Q3. For Q2, what if there are repeated numbers in the array?
```    
    Example 1:
    
    Input: nums = [2,5,6,0,0,1,2], target = 0
    Output: true
    Example 2:
    
    Input: nums = [2,5,6,0,0,1,2], target = 3
    Output: false
```


Q4. Given a non-empty array of integers, every element appears twice except for one. Find that single one.
```
Example 1:

Input: [2,2,1]
Output: 1
Example 2:

Input: [4,1,2,1,2]
Output: 4
```

Q5. Given an array of integers and an integer k, find out whether there are two distinct indices i and j 
in the array such that nums[i] = nums[j] and the absolute difference between i and j is at most k.

```
Example 1:

Input: nums = [1,2,3,1], k = 3
Output: true
Example 2:

Input: nums = [1,0,1,1], k = 1
Output: true
Example 3:

Input: nums = [1,2,3,1,2,3], k = 2
Output: false
```
