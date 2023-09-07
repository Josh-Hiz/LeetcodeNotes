Topic: [[Arrays Hashing Strings]]
Week: 1
```python
class Solution(object):
		def productExceptSelf(self, nums):
			"""
			:type nums: List[int]
			:rtype: List[int]
			"""
			# Brute force solution O(N^2)
			# answer = [0] * len(nums)
			# for i in range(len(nums)):
				# product = 1
				# for j in range(len(nums)):
					# if j != i:
						# product *= nums[j]
				# answer[i] = product
			# return answer
			# The O(n) solution: Neetcode :)
			res = [1] * len(nums)
			prefix = 1
			for i in range(len(nums)):
				res[i] = prefix
				prefix *= nums[i]
			postfix = 1
			for i in range(len(nums)-1,-1,-1):
				res[i] *= postfix
				postfix *= nums[i]
			return res
```
