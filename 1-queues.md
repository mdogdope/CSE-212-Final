# Queues
Writing software would be very difficult if we could not give our data some kind of order. 

A queue can be seen like a line at an amusement park. The order is dictated by when each item enters the queue. When it is time to remove someone from the queue we pick the item at the front of the line. Keeping with our analogy, when someone enters a line at a ride they start at the back, and as each person rides the ride, removing them from the queue, you move forward in the queue.

In python a queue can be created using a list:
```python
queue = [] # Create the queue.

# Populate the queue with some items.
queue.append("Item 1")
queue.append("Item 2")
queue.append("Item 3")

# Remove an item and print it.
# An index of 0 is needed because it is the front of the line.
print(queue.pop(0))
print(queue.pop(0))
print(queue.pop(0))
```
The above will have the following output:
```
> Item 1
> Item 2
> Item 3
```

## Example: Connecting to a full server
You create a service that lets people chat in an open setting. The problem is your business is getting too popular and your chat server can't keep up. To fix this you limit the amount of people who can be online at once. This works but you people are getting mad that they can't join when it is full. To appease the people you implement a queue for when the server is full.

The code might look like this:
```python
# ==================================
# Code for incoming connection.
# ==================================

server = Server()
client_queue = []
connecting_client = incomingConnection()

if server.full() == true:
	client_queue.append(connecting_client)

while client_queue.size > 0:
	if server.full() == false:
		server.connect(client_queue.pop(0))

# ==================================
# Code for chat server.
# ==================================
```

With this when a new client wants to connect to the server that is full, they are placed in the back of a queue, waiting for an open spot. When a spot does open up the person in the queue the longest gets admitted.

## You Try: Deck of Cards
You have made a program that will let two people play a game of cards. You have everything figured out except how to keep track of the cards in the deck.
Using queues make a deck of cards and pull the top card.

Click here for the [Solution](1-answer.md).