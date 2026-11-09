# 4.3 — LL: Under the Hood

> Section 4: Linked Lists

So now we're going to look at linked lists under the hood. So if we have a linked list and we're going to add this node to the end and we have this node point to the new node and tail point to the new node, and we add this into the list. What is really going on when we do that. So in order to understand this we have to first understand what a node is. So this entire thing is the node. It is both the value and the pointer. It is both things. So a good way of thinking of what a node is is to think of this like a hash map.

It is not technically a hash map, but it pretty much works the way a set of nested hash maps would work. So if we look at our node this way and we're going to add this to our linked list, remember that the seven node is also basically a hash map. So how do we have that next pointer point to this new node. Well we have it point to the new node by just setting it equal to the new node. So if you'll recall from our pointers video, when we set something equal to a hash map, the variable is just pointing to the hash map.

So that is how you have one of these nodes point to the next node. So the same is going to be true of this 23 node and the three node and so on. And that very first node up at the top will have hed be set equal to it. And remember that just makes it where head is pointing to that. And then we'll have tail point to this one over here. So conceptually we can represent the linked list like this. It's a lot easier to understand as a diagram. But it is also important to understand that it's really something more like this.

Under the hood.

----------------------------------------
