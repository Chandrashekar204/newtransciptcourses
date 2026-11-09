# 12.2 — HT: Collisions

> Section 12: Hash Tables

So now we're going to talk about a couple of ways that we can deal with collisions. So I'm going to bring up our address space here and put some key value pairs in here. One of the ways of dealing with collisions that we saw in the last video is that you just put the next key value pair at the same address, even if there's already one there. This method is called separate chaining. So now let's remove that key value pair we just added. And look at another way that we might do this.

Another common way of doing this is if there is an item already at the address where you want to put something, you just go to the next open spot and put it there. And then if you're going to add another item, you just keep going and looking for an open spot until you find one, and then you place it there. This is called linear probing. And this is one of the types of open addressing. So separate chaining and linear probing are the most common way of dealing with collisions.

The way we're going to deal with collisions in this course is going to be separate chaining. That's going to be where we have all of these at one address. And the way we're going to do that is by having a linked list at each one of these addresses. So a linked list is a common way of implementing separate chaining and putting multiple items at a particular address. And that is how we are going to deal with collisions.

----------------------------------------
