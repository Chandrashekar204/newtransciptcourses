# 18.3 — BFS: Code

> Section 18: Tree Traversal

So now we're going to write our code for breadth first search. So I'll bring our tree up like this. And I'll shrink it down into the corner to make room for our code. So we're going to start our method out like this. And this method is going to be inside of the binary search tree class. So the return type will be an array. List of integers. All of the integers from this binary search tree. So we're going to create a few variables here I'm going to create a variable called current node.

And we're going to set that equal to the root. And you can see I've colored that in green down here. That current node is going to move through the tree. And whatever the current node is I will color that in green. And then we'll need a queue. And I'm actually going to use the queue that is built into Java. So we'll do that like this. Now notice the Java implementation for the queue uses a linked list. Okay. So once again this is not the queue that we created in the course, nor is it the linked list that we created in this course.

This is the queue and linked list that are built in to Java. Now in the queue section we talked about the best way to implement a queue was with a linked list. And you can see that even with a Java implementation, queues use a linked list. So we'll show that queue down here like this. And then finally we'll create that array list that we're going to return. We're going to call that array list results. So to kick things off we need to add the current node into the queue.

And I'm putting this in here with the graphic that we're using for a node. To emphasize that this queue holds the entire node. It doesn't just contain the value of the node. So I am going to change this graphic to a number in the queue, but I'll leave it blue since that's the color that we're using for our nodes. So if you'll recall from the binary search tree section of the course, one of these nodes contains three parts value left and right. And we will be using all three the value the left and the right.

So now we can bring in the while loop, and this while loop will run until the queue is empty. I'm going to move this up and focus on this while loop now. The first thing we're going to do is remove a node from the queue. We'll do that like this. And we're going to set current node to be equal to that node that we removed. So let's remove this from the queue like that. And remember we're going to use the value and left and right from this node when we remove it from the queue.

So we'll start with value. We will add the value to the results array list. And notice I colored this in green because this is no longer the entire node. This is an integer. The results array list holds a different type. This does not hold the entire node like the queue does. So now we'll look to the left. We'll say if current node dot left is not equal to null. In other words, if there is a node on the left. Then will add that node to the queue.

Like this. Then we'll say if there's a node on the right, we'll add that node to the queue like this. So now we'll run through the while loop again. So these two steps right here I'm going to do these in one step moving forward where we remove the item from the queue and then add it to results. I'll just have that number come straight down from now on. And then we'll check to see if there's an item on the left of the 21 node. There is. And then we'll check to see if there's one on the right.

And there is. And those both get added to the queue. And then we come back up to the top of the while loop. And we'll remove this item from the queue, move that to results, and then we'll add the node to the left of the 76 and the right of the 76. And now we're going to remove that 18 from the queue. Now the 18 doesn't have anything on the left or the right because it's a leaf node. And the same is going to be true of the next three nodes the 27, the 52 and the 82.

And now our queue is empty and that breaks us out of our while loop. So I'll remove the queue from the bottom there. And now let's bring back the rest of our code. The only thing left to do is to return that results array list. So that is all of our code for the breadth first search method. Remember this is going to be inside of the binary search tree class. And we'll look at this in a moment in IntelliJ. And when we do we'll build this tree. And then we'll expect to get this array list returned.

So now let's flip over to IntelliJ and take a look at this. So there is our breadth first search method that we just built added to our binary search tree class. Then I'll come up here to our main class that contains our main method. And with this line here, we'll create a new binary search tree called my binary search tree. And with these lines, we'll build the tree that we just saw. And then down here we're going to run breadth first search and print out the array list that it returns.

And I'll run this. And this is returned the array list that we expected. And that is our method for breadth first search.

----------------------------------------
