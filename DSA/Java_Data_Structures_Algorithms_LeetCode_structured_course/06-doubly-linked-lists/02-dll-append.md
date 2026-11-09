# 6.2 — DLL: Append

> Section 6: Doubly Linked Lists

So now let's build our append method. This will be very similar to the append method for a singly linked list. So with a singly linked list we created a node. We had the last node point to the new node pointed tail at the new node and inserted that into the linked list. For a doubly linked list, the only difference is going to be that green arrow. So we'll still be pointing this over, but we'll also need to point this arrow back. Then we'll have tail point to the new node like this, and that adds that into our doubly linked list.

We also have to code for when we have an empty linked list where we have head and tail point to the new node. So if you're going to code this, go ahead and pause it here. Otherwise I will get into the code. So we'll call our method append. We'll pass it a value. The return type is void because we don't need to return anything to be able to append an item to our linked list. So the first thing we'll do is create a node. We'll use the value that we pass to the append method.

And that creates our node. So our first situation that we'll write code for is when we have an empty linked list where we have head and tail point to this new node. So we have to test to make sure that the linked list is empty. So I'll say if length equals zero. Or you could say if head equals null. Then head equals new node like this. And also tail equals new node like this. So let's add this in with the rest of our code. This is for when we have a linked list with zero items in it.

So now let's write the code for. When we do have items in it, we'll say else and we'll build out this else statement. So the first thing we'll do is say tail dot next equals new node. That is tail dot next equals new node. Then we'll say new node dot previous equals tail. So that previous pointer on the new node we want to have it point to the same node that tail is pointing to. So that will look like this. And then we'll say tail equals new node, and that moves that over and adds that node into our list.

So now let's add this code and with the rest of our code like this. And now the only thing left to do is to increase the length by one. So we'll look at this code in a moment in IntelliJ. And when we do we're going to create a linked list with one item in it with a value of one. And then we'll run the append method and add another node with the value of two. So now let's flip over to IntelliJ and take a look at this. So there is our append method.

There. So I'll come up to our main tab here. And this contains our main method. And with this line of code here we'll create a new doubly linked list. And it will have a node with a value of one. And then with this we will print out that linked list. So I'll run this. And you can see up here we have a linked list with one node in it with a value of one. And then I'll come up here. And this will append a node with the value of two. And then of course, we will run our print list method and take a look at the length list.

And now you can see that we have a linked list with the values of one and two. And that is our method for append.

----------------------------------------
