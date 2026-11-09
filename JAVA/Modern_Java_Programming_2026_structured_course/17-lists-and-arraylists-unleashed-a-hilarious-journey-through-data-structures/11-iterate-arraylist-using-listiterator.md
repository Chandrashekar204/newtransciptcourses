# 17.11 — Iterate ArrayList using listIterator()

> Section 17: Lists and ArrayLists Unleashed – A Hilarious Journey through Data Structures

[00:00] Let's explore the third approach that we have to iterate the elements of a List object. To show you the
[00:05] demo of the third approach, I'm going to copy the class of ArrayListIteratorExample inside the same
[00:11] package, and I will rename this class name to ArrayListListIteratorExample.
[00:17] Because the third approach that we are going to use is with the help of ListIterator.
[00:22] So what is a ListIterator?
[00:23] ListIterator is a sub interface of Iterator, just like how we are getting the object of Iterator
[00:31] by invoking this iterator() method.
[00:33] Very similarly, we can invoke the listIterator() method.
[00:36] When we try to invoke this listIterator() method, we can catch the output with the help of listIterator()
[00:44] on the left hand side, and we can have this variable name as listIterator.
[00:49] So just like iterator using listIterator, we can also check whether the next element is available
[00:56] with the help hasNext().
[00:57] And similarly we can use the next() method to read the next available element.
[01:02] First, let's try to run the program by using this ListIterator.
[01:06] First, let me remove these unnecessary if block post that
[01:09] I'll also remove these System.out.println() that we have outside the while loop.
[01:14] So if I try to execute this program, you can see I'm getting the output based upon the elements that
[01:19] we have inserted here.
[01:21] You may have a question which is, if we already have an iterator, why should we use this ListIterator
[01:27] approach?
[01:27] There are few differences, which makes the ListIterator as a best approach.
[01:31] Using iterator approach, we can only access the elements in a forward direction, whereas with the
[01:38] help of ListIterator, we can access the elements either in the forward direction or in the backward
[01:45] direction.
[01:45] On top of that, using the Iterator, we can only perform the reading operation and remove() operation,
[01:51] but ListIterator allows you to perform any kind of operation.
[01:56] You can update your elements, you can add new elements, you can remove the elements.
[02:00] It's up to you what you want to do with that.
[02:02] You might be thinking like to use always ListIterator.
[02:06] My recommendation is to use the ListIterator only when needed.
[02:11] If you really have a scenario to access your elements both in forward and backward direction, and to
[02:16] delete them or modify them at runtime, then you are good to go and use the ListIterator
[02:22] otherwise, don't try to use ListIterator unnecessarily because compared to Iterator and for each approaches,
[02:28] ListIterator approach is going to take more time.
[02:31] So you will see performance issues
[02:33] you have thousands and thousands of elements inside your Collection object.
[02:38] So as of now, we are trying to traverse the elements in a forward direction.
[02:42] Now let me show you how to traverse the elements in a reverse direction.
[02:46] To access the elements in the reverse direction, I can copy the same while statement, and instead
[02:51] of hasNext() I can invoke the hashPrevious(), and similarly here instead of next(), I can invoke the previous().
[02:58] So with this
[02:59] now first we are trying to traverse the elements in a forward direction.
[03:03] By the end of this while loop the cursor inside the ListIterator object, it is going to point to the
[03:08] last element.
[03:09] That's why by the time I'm trying to execute the hashPrevious(), it is going to start the journey in
[03:14] a reverse or in a backward direction.
[03:17] That's why if we try to execute this program, you will be able to see first the output which is displayed
[03:22] with the help of hasNext() and next() methods.
[03:24] Later on you can see the same elements are displayed in a reverse direction.
[03:29] But don't try to put these hasPrevious() as a very first loop, because if you try to put these
[03:35] hasPrevious() related while loop as a very first while loop, you're not going to get any output from these
[03:41] while loop, because when you try to run your program initially, the ListIterator is going to point
[03:46] to the very first element from the very first element.
[03:49] If you try to check, is there any previous element, you're always going to get the output as false.
[03:54] That's why this while loop is never going to be executed.
[03:57] I can also show you a demo.
[03:59] Let me keep a breakpoint here and execute this program in a debug mode.
[04:03] Now I'll try to click on this step over button.
[04:06] You can see the execution is not going to enter into my while loop.
[04:10] It is going to directly execute the second while condition.
[04:14] If I try to release this program inside the output, you'll be able to see only the output that is received
[04:21] from the second while loop.
[04:22] That's why please always make sure where your cursor is pointed inside your ListIterator whenever you
[04:29] want to use the hasPrevious() or previous() related methods apart from this forward and reverse direction
[04:36] advantage.
[04:37] Like I said, ListIterator also supports various methods.
[04:41] Like you can see, you can invoke the add() method.
[04:44] You can invoke the remove() method.
[04:46] You can invoke the set() method.
[04:48] So you can perform all kinds of modifications whenever you are using the ListIterator.
[04:53] I hope you are clear with the three approaches that we have discussed, everything that we discussed,
[04:58] including the examples
[04:59] I have mentioned inside these slides.
[05:01] So this is the slide related to the for each approach followed by iterator approach.
[05:06] And at last I also have ListIterator approach slide as well.
[05:10] You can also see I have a slide comparing Iterator and ListIterator.
[05:14] Please refer to these slides and example whenever you want to refresh your knowledge around the iterating
[05:19] of the list elements.
[05:21] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
