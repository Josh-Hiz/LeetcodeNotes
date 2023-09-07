Topic: [[Arrays Hashing Strings]]
Week: 1
```python
class Solution:
	def twoSum(self, nums: List[int], target: int) -> List[int]:
		# Two sum is a classic problem in which encompases some basic
		# math and the concept of a hashmap to store key and values
		# the question is asking to find two values, a and b such that
		# a + b == target, the naive brute force way is to compare every single
		# pair of numbers in the array using two for loops O(n^2):
		# for i in range(len(nums)):
		# for j in range(1,len(nums)):
		# if nums[i] + nums[j] == target and i != j:
		# return [i,j]
		# The efficent way is to realize that if a+b == target, then
		# target - b = a, and if we know a is in the array then we can
		# just grab the index of a! In order to get its index, we can store
		# its index in a hashmap where the key is "a" and the value is its
		# index! This allows for efficent searching
		index_hash = {}
		for i in range(len(nums)):
			# if target - b is in the hashmap already
			if target - nums[i] in index_hash:
				return index_hash[target-nums[i]],i
			else:
				# Store every element in the array into the hashmap with its index
				index_hash[nums[i]] = i
```
