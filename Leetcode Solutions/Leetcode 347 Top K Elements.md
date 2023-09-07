Topic: [[Arrays Hashing Strings]]
Week: 1
```python
class Solution:
	def topKFrequent(self, nums: List[int], k: int) -> List[int]:
		# This element is a classic "Top K" question in which asks you to
		# return the top k elements from an array, meaning the top k most
		# frequent elements in the array, my solution would be to have a
		# hashmap to keep track of the frequencies of every number
		# through the array only once, and then using python syntax to return
		frequencies = {}
		for num in nums:
			if num not in frequencies:
				frequencies[num] = 1
			else:
				frequencies[num]+=1
		return list(sorted(frequencies, key=frequencies.get, reverse=True))[:k]
```

```python
#Heap solution (Excellent for learning how to use heaps!)
maxHeap = []
s = set(nums)
for item in s:
	heapq.heappush(maxHeap,[-nums.count(item),item])
res = []
heapify(maxHeap)
while k > 0:
	res.append(maxHeap[0][1])
	heapq.heappop(maxHeap)
	k-=1
return res
```
