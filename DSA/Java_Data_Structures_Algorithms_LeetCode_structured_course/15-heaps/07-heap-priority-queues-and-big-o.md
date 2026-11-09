# 15.7 — Heap: Priority Queues & Big O

> Section 15: Heaps

So now let's talk about priority queues. And priority queues are most often implemented with a heap, so much so that oftentimes you'll hear people use the terms priority queue and heap interchangeably. So with a priority queue, what you want to do is be able to return the highest priority item in the queue. And you can just intuitively tell that with a heap. A heap is going to be a great data structure for doing that. And the reason why it is almost always used for implementing a priority queue just comes down to big O, but technically you could implement a priority queue with something like a linked list, but returning the maximum value here requires that you iterate through the entire linked list to determine the maximum value, and then return it, and that's going to be O of N.

You could also implement a priority queue with something like an array list. This array list is not set up as a heap. These numbers are just in a random order. So to find the maximum value would require that we iterate through the entire array list. Once again, this is o of n, so you might look at that and say, well, how about using a hash map. Because going to this maximum value would be o of one. The problem with that is you don't know that 95 is the maximum value.

We would have to iterate through all of these to determine that that is the maximum value. Once again, this is O of n. Another data structure that we could use would be a binary search tree. So this is not a heap here. This is set up as a binary search tree. And if the tree is balanced getting to the maximum value, you can just go all the way to the right and that would be log n. Also adding a value. Let's say we add the value of 100. We would iterate through the tree and place that to the right of the 95 node.

That is also log in, but that's only the case if this tree is balanced. But with a binary search tree, it is possible to have something that looks like this. Now, getting to that maximum value requires that we iterate through every item which is O of n. Also, if we added the number 100 once again, we would have to iterate through all of these to place that to the right of the 95. So now let's compare this to using a heap. So one of the things that makes a heap very efficient for a priority queue is that it is always balanced, because the tree is always complete.

Now to understand the big O of a heap, you have to be able to understand how we calculate it. The height of the heap. And we talked about this on the binary search tree section. But the height of the tree is going to be log n. So this tree here is seven nodes. But we'll say this is approximately eight nodes. And the height is three. And log sub two of eight is three. So now that we know that the height is log in, let's look at what happens when we remove an item.

This node gets moved to the top and the farthest that we'll ever have to move. That 50 node is sinking it down the entire height of the tree. And the height is log n. So now let's look at adding a node. We'll add the value of 100. And when we bubble this up the farthest that we'll have to bubble the 100 up is bubbling it up the entire height of the tree. So it doesn't matter if we're doing insert or remove of it is O of log n and O of log n is incredibly efficient.

So if we had a heap with a million items in it, n would be a million and log n would be about 20. So it's a huge difference in efficiency. And that's why you will almost always see a heap being used with priority queues.


########################################
