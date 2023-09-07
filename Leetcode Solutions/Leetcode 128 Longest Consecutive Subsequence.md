Topic: [[Arrays Hashing Strings]]
Week: 1
```python
class Solution:
	def longestConsecutive(self, nums: List[int]) -> int:
		# Longest consecutive sequence is a standard and fundamental
		# question about finding the longest of something, meaning
		# you usually go through an array and start counting the occurances
		# of something until its no longer valid, usually with a for loop
		maxLength = 0
		n_set = set(nums)
		for num in n_set:
			if num - 1 not in n_set:
				count = 1
				while num + count in n_set:
					count+=1
				maxLength = max(maxLength,count)
		return maxLength
```
