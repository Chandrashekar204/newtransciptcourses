# 17.1 — rBST: Contains

> Section 17: Recursive Binary Search Trees

So in this section we're going to revisit binary search trees. And we're going to start out by redoing the contains method. We already did this previously in the previous binary search tree section. But when we did this there we did it iteratively, which is to say that we used a loop. And now we're going to write it recursively. So we'll start our code out like this. And we'll call it our contains for recursive contains. But notice that this is private.

So an end user is not going to call this method directly. And the reason for that is we need to kick this off by passing this the root node. And then of course we'll pass it the value that we're checking to see if the binary search tree contains that value. But the method that an end user will use to call this will be this method here. And notice that it has the same name. This is called method overloading, and Java will know which one you're calling based on what arguments that you pass it.

If you call our contains with only an integer, Java will know that you're calling this second method, and when you call this, it will pass that value down to here. And then it will call our contains with the root and the value. Now the first situation that we're going to code for is when we have an empty tree. Because obviously the tree is not going to contain the value that you're looking for if the tree is empty. So we're going to say if current node is equal to null.

And remember that current node in this case is the root, then we're going to return false. But let's say that we're looking for the number 47. And root is pointing to the 47 node. In this case we'll say if current node value is equal to the value that we're looking for we'll return true. Now where this becomes more complicated is if you're looking for a value that is further down in the tree. So let's say we're looking for the number 21. If this is the case, we have to traverse through the tree to get to that node.

So I'm going to bring up a call stack on the right. And we'll kick this off by calling an instance on the root. And then I also have that 21 there because that's the value that we're looking for. So now we'll say if the value that we're looking for is less than current node dot value. And that is the case here, we're going to return our contains. That's where this is recursive. And then we'll call this on current node dot left. And we'll also pass this instance that value of 21.

And then we'll add this to the call stack. So now this is the active instance on the call stack. And we start from the top. We'll say if current node is equal to null. And that is not the case here. So we move down to here and say if current node dot value equals value. And that is the case here, we're going to return true. And when it returns it it's going to return it to the calling method. And once it does that this is popped from the call stack.

So now this is the active instance. Again the last line that it ran was this one. And this portion of this line is what called that method that we just popped from the call stack. So when it returned true, it's specifically returning it to here. And this has a return statement as well. And the place is going to return it to is the calling method. And specifically it's going to return it to this portion here. And when it returns that this gets popped from the call stack.

But this has a return statement as well. And this is going to return this to the original method call. It's going to return it to here. So this is how you have true returned all the way back to where you called this. So now let's look at a situation where we're looking for a value that is not in the tree. So once again we're going to look for the 21 node. And I'll add this to the call stack. And this if statement is what applies. 21 is less than current node dot value.

But in this case current node dot left is equal to null. So. Are going to call an instance on null. And now this is the active instance on the call stack. And we start at the top and say if current node is equal to null. And that is the case here, we're going to return false and we'll return false to the calling method. And this gets popped from the call stack. Now this is the active instance on the call stack. This is where it left off. And false is returned to here.

So when this method returns false it will return it to the calling method which returns it to here. And that will cause this to be popped from the call stack. And this in turn will return false to here. Now to this point, all we have done is traverse left, and we also obviously need to be able to traverse to the right. And I'll bring in this code as well. And that will allow us to traverse to the right as well. And that is all of the code for this method.

And remember we kick all of this off by calling this method. And now that is all of the code. So we'll look at this in a moment in IntelliJ. And when we do we're going to build this tree here. And we're going to call recursive contains on the number 27. And that should return true. And then we'll call recursive contains on 17 which if it did contain it would be here. And that should return false. So now let's flip over to IntelliJ and take a look at this.

So there are the two are contains methods that we just wrote. Then I'll come up to the main tab up here that contains our main method. And I'll click on that. And this is going to create that binary search tree that we just saw in the diagram. And with these lines here we're going to run our contains on the number 27 and the number 17. And I'll run this. And you can see that when we run this on 27 we get true. And when we run it on 17 we get false.

And that is our method for recursive contains.

----------------------------------------
