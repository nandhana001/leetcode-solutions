# leetcode-solutions
My collection of coding problems and elegenat solutions

# LeetCode 136 - Single Number

## Problem
Given a non-empty array of integers, every element appears twice except for one. Find that single one.

### Example
Input: [2,2,1]
Output: 1

---

## 💡 Hey, I found an amazing way to solve this problem!

At first, I thought of using a HashMap to count frequencies. But then I realized that XOR has a special property:

- a ^ a = 0
- a ^ 0 = a

Since every number appears twice, all pairs cancel each other out, leaving only the single number.

---

## Approach
1. Initialize result = 0.
2. XOR each number with result
3. Return result

---

## Python Code


def singleNumber(nums):
    result = 0
    for num in nums:
        result ^= num
    return result


---

## Example Walkthrough

nums = [4,1,2,1,2]

result = 0

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

## Key Insight

Using XOR allows us to solve the problem in constant space without extra data structures.XOR is perfect for problems where elements appear in pairs because duplicate values cancel each other out automatically
<img width="1882" height="723" alt="Screenshot 2026-06-18 110635" src="https://github.com/user-attachments/assets/7ebb300d-5fc4-4938-914d-f978582533f8" />



