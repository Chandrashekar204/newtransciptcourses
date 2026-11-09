# 4.13 — LL: Set

> Section 4: Linked Lists

Now let's create our set method. And just like with the get method, I think the easiest way to show what we're going to do here is to just show the first line of the method. I'll bring this up. So we are going to set the value of a node that is at a particular index. And we're going to return a boolean. Either we were able to set that value or we weren't. So if you are going to code this, go ahead and pause the video here. Otherwise I will get into the set method.

So we'll bring up a linked list like this. And we'll need a variable to point at the node that we're changing the value of. We'll call this temp. It will iterate through the list. Let's say we're going to change the value of the node at the index of one. And we're going to change that from a three to a four. We'll need that temp variable to be able to do that. I'm going to change this back to a three for now, but we'll start out creating the temp variable like this.

So there are some similarities between the set method and the get method and the get method. We couldn't have anything out of range, anything that was greater than or equal to the length. And we couldn't have an index that was less than zero. In these cases, the get method returned null. Otherwise it returned temp which was pointing to a node. So what we can do here with the temp variable is we can leverage the get method. So we'll set temp to be equal to get.

And that will pass the get method the index. And when we do the get method is going to do one of two things. If the index is out of range it will return null. Otherwise it's going to return a pointer to a node. So now we just have to test to see is temp pointing to a node or is it pointing to null? So we'll say if temp is not equal to null. In other words, if it is pointing to a node, then we'll say temp dot value equals the value that we pass the set method.

And in this case it was four. So we will change that to a four. And then after we change that, we'll return true. Then the other possibility is that the Get method returned null because the index was out of range. And if that happens, this if statement, the conditional is going to be false. And we'll skip that and we'll skip down to this line and return false. And that is the entire set method. So the code here is pretty concise because we can leverage the code and the get method.

So we'll look at this code in a moment in IntelliJ. And when we do we're going to create this linked list here. And then we'll change the value of the node at the index of one. And we'll change that from a three to a four. So let's flip over to IntelliJ and take a look at this. So there is our set method there that we've added to our linked list class. Then I'll click on the tab for our main class here that contains our main method. And this is where we'll create our linked list with values 11, three, 23 and seven.

And with this line of code here we will print out that linked list and I'll run this. And our linked list has 11, three, 23 and seven. So I'll come over here and I'll add this line of code. We'll say my linked list dot set at the index of one. We're going to change that value to four. And then we will print the list again. And I'll run this. And you can see now that that second item in the linked list at the index of one has had its value changed from 3 to 4.

And that is our method for set.

----------------------------------------
