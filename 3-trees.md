# Trees
Trees are an efficient way to organize and store data. 

Trees are made up of a root node and child nodes. Each node holds a value or values, along with the address of their left and right child nodes. Below is a visual representation of a binary tree.
![](tree.png)
Node 10 is our root node because it is the start of the tree. It has two child nodes, node 5 as the left node and node 19 as the right node. These child nodes have child nodes themselves, and they are labeled the same way.

The way a tree is organized is based on the value each node holds. The root node can take any value, it is just to get started. When we add more nodes we have to follow a pattern. If the value of the new node is bigger than the existing node we put it as the right child of said node, and the opposite if it is smaller.

Using the image above we see that node 10 is our root node. When we added node 5 we compared it to node 10 and found it smaller, so we placed it to the left. Next we added node 6. It is smaller than 10 so we go to the left and it is bigger than 5 so we go right. Since there is no node to the right of node 5, we make a new node with value 6.

Now let's look at the code.
```python
class Node:
	def __init__(self,data):
		self.right = None
		self.left = None
		self.data = data
	
	def insert(self, data):
		if self.data: # make sure data is set to existing node
			if data < self.data:
				if self.left is None:
					self.left = Node(data)
				else:
					self.left.insert(data)
			elif data > self.data:
				if self.right is None:
					self.right = Node(data)
				else:
					self.right.insert(data)
		else:
			self.data = data
	
	def printTree():
		if self.left:
			self.left.printTree()
		print(self.data)
		if self.right:
			self.right.printTree()

tree = Node(10)
tree.insert(5)
tree.insert(1)
tree.insert(6)
tree.insert(19)
tree.insert(17)
tree.insert(21)
tree.printTree()
```
Output:
```
1
5
6
10
17
19
21
```
# Example: Searching data
We are going to store data about cars. We are going to use the year as the base value so we can search by it.
```python
class Node:
	def __init__(self,year, miles):
		self.right = None
		self.left = None
		self.year = year
		self.miles = miles
	
	def insert(self, year, miles):
		if self.year: # make sure data is set to existing node
			if year < self.year:
				if self.left is None:
					self.left = Node(year, miles)
				else:
					self.left.insert(year, miles)
			elif year > self.year:
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
The above code will store the given info in a tree organized by the year.

## You Try: Organize by miles
Given is the code from the example. Your job is to modify it to organize the nodes by miles instead of by year.
```python
class Node:
	def __init__(self,year, miles):
		self.right = None
		self.left = None
		self.year = year
		self.miles = miles
	
	def insert(self, year, miles):
		if self.year: # make sure data is set to existing node
			if year < self.year:
				if self.left is None:
					self.left = Node(year, miles)
				else:
					self.left.insert(year, miles)
			elif year > self.year:
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


Click here for the [Solution](3-answer.md).