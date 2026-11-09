# 18.7 — DFS: PostOrder - Code

> Section 18: Tree Traversal

So now we're going to write our code for depth. First search post order. We'll bring up a tree like this and our call stack. And we'll begin our method like this. And just like we've done before, we're going to have a results array list. And I'll bring that up on the bottom here. And just like we did with pre order, we're going to have a method inside of this method. And we're going to do that by creating a class called traverse. And then have a method inside of this called traverse.

And I'm actually going to start out by bringing in the exact same code that we used for preorder. So I'm just going to bring this in. This is the preorder code where we added the item to the results array list first, then went left and then went right. To make this post order. We're just going to rearrange this a little bit. So we're going to move that line where we add something to the results array list. To the bottom. And now it's left right.

And then we add the item. And that is the only difference. We'll call this the same way with the root, but it's just the rearranging of those lines of code that are different. And just like we did before, I'm going to focus in on this method and then bring all of this back and walk through this. So we called the traverse method with the root. And we'll add that to the call stack like that. And then on the tree I'm going to color this in green. I'm not going to color it orange until we've written the value to the results array list.

But then we're going to look to the left. And then we're going to call a new instance of traverse on the 21 node and add that to the call stack. Now the 21 is at the top of the call stack, and the first thing it's going to do is look to the left. And now we're going to add the 18 to the call stack. So the ones in green have been visited, but we haven't written any values yet. So now the 18 is going to look to the left. It will look to the right.

And there are no nodes to the left or the right. And now we come down to this line of code and we write the value to the results array list. So that instance of traverse is done running and we can pop that from the call stack. Now the 21 is at the top of the call stack. The 21 is already gone left. Now we can go right. And we'll add the 27 on like that. And now the 27 is going to look left. It's going to look right. And then finally we're going to write its value to results like that.

And we can pop it from the call stack. Now the 21 is at the top of the call stack again. It's already gone left. It has already gone right. So now we can write its value to results. And that one's now done running. So we can pop that from the call stack. And now the 47 is at the top of the call stack. It's already gone left. Now it's going to go right. So that'll add the 76 like that. And then the 76 is going to look left. And that's going to be the 52.

And now the 52 is going to look left. It's going to look right. And then write its value to results like that. And now we can pop that from the call stack. Now the 76 is at the top of the call stack. The 76 is already gone left. Now it can go right. And we'll add the 82 like that. And the 82 is going to look left. It'll look right and then write its value to results. So that is now done running. And we can pop that from the call stack. And now the 76 is at the top of the call stack.

The 76 has already gone left. And right now we can write its value to results. And now we can pop that from the call stack. Now the 47 is at the top of the call stack. It's already gone left and right. And now we can write its value to results and pop that from the call stack. So now let's bring in the rest of our code like this. And the only thing left to do is to return that results array list. So we'll look at this code in a moment in IntelliJ.

And when we do we'll create this tree and we'll run depth first search post order on this. And we'll expect to see this array list returned. So now let's flip over to IntelliJ and take a look at this. So there is our depth first search post order method added to our binary search tree class. And I'll come up here to our main class with our main method. And then all of these lines of code here will create our binary search tree that we just saw in the diagram.

And then down here we'll run depth. First search post order on that binary search tree. And I'll run this. And that is the array list that we were expecting. And that is our method for depth. First search post order.

----------------------------------------
