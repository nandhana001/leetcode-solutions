# LeetCode 136. Single Number

## Problem
Given a non-empty array of integers, every element appears twice except for one. Find that single one.

### Example
Input: nums = [4,1,2,1,2]
Output: 4

---

## 💡 Hey, I found an amazing way to solve this problem!

My first thought was to use a hash map to count frequencies, but that would require extra space.

Then I remembered the XOR trick:

- x ^ x = 0
- x ^ 0 = x

Since every number except one appears twice, all duplicate numbers cancel each other out, leaving only the single number.

---

## Solution

### Python
```python
class Solution:
    def singleNumber(self, nums: List[int]) -> int:
        ans = 0

        for num in nums:
            ans ^= num

        return ans
```

---

## Dry Run

nums = [4,1,2,1,2]

ans = 0

0 ^ 4 = 4  
4 ^ 1 = 5  
5 ^ 2 = 7  
7 ^ 1 = 6  
6 ^ 2 = 4

Answer = 4

---

## Complexity Analysis

- Time Complexity: O(n)
- Space Complexity: O(1)

---

## Key Takeaway

XOR is perfect for problems where elements appear in pairs because duplicate values cancel each other out automatically.
<img width="1882" height="723" alt="Screenshot 2026-06-18 110635" src="https://github.com/user-attachments/assets/7ebb300d-5fc4-4938-914d-f978582533f8" />



