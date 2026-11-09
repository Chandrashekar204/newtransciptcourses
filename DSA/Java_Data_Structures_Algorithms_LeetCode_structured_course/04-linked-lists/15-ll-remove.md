# 4.15 — LL: Remove

> Section 4: Linked Lists

Now we're going to create our remove method. So in this method we are going to remove an item at a particular index. And then we'll return the pointer to that node. So we have access to it. So we'll bring up our linked list. Like this. And just as we've seen before, we can't remove an item out of range. So we can't have anything at an index less than zero, and then we can't have anything that is greater than or equal to the length. So we'll say if the index is less than zero or the index is greater than or equal to the length.

We're going to return null. So I want to point something out about this if statement. I'm going to bring this code back here for our remove method. And I'm going to compare this to our insert method because both of these had if statements for if something was out of range, but one of them returns null and the other one returns false. So why is that? Well, the reason is because remove has a return type of node. And if you're not going to return a node, you're going to return null.

Whereas the insert method has a return type of boolean. So that is why we return false. So let's bring our linked list back up here. So one of the things that we've already written code for is if we remove the first item. So we'll say if the index is zero, we will return remove first. So I'm going to do this same thing again where I bring this back and compare it to what we did in the insert method. So up here in the remove method we're actually returning the method remove first.

Whereas in the insert method we ran prepend. But we put the return statement on a separate line. So the reason for this is that remove first it's return type is node. And because it has the same return type as remove. You can put it right into the return statement. Whereas prepend had a return type of void, and since insert has a return type of boolean, you cannot put prepend in the return statement. You would only be able to put prepend in the return statement here if prepend returned a boolean.

So you run, prepend, and then you have a separate line with a return statement that will return the boolean. So now let's bring our linked list back up here. You could also remove this item. So we'll say if the index is equal to the length minus one, we will return removelast. And once again, because removelast has a return type of node, we can put this right into the return statement. So the other option of course is that we are going to remove something in the middle.

So we're going to remove this item at the index of two. And since we want to return this item we'll need to have a variable that points to it. We'll call this temp. But we also need a separate variable that points at the item before this index I'll call this previous. And the reason we need this is when we remove this, we need that arrow from that three node at the index of one to go over here. So we have to have a variable to the left of that to be able to get to that arrow.

So I'll bring this back. So now let's create these two variables so we can have previous point to that one node by saying previous equals get at index minus one. But we don't want to use the get method for the temp variable. And the reason why is that the get method is O of n. And there's a way of doing this where we can have the temp variable point to the index of two and have it be o of one, and we do it like this temp equals. Previous. Next. So now let's look at this with the rest of our code.

This is what we have so far. And now let's bring back our linked list. So let's move this node up here since that's the one we're going to remove. So the first thing we'll do is have that arrow that's going from the three to the 23 and point it at the seven node. In order to do that that is previous dot. Next we want to set that equal to temp. Next. We'll do that with this line of code. Previous next equals temp dot next. And that points that down there.

Then we want to disconnect that arrow that's going from the 23 to the seven node like this. We'll do that with this line of code temp dot next equals null. And that removes that from the linked list. And now that that has been removed we can decrement the length by one. And then we will just return temp. Like that. So let's look at this with the rest of our code. And that is the entire remove method. And we'll look at this in a moment in IntelliJ.

And when we do we'll create this linked list. And we'll remove the item at the index of two. And we will be left with this linked list 11 three and seven. So now let's flip over to IntelliJ and take a look at this. So there is our remove method there added to our linked list class. And that I'll come up here to our main class with our main method. And these lines here create our linked list with 11, three, 23 and seven. And this line here will print that out and I'll run this.

And this shows we have a linked list with 11, three, 23 and seven. So I'll come up here. And I will add this line. Which will remove the item at the index of two, and then we'll print out our linked list again. And I'll run this. And you can see we now have a linked list with the values 11, three and seven. And that is our method for remove.

----------------------------------------
