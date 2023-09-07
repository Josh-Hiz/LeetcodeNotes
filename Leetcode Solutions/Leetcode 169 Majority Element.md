
Topic: [[Arrays Hashing Strings]]
Week: 1
```python
class Solution:
	def majorityElement(self, nums: List[int]) -> int:
		freq = {}
		for item in nums:
			freq[item] = 1 + freq.get(item,0)
		return max(freq,key=freq.get)
```
