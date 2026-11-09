# 17.5 — rBST: Delete Code (2 of 3)

> Section 17: Recursive Binary Search Trees

So in this video, we're going to write the code for when we remove a leaf node, and then the code for removing a node that has a node on the right, and then the code for removing a node that has a node on the left. So we'll code for all three of these. And this is the code that we wrote in the last video. And you can see that we're going to quickly run out of room for code. So what I'm going to do is remove some of the code that we don't need for this video.

So first this code up here only applies if there's a value that we're looking for that is not in the tree. And that's not going to happen in this video. So I'm going to remove that. And also in this video we will only traverse to the left. We will not traverse to the right. So I'm also going to remove this. So we're going to start out by removing the 21 node. When it is a leaf node. And we'll start out by calling this on the root. And the value that we're looking for 21 is less than 47.

So we'll call an instance on current node dot left. And this is the value that we're looking for. And that will bring us down to this else statement. So we need to test to see is this a leaf node. So we'll say if current node dot left is equal to null and current node dot right is equal to null. And that is the case here. Then we're going to return null. So we'll return null to here. And that instance is popped from the call stack. So now this is the active instance.

Again this is the last line that it ran. This portion here called that instance that was just popped from the call stack. So NULL gets returned to here. So we're setting current node dot left to be equal to null which does this and removes that node from the tree. So now I'm not going to walk through all of the steps for popping this last instance off the call stack. We've gone through that a couple of times now I'm just going to pop this off. And now let's look at removing the 21 node when it has a node on the right.

And as always, we'll start this off with an instance on the root. The value that we're looking for is less than 47. So we're going to call an instance on current node dot left. And this is the number that we're looking for which triggers this else statement. So the code that we're going to add here is going to go underneath this if statement. But to make sure we have plenty of room I'm just going to remove this and then say else if current node dot left is equal to null.

And that is the case here we'll set current node to be equal to current node dot right. So current node is the 21 node. And we're setting it to be equal to current node dot right. And then we return current node. So we'll return that pointer to the 22 node to here. And once that's done this gets popped from the call stack. So this is the active instance. Again this is the last line that it ran. And we're setting current node dot left to be equal to that 22 node.

And when we do that that does this. And now that 21 node doesn't have anything pointing to it, which means it will be garbage collected. And then of course this will be popped from the call stack. So now let's look at removing that 21 node when it has a node on the left but not the right. And I'm not going to walk through the steps of this because this will be basically identical to what we just saw when we have a node on the right. The only difference is we are switching right and left.

And other than that this is identical. So I'll also bring in the code for when we have a leaf node. So this covers the code for all three of those situations. We still need to write the code for when the node we're removing has a child node on the left and the right. And when this happens we're going to say else. And we're going to cover writing the code for this situation in the next two videos. In the next video, we'll write a helper method. And then in the following video, we'll use that helper method to build out this else statement.

But for now this concludes delete node part two.

----------------------------------------
