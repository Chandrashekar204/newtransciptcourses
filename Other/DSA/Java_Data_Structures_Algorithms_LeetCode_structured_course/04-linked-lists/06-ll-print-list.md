# 4.6 — LL: Print List

> Section 4: Linked Lists

So I've created a method called Print List. And I'm just going to walk through what I did with this. It's pretty simple, but it makes it where you can print out your linked list and see what's going on with it. So it's going to look like this. I'm going to call it print list. We're going to have a variable called temp that is set equal to head. So our linked list is going to look like this. Then we're just going to have a while loop. And this while loop is going to print out temp dot value.

So in this case it's going to print out the number 11. And then this line here temp. Temp dot next will cause temp to just start moving across the linked list. When you get to the point where temp is null, it'll break us out of this while loop and then we'll be done. So pretty simple. So here's our code. And let's go look at this in IntelliJ. So there is our linked list class I'm going to scroll up. And you can see that print list is just a method that is inside of that class.

So I'm also going to add three more simple methods here. I'm going to come up here I'm going to paste these in and I'll scroll this up a little bit. So in addition to our print list I have added get head get tail get length. And this just prints out the value of the head node, the tail node and then gives you the length. So in the case of get length for example, I could return an integer that is the length. But generally when you return the length, the whole reason you're doing it is to print that out.

So I just go ahead and format this here. So it will print this out where it says length colon with a space. And it's all formatted nicely. So I'm going to come up here to our main tab. And I'll click on this. And this is where we created the new linked list with a node with the value of four. We've seen this in the last couple of videos. And then here we're going to run, get head, get tail, get length. And then we'll print out the entire linked list.

So I'll run this. And as we would expect, head is pointed to a node with a value of four, as is tail. The length is one, and because the linked list only has one item in it when we do our print list here. It only has that one item with the value of four. So I'll do something similar to this and all of the other data structures as well. It's important to have a way to be able to look at what you have as a way to help troubleshoot your code. All right.

So that is printlist.

----------------------------------------
