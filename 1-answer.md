# Solution: Queues

```python
deck = []

## Add cards
for suit in range(1,4): # The four suits
	for value in range(1,13): # The value of each card
		deck.append(Card(value, suit))

# Get the top card.
top_card = deck.pop(0)
```