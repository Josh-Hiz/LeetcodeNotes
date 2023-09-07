
Topic: [[Arrays Hashing Strings]]
Week: 1

```python
class Solution:
	def replaceElements(self, arr: List[int]) -> List[int]:
		# Original solution, uses two pointers
		# i,j=0,len(arr)
		# while i < len(arr):
			# if i == len(arr)-1:
				# arr[i] = -1
				# break
			# else:
				# max_to_right = max(arr[i+1:j])
				# arr[i] = max_to_right
				# i+=1
		# return arr
		# Solution with just one for loop, simply start at the end such that the max
		# is always going to be found
		m = -1
		for i in range(len(arr)-1,-1,-1):
			new_max = max(m,arr[i])
			arr[i] = m
			m = new_max
		return arr
```

