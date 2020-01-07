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

```
#Answer:
def subsets(nums):
    """
    :type nums: List[int]
    :rtype: List[List[int]]
    """
    result = [[]]
    for num in nums:
        result += [i + [num] for i in result]
    return result

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
```
Answer:
def rotate_search(n, target):
    head = 0
    tail = len(n) - 1
    while (head <= tail):
        mid = (head + tail) // 2
        if n[mid] == target:
            return mid
        elif n[mid] > n[head]:
            if n[tail] > n[mid]:
                if n[mid] > target:
                    tail = mid - 1
                else:
                    head = mid + 1
            else: #smaller
                if n[head] <= target and target < n[mid]:
                    tail = mid - 1
                else:
                    head = mid + 1
        else:
            if n[mid] < target and target <= n[tail]:
                head = mid + 1
            else:
                tail = mid - 1
                
    return -1

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
```
# Answer: think about case [2,2,2,2,2,1,2,2]
def rotate_search2(n, target):
    for i in n:
        if target == i:
            return True
    return False

rotate_search2([2,2,2,2,1,2,2], 3)

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

```
def find_one(nums):
    result = 0
    for i in nums:
        result ^= i 
    return result

find_one([2,2,3,3,4,1,1])
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
```
def find_k(nums, k):
    value_idx = {}
    for i in range(0, len(nums)):
        if nums[i] in value_idx and i - value_idx[nums[i]] <= k:
                return True
        else:
            value_idx[nums[i]] = i
    return False

find_k([1,2,3,4,1,2,3], 4)
```