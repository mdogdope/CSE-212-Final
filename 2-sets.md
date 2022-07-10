# Sets
Sets are in your life every day. When ever you have a list of items that all pertain to something you are using a set.

A set allows us to store multiple values in a single variable. Items in a set are, unordered, unchangeable, and allow no duplicates.

## Example: Names in a Pool
You are making a program to deliver you resume. When listing the languages you know you put them into a set, because you don't want any double entries and order does not matter.

The program can look like this:
```python
s = set("Java", "C++", "Python")

print(s)
```
The Output:
```
{'Java','C++','Python'}
```

## You Try: Cards in a players hand
We already have the deck sorted out from the previous tutorial, now we need to handle each players hand.

In a game of cards each player will have a hand consisting of any number of cards, of which the order does not matter because they can see them all. Using sets write code to handle each players hand.

Click here for the [Solution](2-answer.md).