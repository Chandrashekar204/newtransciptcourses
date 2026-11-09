# 6.1 — DLL: Constructor

> Section 6: Doubly Linked Lists

So now we're going to create doubly linked lists. And we'll start out by creating our constructor. So for the most part, a doubly linked list is very similar to a singly linked list. The only difference being that we have arrows that go the other way. So for now, I'm going to convert this back to a singly linked list. And we'll talk about the difference between a singly linked list and a doubly linked list. So we said that a singly linked list node was similar to a HashMap that looked like this.

So when we built our class for the node it had two class variables which were value and next. The only difference that we're going to have here is we're also going to have another pointer that points to the previous node. The node constructor is going to be identical. And I think it's worth walking through this part again where we pass the node of value, which is this value here. And then we're setting this dot value to be equal to the value that we've passed this and this dot value.

Is this value up here? So now let's start building our doubly linked list class. We're going to have the same class variables that we had with a singly linked list which are head and tail. And then we keep track of the length. So once we have these we'll build the constructor and lists focus in just on this part. Now. In the constructor, the first thing we'll do is create a node with this line of code, and we'll pass this line, this value. But instead of creating a node that looks like this, we're creating one that looks like this.

Then we'll say head equals new node. Like this. And tail equals new node like that. And we'll say the length is equal to one. So let's bring back the rest of our code for our doubly linked list. So far we have three class variables and a constructor. So focusing back in on the constructor, when we create a new doubly linked list, we'll do it like this. So I'll call this my doubly linked list. And when we run this line of code, we will get all of this.

We'll get a new node for our linked list. Head and tail will point to that node and the length will be set equal to one. So now let's go over and look at this code in IntelliJ. So there is all of the code there that we just created. And then our node class is going to be an inner class inside of our doubly linked list class. And just like I did for linked lists I created these four methods here print list, get head, get tail and get length. Now I'm going to click on this main tab up here.

And this is the line of code where we'll create our new linked list with a node with the value of seven. And then down here we'll run our four methods where we can take a look at what's going on with our linked list. And I'll run this. So you can see here that head and tail point to a node with the value of seven. And we have a length of one. And then when we print out our linked list, it just has that one node with a value of seven. So it looks like we have a working doubly linked list constructor.

----------------------------------------
