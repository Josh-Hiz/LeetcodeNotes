
Topic: [[Arrays Hashing Strings]]
Week: 1
```python
class Solution:
	def subarraySum(self, nums: List[int], k: int) -> int:
		# N^2 sol
		# res = 0
		# for i in range(len(nums)):
			# for j in range(i,len(nums)+1):
				# if sum(nums[i:j]) == k and j != i:
					# res+=1
		# return res
		# Prefix sum solution
		prefix_sum_dict = {0:1} # Key is sum, count of occurances is value
		prefixSum = 0
		res = 0
		for i in range(len(nums)):
			prefixSum += nums[i]
			difference = prefixSum - k
			if difference in prefix_sum_dict:
				res += prefix_sum_dict[difference]
			prefix_sum_dict[prefixSum] = 1 + prefix_sum_dict.get(prefixSum,0)	
		return res
```
