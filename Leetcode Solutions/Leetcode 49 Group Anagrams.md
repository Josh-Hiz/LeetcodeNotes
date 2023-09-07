Topic: [[Arrays Hashing Strings]]
Week: 1
```python
class Solution:
	def groupAnagrams(self, strs: List[str]) -> List[List[str]]:
		# This problem wants you to group every string in the strs
		# array that are anagrams of eachother, meaning that every anagram
		# list will be unique and that every word in every anagram list will
		# share a common atribute (that being anagrams) but to make it easier
		# when they are sorted lexographically they will be the same! so we can
		# just store their sorted versions in a hashmap key and group based on that
		res = {}
		for word in strs:
			# Sort a string as a list and store as a string
			sword = "".join(sorted(word))
			# check if the anagram is in the hashmap
			if sword in res:
				res[sword].append(word)
			else:
				res[sword] = [word]
		# return all the values!
		return res.values()
```
