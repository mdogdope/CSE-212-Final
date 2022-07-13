# Solution: Trees
```python
class Node:
	def __init__(self,year, miles):
		self.right = None
		self.left = None
		self.year = year
		self.miles = miles
	
	def insert(self, year, miles):
		if self.miles: # make sure data is set to existing node
			if miles < self.miles:
				if self.left is None:
					self.left = Node(year, miles)
				else:
					self.left.insert(year, miles)
			elif miles > self.miles:
				if self.right is None:
					self.right = Node(year, miles)
				else:
					self.right.insert(year, miles)
		else:
			self.year = year
			self.miles = miles
	
	def printTree():
		if self.left:
			self.left.printTree()
		print("[" + str(self.year) + "|" + str(self.miles) +"]")
		if self.right:
			self.right.printTree()

tree = Node(1997, 200241)
tree.insert(2010, 78299)
tree.insert(1999, 180300)
tree.insert(2005, 104203)
tree.printTree()
```