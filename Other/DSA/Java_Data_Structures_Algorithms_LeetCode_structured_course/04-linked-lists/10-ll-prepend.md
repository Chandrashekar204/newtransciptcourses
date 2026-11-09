# 4.10 — LL: Prepend

> Section 4: Linked Lists

Now let's create our prepend method. So we'll start out with our linked list like this. And we'll create a node. And we need that new node that for node to point to the 11 node. In other words it needs to point to the same node that head points to. Like that. And then we'll have head point the new node, and that adds that into the linked list. We also need a code for when we don't have any items in the linked list. In this situation, we'll have head and tail point to the new node.

So if you're going to code this, go ahead and pause it here. Otherwise I'll get into the code. So we'll say prepend. We're going to pass it a value. Notice that the return type is void because we're just going to add that to the end of the linked list and not return anything. And the first thing we need to do is create a node. So we'll pass this the value and that creates our node. So let's code for when we don't have any items in the linked list.

This is where we have head and tail point to the new node. In order to do this, we have to test to see if the linked list is in fact empty. And I'm going to do it like this. If length equals zero, and then the other common way to see this is if head equals null. So we'll say head equals new node like this. And then we'll set tail equal to the new node. And now head and tail both point to that node. So let's add this code in with the rest of our code like this.

This is for if we have an empty linked list, and if we have items in the linked list we'll say else. And let's build out the else statement. So we'll say newnode.next equals head. That does this. And then we'll say head is equal to new node, and that moves that over to the new node and adds that into our linked list. So now let's add this in with the rest of our code. And the only thing left to do is to increase the length by one. So we'll look at this code in a moment in IntelliJ.

And when we do, we'll create a linked list with the values two and three. Then we'll prepend a node with the value of one. And then we'll have a linked list that is one two, three. So now let's flip over and take a look at this. So there is our prepend method there. And I'm going to come up here to our main tab. And this is where we create a linked list with the values two and three. And then this line here will print that out. And I'll run this.

And you can see up here that our linked list has the values of two and three. So I'm going to come over here. And I'm going to add this line of code where we prepend the value of one. And then we'll do our print list again and I'll run this. And now this prints out a linked list with values one, two and three. And that is our method for prepend.

----------------------------------------
