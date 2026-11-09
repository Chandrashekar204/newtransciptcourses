# 8.7 — Queue: Enqueue

> Section 8: Stacks & Queues

So now let's create our method for enqueue. And enqueue is adding something to the line. Adding something to the queue. Except our queue is going to look like this, and adding something to the end of the queue will look something more like this. That's what it looks like if we have items already in the queue. If we have an empty queue, we're going to have first and last point to the new node. So our method name is going to be in queue. Our return type is void because we're just adding something to the end of the queue.

And then we'll pass this a value. And we'll use that value to create our node like this. That will add to the end of the queue. So let's start with adding this to an empty queue, where we're going to have first and last point to this new node. To do that, we have to test to make sure that the queue is in fact empty. So I'll say if the length equals zero. Or you could say if first is equal to null. Either way we'll set first to be equal to new node like this.

And then we'll say last equals new node. And now first and last both point to the new node. So let's put this in with the rest of our code. That was for if we had an empty queue. If we have items in the queue we'll say else. And let's build out this else statement. We'll say last dot next equals new node. That is last dot. Next equals new node. Then we'll say that last equals new node, and that moves that over and adds that into our queue. So let's take this code and put it in with the rest of our code.

The only thing left to do now is to increase the length by one. So that's our entire enqueue method. We'll look at this code in a moment in IntelliJ. And when we do we will create a queue with one item in it with a value of one. Then we will enqueue another node with a value of two. And we'll print this out. And we should have one and two. Now let's flip over to IntelliJ and take a look at this. So there is our enqueue method there. That is part of our queue class.

And then I'll come up here to this tab that takes us to our main class that contains our main method. And this line of code here is going to create our new queue with a node with the value of one. And then with this line here we will print out that queue and I'll run this. And you can see that our queue has one item with a value of one. So now we'll come over here. And I'll add this line of code, and this line will enqueue a new node with a value of two.

And then we'll print out our queue again. And we should see one and two. And I'll run this and you can see that our queue now has one and two. All right. And that is our method for enqueue.

----------------------------------------
