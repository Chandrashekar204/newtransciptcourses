# 4.12 — LL: Get

> Section 4: Linked Lists

So now we're going to create our Get method. The best way to explain what we're going to do with this method is just to show you the first line of code and the method. So we're going to get a node at a particular index. So if you're going to code this, go ahead and pause the video here. Otherwise I will get into this. So I'm going to bring up a linked list here. And what's going to be different this time is I have included the indexes. So we can only get a node at the index of zero, one, 2 or 3.

We cannot get a node at the index of negative one. Or we could say less than zero. And we can't get a node at the index of four. Or we could say greater than or equal to the length. So we'll create this if statement that says if the index is less than zero or the index is greater than or equal to the length. We're just going to return null. So now let's bring our linked list back up here. And since we're returning a node which will be a pointer to a node, we need to create a variable that we can return.

At the end of this we'll call this temp and we'll set it equal to head. And we'll do that with this line of code. And we won't need head and tail for the rest of the video. So I'll go ahead and remove those. Now we just need to move temp to the index that we want to return. So we'll use a for loop for that. And then inside of the for loop we will move the temp variable forward by saying temp equals temp next. So if we were looking for the node at the index of two this for loop would run one two times and then we would return temp.

And that is the entire method for get. So this is all pretty straightforward. The one part that people tend to forget is this line here to make sure that the index is in range. So we'll take a look at this code in a moment in IntelliJ. And when we do, we'll create this linked list where all of the values are equal to the index. That makes things easy. And then we'll get the node at the index of two. And we will expect to have the one with the value of two returned.

So now let's flip over to IntelliJ. So there is our Get method here as part of our linked list class. And then I'll click on our main tab up here. And this is going to create our linked list with values zero through three. And we'll print the list out with this line of code here. And I'll run this. And you can see that we have a linked list with zero, one, two and three. So I'll come up here and I will add this line of code. So we're going to run my linked list dot get with a value of two.

And then I have a line break here. And then we'll print the list again and I'll run this. And there is the node that has been returned with the Get method. And I want to point out with the linked list here that the two is still in the list. So the git method is going to get the node, but it is not going to remove the node. We have a separate method that will create in a couple of videos called remove, that will remove and return a node at a particular index.

So I want to make sure that this is returning the correct node. So I'm going to come over here and put dot value. And then we'll run this again. And you can see here that this has returned the node with the value of two. And that is our method for get.

----------------------------------------
