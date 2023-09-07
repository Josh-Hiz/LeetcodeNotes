Topic: [[Arrays Hashing Strings]]
Week: 1
```python
class Solution:
	def isValidSudoku(self, board: List[List[str]]) -> bool:
		rows = defaultdict(set)
		cols = defaultdict(set)
		squares = defaultdict(set)
		# Constant board dimensions
		for row in range(9):
			for col in range(9):
				if board[row][col] == '.':
					continue
				elif (board[row][col] in rows[row] or board[row][col] in squares[(row//3,col//3)] or board[row][col] in cols[col]):
					return False
				else:
					rows[row].add(board[row][col])
					cols[col].add(board[row][col])
					squares[(row//3,col//3)].add(board[row][col])
		return True
```
