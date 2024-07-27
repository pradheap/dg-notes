[Problem Link](https://leetcode.com/problems/contains-duplicate/description/)
Given an integer array `nums`, return `true` if any value appears **at least twice** in the array, and return `false` if every element is distinct.

**Example 1:**

**Input:** nums = [1,2,3,1]
**Output:** true

**Example 2:**

**Input:** nums = [1,2,3,4]
**Output:** false

**Constraints:**

- `1 <= nums.length <= 105`
- `-109 <= nums[i] <= 109`

```python
class Solution:
     def containsDuplicate(self, nums: List[int]) -> bool:
```
## Thoughts
Imagine we're given a set of numbered cards such that there is a duplicate and we've to find it. How can we solve it? 

We go through the numbers (if they are few like 5), memorize it (extra space) and go through the set of cards at hand to find the duplicate. If there are a large number of cards, we might need to note down the numbers we see from left to right and then go through the cards at hand. (2 iterations, right?)
But we can also do that in one go, if we think about it. While going through the cards at hand and noting down the numbers, we can also check if the number in the card was noted down already. This optimization will result in only one traversal of the cards at hand.

What if there is no pen and paper available to us. (meaning no extra space) What can we do?
Hmm, maybe we can sort the numbered cards at hand and then it is easy to spot the duplicates in a regular traversal with two pointers.

We can also convert the given array/list into a set and compare their size, if we can use language specific functions. If their size differs, then there are duplicates in the given list.
## Code

```python

class Solution:
	def containsDuplicate(self, nums: List[int]) -> bool:
		all_nums = {}
		for num in nums:
			if num in all_nums:
				return True
			else:
				all_nums[num] = 1
		return False
```
### After Thought
We could use `set()` instead of a dict `{}`.