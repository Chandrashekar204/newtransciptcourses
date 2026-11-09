# 17.4 — rBST: Delete Code (1 of 3)

> Section 17: Recursive Binary Search Trees

In this video, we're going to start writing the code for deleting a node from a binary search tree. And we'll start our code off like this. And just like we have seen with recursive insert and recursive contains, this is going to be private. And for the same reason we have to kick this off with the root node. So we're also going to have this method that we pass a value to. And then this will pass the root and the value to this method. So we'll bring in a tree and the call stack.

And what I'm going to start out with here is looking for a value to delete that is not in the tree. So we're going to look for the number 18 and show how that works. And then we'll look at deleting a value that is in the tree. So we'll kick this off with the root node. And as we build this out I want you to notice the similarities between the delete node method and the recursive insert method. So we'll say if the value that we're trying to delete is less than current node dot value, and it is, we're looking for the number 18.

Then we're going to say current node dot left equals delete node. This is where it's recursive. And then we'll call that on current node dot left. And I'll add that to the call stack. And then we also pass this method the value of 18. So now this is the active instance on the call stack. So then we'll say if the value that we're looking for 18 is less than current node dot value, then we'll run an instance of delete node on current node dot left.

And in this case current node dot left is null. So we're calling an instance on null. And now this is the active instance on the call stack. And it is also our base case. And to this point returning null is the first thing that is different than the insert method. And we will return null to the calling method down to here. And this gets popped from the call stack. So now this is the active instance. Again this is the last line that it ran. And this portion here is what called that instance that we just popped from the call stack that returned null.

So we're setting current node dot left to be equal to null which doesn't change anything. And just like we did in the insert method we're going to return current node. So current node is that 21 node. And we are returning it to here. And when we do that this gets popped from the call stack. So now this is the active instance on the call stack. Again this is the last line that it ran. This portion here called that method that we just popped from the call stack.

So we're setting current node dot left to be equal to this 21 node. And that just makes it where the 47 node continues to point at the 21 node. And then we return current node. And this gets returned to the calling method like that. And this is popped from the call stack. We have written this code to traverse left. So then I will also add the code to traverse right. So now let's look at deleting a value that is in the tree. We're going to delete the value of 21.

And we'll start out by calling an instance of delete node on the root. And since 21 is less than, we're going to go to the left and add an instance on the 21 node. So now this is the active instance. And 21 is the value that we're looking for. So let's start at the top. And current node is not equal to null. But because 21 is equal to current node it is not less than and it is not greater than it is equal. So we will say else. And this else means that we have found the value that we're looking for inside of this else statement.

We need to deal with four different situations. Either the node that we're trying to delete is a leaf node, or it has a node on the right, but not one on the left, or it has one on the left, but not on the right, or it has a node on each side. In the next video, we'll write code for all three of these situations. These are the easier ones. Then we'll take two videos to write the code for that. This situation. One of those will be a helper method called minimum value.

But like I said in the next video, we'll write code for all three of these situations. But for now that concludes Delete node part one.

----------------------------------------
