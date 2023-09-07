Topic: [[Arrays Hashing Strings]]
Week: 1
```python
class Solution:
	def isAnagram(self, s: str, t: str) -> bool:
		# This question is about going through a string
		# and making sure that both strings contain all the
		# same letters exactly once, what we can do is use a
		# python set, or in this case a Hashset so that we can go
		# through every character of s exactly once and check its count
		# by using the count method to see if it matches with t's count
		if len(s) != len(t):
			return False
		else:
			for letter in set(s):
				if t.count(letter) != s.count(letter):
					return False
			return True
```
