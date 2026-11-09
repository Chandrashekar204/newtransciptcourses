# 4.1 — Linked List: Intro

> Section 4: Linked Lists

So now we're going to look at linked lists. This will be the first data structure we build in the course. And I'm going to start out explaining linked lists by comparing them. To an array list and talk about the differences between an array list and a linked list. And an array list is the data structure that linked lists are most commonly compared to. And the reason why linked lists are more commonly compared to an array list is because linked lists are dynamic in length, just like array lists, whereas arrays are fixed in length.

So the first difference between an array list and a linked list is we're not going to have these indexes where we can go directly to a particular item. So I'm going to remove those. Another difference is that with a linked list, instead of all of these being in a contiguous place in memory, they are going to be spread out. Now, one of the things that I like to do when we move to a new data structure is change how we represent it visually. We represented the array list and arrays as green squares.

In a linked list, I'm going to represent these as purple circles. And that helps us to visually separate the two data structures. Linked list is also going to have a variable called head that points to the first node, and one called tail that points to the last node. And if you'll recall from our pointer video, both of these variables are pointers that just point to nodes. And then each node is going to have a pointer that points to the next node and the next, and so on until we get to the end.

That last node has a pointer as well. It just points to null, which means it doesn't point to anything, but it does have a variable there for that pointer. So the length list, if you look at this in memory, is all over the place like this, with each one pointing to the next to the next. So if you compare this to an array list or an array, those data structures are going to be in a contiguous place in memory like this. And that's why with those data structures, we can have indexes.

Okay. And that is our quick overview of linked lists and how they compare to array list.

----------------------------------------
