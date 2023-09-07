
Topic: [[Arrays Hashing Strings]]
Week: 1
```python
class Solution:
	def checkPossibility(self, nums: List[int]) -> bool:
		used = 0
		for i in range(len(nums)-1):
			if nums[i] <= nums[i+1]:
				continue
			if used:
				return False
			if i==0 or nums[i+1] >= nums[i-1]:
				nums[i] = nums[i+1]
			else:
				nums[i+1] = nums[i]
			used = 1
return True
```
