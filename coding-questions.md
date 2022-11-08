# Coding Questions / Challenges etc.

## Inbox

--

## Log

--

## Notes

### contains duplicate

- [LeetCode](https://leetcode.com/problems/contains-duplicate/)

#### brute force

```python
class Solution:
    def containsDuplicate(self, nums: List[int]) -> bool:
        for i in range(len(nums)):
            for j in range(i+1, len(nums)):
                if nums[i] == nums[j]:
                    return True
        return False
```

time: O(n^2) time complexity because it has to loop through the list twice
space: O(1) no extra memory required

#### sorting

```python
class Solution:
 def containsDuplicate(self, nums: List[int]) -> bool:
        nums.sort()
        for i in range (1, len(nums)):
            if nums[i-1] == nums[i]:
                return True
        return False
```

time: O(nlog(n))
space: O(1)

```python
class Solution:
    def containsDuplicate(self, nums: List[int]) -> bool:
        s = set()
        for num in nums:
            if num in s:
                return True
            s.add(num)
        return False
```

```python
class Solution:
    def containsDuplicate(self, nums: List[int]) -> bool:
     return len(set(nums)) < len(nums)
# shortest solution        
```

time: O(n)
space O(n) additional memory allocation for set


#### hash set

--

## End
