
Topic: [[Arrays Hashing Strings]]
Week: 1
```python
class Solution:
	# Merge sort implementation
	def mergesort(self, nums: List[int]) -> List[int]:
		# Split the array
		if len(nums) > 1:
			middle = len(nums) // 2
			leftArray = nums[:middle]
			rightArray = nums[middle:]
			self.mergesort(leftArray)
			self.mergesort(rightArray)
		
		# sort the array
		i,j = 0,0
		idx = 0
		# merge two arrays into one sorted array
		while i < len(leftArray) and j < len(rightArray):
			if leftArray[i] <= rightArray[j]:
				nums[idx] = leftArray[i]
				i+=1
			else:
				nums[idx] = rightArray[j]
				j+=1
			idx+=1
		# Check if any remaining items are in either array
		while i < len(leftArray):
			nums[idx] = leftArray[i]
			i+=1
			idx += 1
		while j < len(rightArray):
			nums[idx] = rightArray[j]
			j+=1
			idx += 1
			
	def sortArray(self, nums: List[int]) -> List[int]:
		self.mergesort(nums)
		return nums
```
