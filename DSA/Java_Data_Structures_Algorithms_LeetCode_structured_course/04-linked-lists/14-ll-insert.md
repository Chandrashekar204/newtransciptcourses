# 4.14 — LL: Insert

> Section 4: Linked Lists

Now let's create our insert method. So with insert we're going to insert a new node of a particular value at a particular index. And then we'll return either true or false as to whether we were able to insert that node. So I'll bring up our linked list. Like this. And this will be our new node that we're going to insert. So if you look at the different places where we can insert this node, just like with Get and set, we can't insert this at an index that is out of range.

So we can't insert this at the index of negative one. Or we could say an index less than zero. And then we also can't insert this at the index of five. Or we could say at an index greater than the length. So we can create an if statement that says if the index is less than zero or the index is greater than the length. We'll just return false. So now let's look at if we insert this at the index of zero. We've already created a method to insert an item at the index of zero.

And that is prepend. So we'll say if the index is equal to zero. We'll run the prepend method. So at this point we are done running code. We just need to have a return statement. And because we are returning a boolean, we will return true. Also, we could insert this on the other end of the linked list. And this is also something that we've written a method for. So we could say if the index is equal to the length. We're just going to run the append method and once again we'll return true.

So now let's look at all three of these if statements. This is if we have an index that's out of range. This is if we're at the index of zero, and this is if we are adding something to the end of the linked list. So now let's look at what we do. If we insert something in the middle of the linked list, let's say we're going to insert something at the index of two. That would look like this. When we're done, I'm going to put this back. In order to do this, we're going to need a variable that points to the node before the index where we're going to insert it.

And the reason for that is we need to redirect this arrow to point at the new node. If temp is over here, we don't have any way of getting to that arrow. So it has to point to this node. So now let's write the code to create this node. It'll look like this. We've seen this a few times now. And then for our temp variable we'll do this. Temp equals and then we'll use the get method. And then we'll do index minus one. And that puts it at the node one before the index.

So now let's look at this in with the rest of our code. This is what we have so far. And now let's bring back our linked list. So we want to have that arrow on that new node. This one right here new node dot. Next we want to have that point at that 23 node. So we need to set that to be equal to something that is already pointing at the 23 node. And the arrow that is pointing to the 23 node is temp dot. Next. So we'll set these equal and we'll do that like this newnode.next equals temp dot next.

Then we want to say temp dot next. Is equal to the new node. We'll do that like this. Temp dot next equals new node. And that adds that into our linked list. So now let's look at these two lines. And with the rest of our code like this. Now we just need to increase the length by one. And then we'll return true. And that is our entire method for insert. So we'll look at this code in a moment in IntelliJ. And when we do. We will create this linked list with values of zero and two, and then we will insert a node with the value of one at the index of one.

And then we'll have zero one, two. So now let's flip over to IntelliJ and take a look at this. So there is our insert method there added to our linked list class. And I'll come up to our main tab up here. And this is where we create our linked list with values of zero and two. And we'll print it out with this line here. And I'll run this. And that gives us a linked list with the value of two that I'll come up here. And I'll add this line here where we insert at the index of one a node with a value of one.

And then we will print this again. And you can see our linked list is now 012. And that is our method. For insert.

----------------------------------------
