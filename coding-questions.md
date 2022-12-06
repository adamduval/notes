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

hashing one line version

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
class Solution:
    def isAnagram(self, s: str, t: str) -> bool:
        
        # if len s != len r return false
        if len(s) != len(t):
            return False
        
        # setup tracking dictionaries
        tracking_s, tracking_t = {}, {}
    
        # count all characters in s, t
        for i in range(len(s)):
            tracking_s[s[i]] = 1 + tracking_s.get(s[i], 0)
            tracking_t[t[i]] = 1 + tracking_t.get(t[i], 0)
        
        # check equality
        return tracking_s == tracking_t
```

time: O(n) - based ont the size of both strings  
space: O(n) - additional memory allocation for hash maps of each string

sorting

time: n(log(n)) - depends on the sort type, best case sorting algo is n(log((n))
space: O(1) - assumption that sorting does not take extra space

```Python
class Solution:
    def isAnagram(self, s: str, t: str) -> bool:
        return sorted(s) == sorted(t)
```

#### two sum

[LeetCode](https://leetcode.com/problems/two-sum/)

brute force

```Python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        
        for i in range(len(nums)):
            for j in range(i+1, len(nums)):
                if nums[i] + nums[j] == target:
                    return [i, j]         
```

time: O(n^2) - need to go through array size n at maximum n times for each number (n*n) = n^2
space: O(1) - no extra memory required

hash map

```Python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        
        hmap={} # val: num
        
        for idx, num in enumerate(nums): 
            diff = target - num
            if diff in hmap:
                return[hmap[diff], idx]
            hmap[num] = idx
```

A hash map has constant lookup time. The algorithm on loops through the array once and each insertion/lookup is O(1).

time: O(n)
space: O(n)

#### group anagrams

[LeetCode](https://leetcode.com/problems/group-anagrams/)

brute force

```Python
class Solution:
    def groupAnagrams(self, strs: List[str]) -> List[List[str]]:
        
        answer = []
        
        #track words added to answers list
        added=[]
        
        # loop strings, get str1 to check
        for i in range(len(strs)):
            str1 = strs[i]
            
            # check if str already in an anagram list
            if str1 in added:
                continue
            
            # track anagrams for string
            str_ouput = []
                
            # loop comparison string, str2
            for j in range(i+1, len(strs)):
                str2 = strs[j]
                
                # compare length    
                if len(str1) == len(str2):
                    
                    # make comparison 
                    
                    str1_track, str2_track = {}, {}
                    
                    # compare letters
                    for k in range(len(str1)):
                        str1_track[str1[k]] = 1 + str1_track.get(str1[k], 0)
                        str2_track[str2[k]] = 1 + str2_track.get(str2[k], 0)
                        
                    if str1_track == str2_track:
                        str_ouput.append(str2)
                        added.append(str2)
                            
            str_ouput.append(str1)    
            answer.append(str_ouput)
        
        return answer
```

time: #TODO
space: #TODO

--

## End
