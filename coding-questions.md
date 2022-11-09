# Coding Questions / Challenges etc

## Inbox

--

## Log

--

## Notes

### Arrays and Hashing

#### contains duplicate

[LeetCode](https://leetcode.com/problems/contains-duplicate/)

brute force

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

sorting

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

hashing (hash set)

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
space: O(n) additional memory allocation for set  

#### is valid anagram

[LeetCode](https://leetcode.com/problems/valid-anagram/)

brute force

```python
# working
class Solution:
    def isAnagram(self, s: str, t: str) -> bool:
        
        # if len s != len r return false
        if len(s) != len(t):
            return False
        
        # check if t has same letters and quantities as s
        
        for i in range(len(s)):
            for j in range(len(t)):
                if s[i] == t[j]:
                    j[i] == '\0' # flag char as already accounted for
                else:
                    return False
            return True
```

--

## End
