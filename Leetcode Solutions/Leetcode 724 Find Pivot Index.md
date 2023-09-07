
Topic: [[Arrays Hashing Strings]]
Week: 1
```python
class Solution:
	def pivotIndex(self, nums: List[int]) -> int:
		# Original solution
		# for i in range(len(nums)):
			# if sum(nums[0:i]) == sum(nums[i+1:]):
				# return i
		# return -1
		# Better solution
		left = 0
		right = sum(nums)
		for i in range(len(nums)):
			right-=nums[i]
			if right == left:
				return i
			left+=nums[i]
		return -1
```