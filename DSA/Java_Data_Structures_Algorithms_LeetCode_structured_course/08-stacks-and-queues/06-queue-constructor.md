# 8.6 — Queue: Constructor

> Section 8: Stacks & Queues

So now let's create our constructor for our queue. So we said that a queue was basically like a line first and first out, except our queue is going to look like this, where the person first in line is on the left and the person last in line is on the right. So to build our constructor for this, the first thing we need to do is build our node class. And we had said that a node is similar to a HashMap. So our node class is going to have two class variables value and next with next being a pointer that can point to another node.

And then with the constructor itself we pass it a value. And then we assigned that value to this dot value. So this node class is identical to the one that we use for linked lists, and identical to the one that we used for stacks. So now let's build our queue class. So this will have three class variables. We'll start with first and last. That's going to point to the first and last item in the queue. And then we'll also keep track of the length.

So now let's build out our constructor for the class. It has the same name as the class. We call it queue. We'll pass it a value. And to build this out, I'm going to just focus on this. We'll pass that value that we pass the Q constructor to the node constructor and use that to create this node. Then we'll have first and last both be set equal to the new node like this. And then we'll set the length equal to one. Since this q now has one node in it.

So now let's bring back the rest of our code for the queue class so we can see all of this together. And now I'm going to focus back in just on the constructor like this. We would create a new queue. In this case I'm calling it my queue with a line of code like this. And this line of code will create all of this. It will create that first node with a value of seven. It'll create first and last, and point it to the new node and set the length equal to one.

So we'll take a look at all of the code that we've written for the node and queue classes in a moment. And when we do, we'll run this line of code and create this queue and IntelliJ. So now let's flip over and take a look at this. So the first thing I want to do is come over here and show that we've created a new package called queue that is lowercase q for the package. And it contains two classes which are queue. And main classes of course are uppercase.

And these queue and main classes I have those tabs open up here. So I'm going to close this side panel. So this is all of the code that we wrote to create our queue and node classes. The node class is an inner class inside of our queue class. And then I'm just going to scroll up here and I've created a print queue method. And then one for get first, get last and get length. So you can copy and paste these into your code. And you can run these to have visibility into your queue for troubleshooting purposes.

Then I'm going to come up here to our main tab that has our main class which contains our main method. And with this line of code here we are going to create that queue that we just saw, that just had one item with a value of seven. And then we're going to run, get first, get last get length and then print queue. So I'll run this. So you can see that first and last both point to that seven node. The length is one. And then when we run print Q we just get that one node with a value of seven.

And that is our cue constructor.

----------------------------------------
