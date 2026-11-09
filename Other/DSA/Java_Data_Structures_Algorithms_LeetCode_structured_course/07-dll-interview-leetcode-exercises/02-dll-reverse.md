# 7.2 — DLL: Reverse

> Section 7: <> DLL: Interview / LeetCode Exercises

So now we're going to do doubly linked list reverse. We'll start out with this doubly linked list. And in order to be able to keep track of which pointer is a next pointer and which one is a previous pointer, I'm going to change the color on all of the previous pointers. And when we're done, we're going to have a doubly linked list that looks like this. But we're going to start out like this. And we're going to need a couple of variables. I'm going to call this one current.

We're going to set that to be equal to head. And then we'll have another one called temp that doesn't point to a node. And we're going to start out by having current previous be equal to current. Next like this. And we're going to have current next be equal to temp. Which means it is not going to point to a node. And then we'll set current to be equal to current previous which will move it up to the next node like this. And now that it's pointing to the two node current, previous is pointing to the one node.

We're going to have temp be equal to current previous which is going to move that up. And then we're going to do the same thing where we swap these. And we're going to move these up swap these and move these up and swap these and so on like this. And then in the last iteration, current is not going to be pointing to a node. And that's what's going to break us out of our loop. So I'm going to go ahead and remove those. And then the other thing that we need to do is we have head and tail pointing to these nodes.

And we need to swap them. So now all of the previous pointers are pointing to the right. And the next pointers are pointing to the left. Let's go ahead and flip all these over. So they're pointing in the right direction. And that is how we do. Doubly linked list reverse.

----------------------------------------
