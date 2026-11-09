# 4.11 — LL: Remove First

> Section 4: Linked Lists

Now we're going to create our method for removing the first item from the linked list. It will look like this. We'll move head over to this node. We'll remove this node and we'll return it. So we have a couple of edge cases here. The first one being when we have one item in the linked list. We saw this with the remove last method as well. And then of course if we don't have any items in the linked list at all. So if you want to code this go ahead and pause it here.

Otherwise I'm going to get into the code. So the name of the method is remove. First, the return type will be node. And this will be the first situation that we code for, for when we have an empty linked list and it'll look like this. If the length is zero, we'll return null. And once again, a common way of doing this is saying if head is equal to null, return null. And now let's look at when we have multiple items in the linked list. So what's that first item, the 11 node that we're going to be removing.

And because we want to return this we need to have a variable set equal to that node. We're going to call it temp. And we'll create that variable like this. It will be of type node. And we'll say that temp equals head. And then we're going to move head over to point at that three node. So we'll say head equals head dot next. And that'll move that over. We'll do that with this line of code. Head equals head dot next. And then we need to remove that 11 node from the linked list.

So we'll say temp dot next equals null. Tip next equals null. And now we can decrement the length by one. And this brings us to our other edge case when we have one item and the linked list. So let's walk through these four lines of code and look at what happens in this situation. So we'll start with the first one here temp equals head. We'll bring that in there and remove that line of code. And then next it is head equals head dot next. So head dot next equals null.

So this means head is going to be equal to null. And we'll remove that line of code. There will say temp dot next equals null and temp dot next is already equal to null. So this doesn't do anything. We'll remove that line of code. And I'll also remove temp from our diagram here like that. And the only thing left is we're going to decrement the length by one. So the linked list had started with one item. Now the length is zero. So the problem is that tail is still pointing to that node, even though the length has been set to zero.

So what we're going to say is if the length is equal to zero, let's also set the tail to be equal to null. And that will move that over and point it to null. So let's look at this code in with the rest of our code like this. And just like we had with the remove last method we have if length equals zero here and then we have it again down here. The difference being that this one, the second one happens after we have decremented the length. So the second one applies to a linked list that started with one item in it.

Then we decremented the length and made the length zero. Now the only thing left to do. Is to return temp, and temp is the pointer to the node that we just removed. So we'll look at this code in a moment in IntelliJ. And when we do we're going to create this linked list. Remember we had three different scenarios. The first one was if we had a linked list with multiple items in it, we want to make sure that works when we remove the first item in that situation.

And then we want to make sure that this works when there is one item in the linked list. And then we'll run it a third time when there are zero items in the linked list. But we will start out by having the linked list look like this. Now let's flip over to IntelliJ. So there is our remove first method there that we've added to our linked list class. Then I will come over here to our main tab. And remember this main class is in the same package as our linked list class.

And I'll click on this. So this creates our linked list with values of two and one. And I'll print out the linked list here. And I'll run this. And you can see that this has returned a linked list with the values of two and one. So what I'm going to do is I'm going to come down here and replace this line that says print list. And I'm going to paste in these lines of code. So for each of these three lines of code, we're running the remove first method on my linked list.

So we're running it for when the linked list has two items, then one item and then zero items. And I'll run this. And you can see here this returns two nodes and then finally returns null. And for these first two situations where it's returning a node, I'm going to come up here and say dot value and then do the same thing here. And I'll run this again. And you can see that it returns the node with the value of two. Then the node with the value of one and then finally returns null.

And that is our method for remove first.

----------------------------------------
