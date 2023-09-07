
Topic: [[Arrays Hashing Strings]]
Week: 1
```python
class Solution:
	def isSubsequence(self, s: str, t: str) -> bool:
	# First solution
	if s == '':
		return True
	idx = 0
	for i in range(len(t)):
		if t[i] == s[idx]:
			idx+=1
		if idx == len(s):
			return True
# The original solution is above, except this is a more clear two pointers, my previous was two pointers except I have i continue running and the idx was its own variable
		# i,j = 0,0
		# while i < len(s) and j < len(t):
			# if s[i] == t[j]:
				# i+=1
			# j+=1
		# return i == len(s)
```
