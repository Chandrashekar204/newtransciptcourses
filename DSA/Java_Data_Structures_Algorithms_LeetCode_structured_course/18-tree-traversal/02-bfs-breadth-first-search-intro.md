# 18.2 — BFS (Breadth First Search): Intro

> Section 18: Tree Traversal

So in this video, we're going to walk through the steps for breadth first search. And then in the next video we'll write the code. So I'm going to bring up a tree like this. And in breadth first search this is the one where we start at the top. And then we do the next row. And we do this row by row and add these numbers to an array list. So the way we're going to do this, I'm going to move this over to the side. First we're going to have a Q, and then we're also going to have an array list called results.

So in the Q we're going to store nodes. And obviously this is going to be a pointer to a node. But we'll have access to all of the attributes to this node. So I'm going to change this node to look like this I'll keep it as blue since that's the color of our nodes. But it's important to understand that we're not just storing the value. And we will be using the value and the left and the right from that node. So what we're going to do with that node that's in the queue is we will dequeue it and store the value in results.

And I change that color to green because we're only storing the value, not the entire node. And then from that 47 node in the tree, we're going to go left and to the left of the 47 node is the 21 node. We'll put that in the queue. And to the right is the 76 node. And we'll put that in the queue. Then we will dequeue the 21 put its value in results. And from the 21 we're going to go left and add the 18 and then right and add the 27 to the queue. And once we've gone left and right we will dequeue the next item which is 76.

And then from the 76 node we're going to go left. And that is the 52. And right. That is the 82. And now that we've gone left and right we'll dequeue the 18. But the 18 doesn't have anything on the left or the right. So we can just go to the 27. Same thing with the 27. It doesn't have anything on the left or the right. And that is true of the 52. And the 82. And we're going to have a loop that runs until that queue is empty. And when the queue is empty, we know that we have all of the values added to results.

So I'll remove the queue. So now I want to just look at the numbers here and show you the pattern that they're in. If you take this 47 and put it at the top and take the next two and put them here, you can see that this exactly matches our tree. So we will code this in the next video. But for now this is our introduction to breadth first search.

----------------------------------------
