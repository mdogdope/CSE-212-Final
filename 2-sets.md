# Sets
A set is a useful tool when we want to compile a list of unique data. The way items are checked and inputed is done in a very efficient way.

When you add an item to a set it is hashed into a number and that is where the item is placed. This is because when the same item is added it is inserted into the same spot thus eliminating any duplicates.

The basic methods of a set is:
- add() - Insert an item into a set
- remove() - Remove the given item if present.
- intersection(set) - returns all items that are in both sets



## Example: Remove doubles.
```python
ids = [1, 2, 3, 4, 7, 9, 3, 6, 2, 0, 5]

set = set()
for id in ids:
	set.add(id) # Add each id to the set.

for item in set:
	print(item)
```
Output:
```
0
1
2
3
4
5
6
7
9
```
## You Try: Different search
Write code to remove all double ids using a set.
```python
ids = [1, 2, 3, 4, 7, 9, 3, 6, 2, 0, 5]
def removeDoubles(itemArray):
	pass
```