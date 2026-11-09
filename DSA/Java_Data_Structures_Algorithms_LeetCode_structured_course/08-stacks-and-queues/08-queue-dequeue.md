# 8.8 — Queue: Dequeue

> Section 8: Stacks & Queues

So now we're going to do our DQ method and DQ is going to look like this. We're going to remove the first item from the queue and then we're going to return it. So we have a couple of edge cases. One is if we have one item in the queue. We saw this with linked lists and doubly linked lists with the remove first method. And then the other edge case of course is if we have an empty queue. So we'll start out our code like this. The return type is node.

That will be a pointer to the node that we have dequeued. And the first of our three scenarios we're going to code for is if we have an empty queue. So we'll say if the length is equal to zero, return null. You could also say if first is equal to null, return null. So now let's code for when we have one item in the queue. The first thing we'll need to do is create that pointer that we're going to return. We'll call it temp and we'll create that like this temp equals first.

And we'll say if the length is equal to one. Was set first and last to be equal to null. Like this. So let's add this in with the rest of our code. This is for if we have zero items in the queue. This is if we have one item in the queue. And now we'll write our code for when we have two or more we'll say else. And let's build out this else statement. Remember we already set temp to be equal to first so it's already pointing to that node. So the first thing we'll do is move that first pointer over one.

We'll say first equals first dot. Next we'll do that with this line of code. First equals first dot next that moves that over. And then we'll say temp dot next equals null. We'll do that with this line of code temp dot next equals null. So let's add this in with the rest of our code like that. Now we just need to decrement the length by one. And then we'll return temp which is that pointer to the node that we dequeued. So we'll look at this code in a moment in IntelliJ.

And when we do we'll create this queue. We want to make sure that our dequeue method works for when we have two items, and then also for when it has one item, and then finally when it has zero items. So now let's flip over to IntelliJ and take a look at this. So there's our dequeue method there that we just added to our queue class. So now I'm going to come up here to this tab and open our main class that contains our main method. And this is where we create that queue with the values of two and one.

And then with this line here, we will print this out and I'll run this. And you can see over here that our queue contains two and one. So now what I'm going to do is come over here and replace this line where we print out the queue with these lines of code here. So all we're doing here is running dequeue three different times, once for when we have two items in the queue and then one item and then zero items. So now I'll run this. And you can see we've returned two different nodes and then finally null.

So for the first two I'm going to come up here and put dot value on the end of each of these. And now I'm going to run this again. And you can see that we've returned the node with the value of two, the node with the value of one, and then finally returned null. So it looks like we have a working method for dequeue.


########################################
