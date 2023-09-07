
Topic: [[Arrays Hashing Strings]]
Week: 1

```python
class Solution:
	def sortColors(self, nums: List[int]) -> None:
		"""
		Do not return anything, modify nums in-place instead.
		"""
		# Linear time solution using counting sort in O(n) with O(n) space
		# Counting sort implementation
		output = [0] * len(nums)
		count = [0] * 10
		size = len(nums)
		for i in range(0,size):
			count[nums[i]]+=1
		for i in range(1,10):
			count[i] += count[i-1]
		i = size - 1
		while i>=0:
			output[count[nums[i]]-1] = nums[i]
			count[nums[i]]-=1
			i-=1
		for i in range(0,size):
			nums[i] = output[i]
		return nums
```
