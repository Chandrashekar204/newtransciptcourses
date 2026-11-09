# 18.9 — DFS: InOrder - Code

> Section 18: Tree Traversal

So now we're going to write our code for depth. First search in order, and I'll bring up our tree and our call stack and start writing our method like this. And of course we're going to start out by creating that results array list like this. And just like we did for preorder and Postorder, we're going to have a class called traverse that contains a method called traverse. And I'm going to bring in our code that we use for preorder. That was like this.

And Postorder had our code like this. And as you may have guessed in order. It's going to be like this. And just like we've done before, we're going to kick this off by calling traverse on the route. So I'm going to remove all of this code and focus in on this traverse method and bring all of these items back up. And we kicked this off by calling traverse on the route. Which does this. And then 47 is going to look to the left, and that's going to add the 21 onto the call stack.

And the 21 is going to look to the left. And that's going to add the 18 to the call stack. So to this point the tree and the call stack look identical to what it did with Post-order. But with in-order we're going to do this line next and add the value to the results array list. And that colors the 18 in orange. And then the 18 is going to look to the right. And there's not an item there. So we pop that from the call stack. Now the 21 is at the top of the call stack.

It's already looked left. Now we can write its value to results. And then it's going to look to the right. And that adds 27 onto the call stack. It's going to look left and then it's going to write it's value 27 to results, and then it's going to look to the right. And there's not a node to the right. So this is done running. And we can pop that from the call stack. So now the 21 is at the top of the call stack. Again it's gone to the left. It's written its value to the results array list and it's gone to the right.

So now we can pop that from the call stack. So now the 47 the root node is at the top of the call stack. Again it's gone to the left. Now it can write its value 47 to results. And now it will go right. So now that adds the 76 node to the call stack. And the 76 node is going to look to the left. And that adds the 52. The 52 will look to the left and then write its value to results. And then it will look to the right. And there's not a node to the right.

So that's done running and we'll pop that from the call stack. So now the 76 is at the top of the call stack. Now it has already gone left. Now we will write its value to results. And then go to the right that calls traverse on the 82 node. And now that instance of traverse is going to look left. It's going to write the value 82 to results. And then look to the right. And since there's not an item on the right we can pop that from the call stack.

So now the 76 is at the top of the call stack. It has gone to the left. It is written as value to results. And it has gone to the right. So we can pop that from the call stack. And the same is true for the 47. It has gone left. It has written its value and gone right. And we can pop that from the call stack. So we've written all of our values to the results array list. And you can see here that the numbers are all in numerical order, hence the name depth.

First search in order. So let's bring back the rest of our code. And the only thing left to do is to return that results array list. So we'll look at this code in a moment in IntelliJ. And when we do we'll create this binary search tree. And then we'll run depth first search and order. And we'll expect to see this array list returned. So now let's flip over to IntelliJ and take a look at this. So there is our depth first search in order method there that's been added to our binary search tree class.

And I'll come up here to our main class that contains our main method. And these lines will create a new binary search tree just like we saw in the diagram. And then with this line here we'll run depth. First search and order on that binary search tree and print that out. And I'll run this. And you can see that we have returned an array list with all of the values, and our binary search tree returned in order. And that is our method for depth first search in order.


########################################
