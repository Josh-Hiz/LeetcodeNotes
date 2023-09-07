
Topic: [[Arrays Hashing Strings]]
Week: 1
```python
class Solution:
	def findDisappearedNumbers(self, nums: List[int]) -> List[int]:
		res = []
		nums1 = set(nums)
		for i in range(1,len(nums)+1):
			if i not in nums1:
				res.append(i)
	return res
```
