Topic: [[Arrays Hashing Strings]]
Week: 1
```python
class Solution:
	def containsDuplicate(self, nums: List[int]) -> bool:
		# Hashset solution
		# This question is fundamental to understanding detecting duplicates
		# any iterable object, hashsets are excellent for doing so sets dont
		# allow duplicates
		nset = set()
		for num in nums:
			if num in nset:
				return True
			else: 
				nset.add(num)
```
