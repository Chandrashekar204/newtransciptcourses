# 6.8 — DLL: Insert

> Section 6: Doubly Linked Lists

So now let's create our insert method. And the best way to describe this method is to just bring this line up. Here we're going to insert a new node with a particular value at a particular index. And then we'll return a boolean. So I'll bring up our doubly linked list like this. And this will be the node that we're going to insert. So we've seen a few times now that we cannot insert an item that is out of range, or in this case less than zero on this end.

Or greater than the length on this end. So we'll create this if statement. If the index is less than zero or the index is greater than the length, we'll return false. Also, if we add the node to the end on this end, we've already created a method for this. So we'll say if the index is equal to zero, we'll run prepend and then return true. And then also if we're adding it to this end, we have a method for that. And we'll say if the index is equal to the length, we'll run the append method and then we'll return true.

So let's take a look at all three of these if statements for a moment. And now I'll bring back our doubly linked list. So now let's look at adding an item somewhere in the middle. In order to do this, we're going to need a couple of variables. I'm going to call these after. And before, so they'll be before and after where we insert this new node. So let's create these three items starting with the creation of this new node. Now let's create this before variable.

We'll say before equals get at index minus one. And we've seen before that we don't want to use the Get method to create the after variable. And the reason for that is the get method is O of n, and there's an O of one way of having after point to that node. We just set it equal to before next. So let's look at these in with the rest of our code like this. And now let's bring back our doubly linked list. So I'm going to stretch these apart like this.

And what we're going to need to do is write four lines of code that redirect these four arrows. Where they'll look like this. So let's put this back. So the first line we'll do here is we'll say new node dot previous equals before. So what we're doing here is taking the previous arrow on the new node and pointing it at the same node that before points to like this. Then we'll say new node dot next equals. After this is going to take the next pointer from the new node and point it at the same node that after is pointing to like this.

Then we'll say before dot next equals new node. That is before dot next equals new node. Then we'll say after previous equals new node that is after. Dot previous equals new node. And that adds that into our doubly linked list. Let's bring back those other two lines of code. These are the four lines of code that redirected these four arrows. So now let's look at this. And with the rest of our code like this. Now we just need to increase the length by one.

And because this method requires a boolean be returned, we will return true. We'll look at this code in a moment in IntelliJ. And when we do, we'll create a doubly linked list with the values of one and three. And then we'll insert a node with the value of two. And then it'll be one two, three. So now let's flip over to IntelliJ and take a look at this. So there is our insert method there as part of our doubly linked list class. And then I'll come up to this tab, which contains our main class that contains our main method.

And these two lines here create our linked list with values of one and three. And this line here will print that out and I will run this. And you can see that this has returned our linked list with values of one and three. So I'll come over here. And I'll paste in this line, which will insert at the index of one a node with a value of two. And then we'll print this again. And I'll run this. And you can see that our linked list now contains one, two, three.

And that is our method for insert.

----------------------------------------
