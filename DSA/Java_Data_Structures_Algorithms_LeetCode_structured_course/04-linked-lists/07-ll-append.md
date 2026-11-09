# 4.7 — LL: Append

> Section 4: Linked Lists

So now we're going to create our append method. So append is going to look like this. We're going to need to create a node. The last item in the linked list will need to point to it. Tail will need to point to it, and that adds that into the linked list. That is if the linked list has items in it. If the linked list is empty and we just want to have head and tail point to the new node. So what I'm going to do throughout the course is I will try to show you the steps for a particular method.

And then if you want to try to code it, this is where you'll pause the video, go take a shot at coding it, and then come back and watch how we code this. So we'll begin our append method like this. We're going to pass it a value and we'll use that value to create a node. Like this. So the first situation will code for is when the linked list is empty, where we want to have head and tail point to the new node. In order to do this, we have to actually test to see if the linked list is empty.

So we'll say if length equals zero and to test if it's empty. You could also say if head is equal to null or tail is equal to null. But I'll use length equals zero. Then we'll say head equals new node like this. And then we'll say tail equals new node. And now head and tail are both pointing to the new node. So let's put this in with the rest of our code like this. And this is if we have an empty linked list. If we have items in the linked list we'll say else.

And let's build out the else statement. So we'll say tail dot next equals new node. That is tail dot next equals new node. Then we'll say tail equals new node. And that moves tail over like that and adds that into our list. So now let's put this in with the rest of our code. So far we have created a node and this is what we do. If we have an empty linked list, this is what we do. If we have items in the linked list, and the only thing left to do is to increase the length by one.

So we'll look at this code in a moment in IntelliJ. And when we do. We'll have a linked list with one item in it with a value of one, and then we'll run the append method. And add a node with the value of two. So now let's flip over and take a look at this in IntelliJ. So there is our append method there. And then I'll come up here to our main tab. And this line of code here is creating our new linked list with the node with the value of one. And then here I'm going to print this out.

And I'll run this. And you can see here we have a linked list with one node with a value of one. That I'm going to come over here and paste in a line of code. And this is going to append a node with a value of two. And then we're going to print this again. And now we should have a linked list with one and two. So I'll run this. And you can see here that our linked list now has one and two. So it looks like we have a working method for append.

----------------------------------------
