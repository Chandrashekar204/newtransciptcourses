# 10.4 — BST: Constructor

> Section 10: Trees

So now we're going to build our constructor for our binary search tree. So the first thing we need to build here is a node. So we'll use the same hash map analogy for a node that we've seen in linked lists and doubly linked lists. Except this one is going to have value left and right instead of value and next or value next and previous in the case of a doubly linked list. So those will be our class variables for our node class. And then the constructor itself for the node is going to be identical to what we've seen before to create a node.

So now we can start building out our binary search tree class. And the first thing that we need to look at, I'm going to bring up a node and I'm going to put this in a tree. Each node has to have a pointer pointing to it or it's going to get garbage collected. And every node here has something pointing to it except that top node. This is similar to what we saw with linked lists. We needed to have head point to the first node. If you don't have anything pointing to the first node, it will get garbage collected and then all of the other nodes will get garbage collected as well.

So we need to do something similar with a tree, but instead of calling it head, we call it root. So the first thing we need to do with our binary search tree class is create this variable root that can point at a node. So then we'll build out our constructor for the binary search tree. We'll pass this a value and let's just focus in on the constructor. And we'll create a node. And that creates one of these. Then we'll set root to be equal to the new node like this.

So with a linked list we also had length a way to keep track of how many nodes we had. We're not going to do that with a binary search tree. So this is the entire constructor. So now that we have this built out and this is a valid constructor, I'm going to go through and show how to do this constructor in a different way. So in the constructors that we've done so far with linked list, doubly linked lists, stacks, queues, we have created the first node at the time that we created a new instance of that data structure.

But we don't have to do it that way. We can just initialize a tree that doesn't have any nodes in it, and then we add the first node with the insert method. So what I'm going to do is bring back our code, and then we'll go through and change it to be a constructor that builds an empty tree at the time that we create a new tree. So let's bring the code back here and go through it line by line. So in that first line we pass this a value. The whole reason we pass this a value was to create the first node.

So we no longer need that. And then this line here this line creates a new node. If we're not going to create a new node we can remove that. And then we set root to be equal to new node. But now we're just going to set root to be equal to null. So this becomes the entire constructor. So let's bring back the rest of our code for our binary search tree class up here. When we created root we didn't set it to be equal to anything. So root is already equal to null.

So setting it equal to null down here is redundant. And since that's the only thing the constructor does, we don't need this constructor at all. We can completely remove it. So when you create a new instance of a binary search tree, the only thing that's going to have is this variable root and root will automatically be set equal to null. So now let's go take a look at this. And IntelliJ. So over here we have a new package binary search tree that is that file folder there.

That's all in lower case. And it contains our class binary search tree which is capitalized. And then we have our main class that contains our main method. So I'm going to close this sidebar here. So we just have the code. So here is our binary search tree class so far. And this is where we have that one class variable root. And this is where we have that inner class that creates nodes. So one of the things I'm going to do is I'm going to come up here and remove private from root.

Normally you want your class variables to be private, but I want to have access to this, so I have visibility to it. When we flip over to our main tab I'm going to come up here and click on this. So what we're going to do here is we're going to create a new binary search tree called my binary search tree. And then with this line here we're just going to print out root equals and then show what the root is equal to. So I'll run this. And you can see here that the root is equal to null.

So it looks like we have a working binary search tree constructor.

----------------------------------------
