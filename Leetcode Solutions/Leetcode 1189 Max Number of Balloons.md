
Topic: [[Arrays Hashing Strings]]
Week: 1
```python
class Solution:
	def maxNumberOfBalloons(self, text: str) -> int:
		# Simply count frequency of all letters in the text that are in the word balloon
		# then just simply return the smallest count as that will be the max number you can construct
		freq = {'b':0,'a':0,'l':0,'o':0,'n':0}
		
		for item in text:
		
		if item in freq:
		
		freq[item]+=1
		
		return min(freq['b'],freq['a'],freq['l']//2,freq['o']//2,freq['n'])
```
