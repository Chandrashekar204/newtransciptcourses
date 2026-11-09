# 17.6 — rBST: Minimum Value

> Section 17: Recursive Binary Search Trees

In this video, we're going to write a helper method that finds the minimum value in a particular subtree. I'm going to bring up a binary search tree, and you can tell by looking at this that the minimum value in this tree is 18. But we have to write an algorithm that can determine that. And the way we do this is we start at the root and then we go left, and we go left again. And this time when we go left, left is null. And that's how we know that 18 is the minimum value in this tree.

So the node with the minimum value will always be open on the left. So this method that we're writing will also work on a subtree. So we could pass it that 76 node. And I'll gray out the rest of the nodes here. And you can see in this subtree that the minimum value is going to be 52. And we'll find this the same way. We'll go to the left. And if we go to the left again and it's null, we'll know that the 52 is the minimum value. So let's put the tree down here in the corner.

And then we'll start writing our code. Since this is a helper method we could make this private. But I want to test this code at the end of the video. And that's why I'm writing this as public. So we'll pass this a node that we'll call current node. And to begin with we're going to start with the root. And then we'll say while current node dot left is not equal to null. And that is the case here. We're going to set current node to be equal to current node dot left which moves that down.

So now we'll run this while loop again. And then we'll say while current node dot left is not equal to null, we'll set current node to be equal to current node dot left and move this down again. But now when we run this while loop current node dot left is equal to null. That breaks us out of this while loop and we'll return current node dot value. So I want you to notice that we're not returning current node. We're returning current node dot value.

So it is that value of 18 that is being returned. So now let's look at running this same code on this subtree where we pass it the 76 node. We'll say while current node dot left is not equal to null, we'll set current node to be equal to current node dot left and move that down. But now current node dot left is equal to null. It breaks this out of the while loop. And then we return the value of 52. And that is all of the code for min value. So we'll look at this code in a moment in IntelliJ.

And when we do we'll run it with this line that runs this on the root. And we're running it on this same binary search tree. And that should return the value of 18. And then we'll run min value again on that 76 node. We'll do that with this line of code where we run it on root dot. Right. And that should return the value of 52. So now let's flip over and take a look at this. So there is the min value helper method that has been added to the binary search tree class.

And then I'll come up here to our main class that contains the main method. And this creates that binary search tree that we just saw. And then these are the two lines that run min value on the root and root dot. Right. And I'll run this and you can see that this is returned 18 and 52. And that is our method that finds the minimum value.

----------------------------------------
