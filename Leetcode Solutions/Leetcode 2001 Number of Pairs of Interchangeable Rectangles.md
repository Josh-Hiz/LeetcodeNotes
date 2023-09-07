
Topic: [[Arrays Hashing Strings]]
Week: 1
```python
class Solution:
	def interchangeableRectangles(self, rectangles: List[List[int]]) -> int:
		# Original solution, O(n^2) that uses two pointers
		# i,j = 0,1
		# num_pairs = 0
		# while i < len(rectangles)-1:
			# while j<len(rectangles):
				# if rectangles[i][0]/rectangles[i][1] == rectangles[j][0]/rectangles[j][1]:
					# num_pairs += 1
				# j+=1
			# i+=1
			# j = i + 1
		# return num_pairs
		# Better solution using the combinations formula and hashmap
		count = {} 
		for w,h in rectangles:
			count[w/h] = 1 + count.get(w/h,0)
		res = 0
		for c in count.values():
			if c > 1:
				res += (c * (c-1)) // 2
		return res
```