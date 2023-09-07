
Topic: [[Arrays Hashing Strings]]
Week: 1
```python
class Solution:
	def strStr(self, haystack: str, needle: str) -> int:
		i = 0
		while i < len(haystack):
			if haystack[i] == needle[0]:
				count = 0
				j = i
				while count < len(needle) and j<len(haystack) and haystack[j] == needle[count] :
					count+=1
					j+=1
				if count == len(needle):
					return i
			i+=1
		return -1
```
