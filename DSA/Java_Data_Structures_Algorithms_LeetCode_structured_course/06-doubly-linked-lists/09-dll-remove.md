# 6.9 — DLL: Remove

> Section 6: Doubly Linked Lists

Now we're going to create our remove method and remove is going to look like this. We'll remove a node at a particular index and we will return it. And of course technically we are returning the pointer to that node. So let's bring up our doubly linked list. And as always, we need to check to see if that index that we're trying to remove is in range. So we'll say if the index is less than zero or if it's greater than or equal to the length, we're going to return null.

And then if we try to remove the item at the index of zero, we've already written a method for this. So we'll say if the index is equal to zero we'll return remove first. And we've also written a method for removing an item on the other end. So we'll say if the index is equal to the length minus one, we'll return remove last. So now let's look at all three of these if statements. Now let's bring back our doubly linked list. So now let's write the code for removing an item somewhere in the middle of the linked list.

We'll remove the item at the index of two. So since we will be returning this item, we will need a variable to point at this, and at the end of the method we will return temp. And we're going to look at a couple of different ways that we can do this from here. What we could do is bring in a couple of variables. We could call them before and after. And the way that we would use these is when this is removed. We could say that before dot next equals after and after dot previous equals before.

And this would be my preferred way of doing this because it is very readable. But I'm going to show a different way of doing this. I'm going to remove both of these, and we're not going to use those in this implementation. Going to bring this back, and I'm going to show you how we can do this with only one variable. And like I said, this is not the way I would do it normally because I think the other way is more readable. But I'm going to do it this way to teach a different concept.

So now let's create this temp variable. We'll do that like this temp equals get at the index where we're trying to remove a node. And let's look at this in with the rest of our code. And we'll bring back our doubly linked list. And since this is the one we're going to remove, I'm going to put this up here. And now I'll show you how we can do this with just one variable. So we're going to start out by moving these two arrows and having them point like this.

So let's put this back and look at how we do this with one variable. So we're going to say temp dot next dot previous. This is the arrow that we're going to move. We're going to set it equal to temp dot previous. So this is the line of code here. Temp dot nextprevious equals temp dot previous. And that moves that over there. And now we'll say temp dot previous dot next. That's the arrow we're going to move. Now we're going to set that equal to temp dot next.

And this is the line of code that does that temp dot previous next equals temp dot next. And that moves that arrow over there. Now we want to set these two arrows to be equal to null. And we'll do that like this. Temp dot next equals null and temp dot previous equals null. And that does this. And that removes the node from the doubly linked list. So I'll take this off the screen and we can decrement the length and then we will return temp. Which returns that node.

So now let's look at all of this and with the rest of our code. Like this and that is the entire remove method. We'll look at this code in a moment in IntelliJ. And when we do, we'll build this doubly linked list with zero, one and two. And then we'll remove the item at the index of one which will also have a value of one. And then we'll have a linked list with zero and two. So now let's flip over to intelligence and take a look at this. So there is our remove method there, which has been added to our doubly linked list class.

And I'll come up here to this tab which takes us to our main class which contains our main method. And these lines here create our doubly linked list with values zero, one and two. And this line here will print out our doubly linked list. So I'll run this. And that gives us zero, one and two. So I'll come over here. And I'll paste in this line, which will remove the item at the index of one. And then we will print out our linked list again. And now that that item at the index of one has been removed, our doubly linked list just contains nodes with values of zero and two.

And that is our method for remove.


########################################
