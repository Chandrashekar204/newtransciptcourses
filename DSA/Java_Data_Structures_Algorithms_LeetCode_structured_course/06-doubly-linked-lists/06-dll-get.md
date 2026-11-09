# 6.6 — DLL: Get

> Section 6: Doubly Linked Lists

So now let's write our Get method. So this is one of the methods where our code is very different in a doubly linked list versus a singly linked list. So remember in the Get method what we're doing is we are getting a node at a particular index. So I'm going to start out here by bringing up a singly linked list. So it doesn't matter if you have a singly linked list or a doubly linked list, you still can only get the indexes of zero, one, 2 or 3.

You can't get anything that is less than zero. And you can't get anything that's greater than or equal to the length. So this is going to be the same with a singly or a doubly linked list. And in this situation we return null. So let's bring our singly linked list back up here. So if you'll recall we had our temp variable point to the head. We created that like this. Temp equals head. And we'll do the same thing with a doubly linked list. So I'm going to remove head and tail here.

So then we used this for loop. We can use this same for loop and a doubly linked list. Then we move temp forward by saying temp equals temp. Next. And if we were getting the item at the index of two, we would just move this forward like this and then return temp. So let's put this in with the rest of our code like this. So this method, this is exactly how it was written for a singly linked list as it is written here, will work for a doubly linked list.

But with a doubly linked list. We can add some code to this to make this all more efficient. To show you what I mean. Let's bring back our linked list here and turn it into a doubly linked list. If we were going to get the item at the index of one, what is the most efficient way to get to this node? Well, we'd start at the head and then we'd move through the list like this until we got to this node, and then we could return the pointer to this node.

But what if we wanted to get to this node? Now, starting at the head is not the most efficient way to get to this node, since this node is closer to the end than it is the beginning, it's going to be more efficient to start at the tail and go the other way. So let's bring this code back and we'll start modifying it to take advantage of this efficiency and a doubly linked list. So this for loop that moves us forward through the linked list. We only want to run this if the node that we're looking for is in the first half of the linked list.

So we'll wrap this with an if statement like this. If the index is less than the length divided by two, only then will we run this for loop. Otherwise we'll say else. And what we have to start out with here is setting temp equal to tail. So let me show you here in the diagram temp to begin with is set equal to head. Since this is what we're going to use to iterate through the doubly linked list. If we're going to go backwards, we have to move it to here and then move it to the left.

So now that that's here, we can create our for loop to go the other way. Now before temp was at the index of zero. And that's where we started our for loop. Now temp is at the index of three. So our for loop is going to say I equals the length minus one. The length is four. So the index where we need to start is three. That's length minus one. And then with each iteration of the for loop we will decrement I. And then inside of the for loop we'll say temp.

Temp dot previous. And that will move temp to the left. So if we were looking for the index of two we would then return temp. So let's look at this with the rest of our code. And that is our new and improved Get method. So we'll look at this code in a moment in IntelliJ. And when we do, we'll create this doubly linked list. And we'll get the node at the index of one which will also have a value of one. And we'll get the node at the index of two which has a value of two.

So let's flip over to IntelliJ and take a look at this. So there is our Get method there. Then I'll come up to this tab to look at our main class that contains our main method. And this creates our doubly linked list with values zero through three. And then with this line here we'll print that out and I'll run this. And you can see here that our doubly linked list contains values zero through three. So now I will come over here. And I will add these two lines of code.

And we're going to get the node at the index of one and the node at the index of two. And you can see here I added the dot value. So it'll just print out the value of each of these nodes. And then I also added a line break here because I'm going to leave the print list in here. And now I will run this. And you can see that we've returned the nodes with the values one and two. And then our print list here is still showing that we have zero through three.

So I wanted to run the print list here to emphasize that when we run the get method, we're not removing the nodes from the doubly linked list. And that is our method for get.

----------------------------------------
