# 6.5 — DLL: Remove First

> Section 6: Doubly Linked Lists

So now we're going to create our remove first method. So that is going to look like this. We'll remove that node and have head move over like that. And then we have a couple of edge cases. One of them being if we have one item in the linked list and one if we don't have any items in the linked list. If you're going to code this, go ahead and pause it here. Otherwise I will get into the code. So the method is called remove. First. The return type is node.

It'll be that item that we have removed. And our first situation will code for is when we have an empty linked list like this. And to do that we have to test to see if the linked list is empty. So we'll say if the length is zero, we'll return null. So now we'll look at our other edge case for when we have one item in the linked list. So we will need a temp variable to be able to return this node. Or create that like this. Temp equals head. And then we'll say, if the length is equal to one, we'll have head and tail be equal to null.

Like this. So let's add this in with the rest of our code. So we've coded for if we have an empty linked list, and then if we have a linked list with a length of one. Now we'll code for when we have two or more items in the linked list. We'll say else and we'll build out this else statement. So the first thing we're going to do is move that head pointer over one. We'll do that by saying that head is equal to head dot next. And the code looks like this head equals head dot next.

And that moves that over. And now that we have that moved over, we can set head dot previous to be equal to null. Which breaks this connection here. And we'll do that with this line of code. Head dot previous equals null. And then we'll say temp dot next is equal to null. With this line of code temp dot next equals null. And now we can take this and add this in with the rest of our code like this. And now we will decrement the length by one and then return temp, which returns the pointer to that node that we just removed.

So we'll look at this code in a moment in IntelliJ. And when we do we'll create this linked list with the items two and one in them. This way we can test to make sure our code works when we have two items in the linked list and run, remove first and then make sure it works for when we have one item in the linked list. And then we'll run it one more time to make sure it works when we don't have any items in the linked list. So now let's flip over to IntelliJ and take a look at this.

So there is our remove first method there. So we're going to come over to our main tab here. This contains our main method. And this creates our doubly linked list with values of two and one. And then we'll use this line here to print that out. And I'll run this. And you can see our linked list contains nodes with the values of two and one. So what I'm going to do is I'm going to come over here and I'm going to replace this print list line with these lines of code.

And what we're doing here is running the remove first method three different times. We're running it for when we have two items, then one item, then zero items. So I'll run this. And you can see up here that the first two items returned are nodes, and then the third one returns null. So to make sure we are getting the correct nodes I'm going to come over here and add dot value. To these two. And remember, you don't want to add it to that third one because that third one returns null.

It's not returning a node. So I'll run this. And you can see that the nodes that were returned were two and one. Then of course it returns null on the third one. All right. And that is our method for remove first.

----------------------------------------
