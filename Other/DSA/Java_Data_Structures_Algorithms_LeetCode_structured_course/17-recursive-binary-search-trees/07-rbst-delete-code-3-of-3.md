# 17.7 — rBST: Delete Code (3 of 3)

> Section 17: Recursive Binary Search Trees

So now this is going to be our final video for the delete node method. In the last video we wrote code for these situations. And this is the code that we wrote in this video. We'll write code for this situation where the node that we're trying to delete has a child node on each side. And for this situation we'll say else and then we'll build out this else statement. So for everything we're going to do in this video, this 21 node is going to be current node.

And remember from the intro video that we need to find the lowest value in that subtree on the right. And this is where we use that helper method that we wrote in the last video. So we'll say subtree min is equal to min value of current node dot right. Which is this node here. And the minimum value in that subtree is going to be that number 24. So I'll highlight that. So for our next step we need to take that 21 node and change its value to 24. And we'll do that like this.

Current node dot value equals subtree min. And that changes that value to 24. So now at this point we have 224 nodes in the tree. And we need to delete the one at the bottom. And we've already written all the code for deleting a node. We just have to call another instance of delete node to delete that second 24. So in order to do that, we're going to have to traverse to the right of this node and traverse through this subtree. So we'll say current node dot right equals delete node on current node dot right.

And we'll pass it subtree min. So it will go through that subtree. And look for the number 24 and delete it. And these three lines of code are all that we need to delete a node that has two child nodes. So now I am going to bring back this 24 node. And I want to point something out. This node will always be open on the left. So if you remember from the last video when we wrote the min value helper method, in order for this to be the minimum value in the subtree, it has to be open to the left.

So it can either be a leaf node or be open to the left and have a node on the right. So now let's bring this code back and I'll take that and move that down to here. So we can bring back the rest of our code. And this is a good amount of code here. So I want to walk through this and talk about the logic of it top to bottom. All of this code at the top here is going to traverse left and right. And either determine that the value that we're looking for is in the tree or it is not in the tree.

So specifically this code here is what does the traversing. And let's say the value is not in the tree. It's going to trigger this if statement. Or we will traverse left and right. And we find the value that we're looking for. And it triggers this else statement. So if you do trigger this else statement there are four possibilities. First it could be a leaf node. It could be a node that is open on the left and has a node on the right. It could be a node that is open on the right and has a node on the left.

Or it could have a node on the left and the right. So if you look at the logic of this top to bottom, it's not really that hard to follow. So now let's go take a look at this code in IntelliJ. So there is that delete node method that we were just looking at. And this method down here is the overloaded method the one that is public that will actually call. So I'm going to come up here to our main class that contains our main method. And what we're going to do here is create a binary search tree that is 213.

It will be like this when we're done. And then with this code we're going to print that out root and root left and root right. And we should get 213. And then I'm going to scroll up here. And then we'll run delete node on the value of two. And then our tree should look like this. And then I'll press. Sent us out again and we should get three one null. So I'll run this and you can see that to begin with, our binary search tree was 213. And then we deleted the two node and it is three one null.

And that is our method for delete node.


########################################
