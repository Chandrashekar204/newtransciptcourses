# 18.3 — How to create objects of LinkedList

> Section 18: LinkedLists - Java's Dance of Nodes

[00:00] Let's make our hands dirty by writing some code around the LinkedList.
[00:04] First, I'm going to show you what do we have inside the LinkedList class?
[00:09] You can see this class is present inside the package java.util. Like you can expect
[00:14] this class implements List interface.
[00:18] If you try to understand what is there present inside this LinkedList, you'll be able to see about
[00:23] a node.
[00:24] Let me click on this node and it is a inner class inside the same LinkedList.
[00:29] So what do we have inside this node?
[00:31] The Node class is capable of storing three different types of information.
[00:36] The very first one is what is the actual element.
[00:39] The next information is the memory location of the next node element, and the last information is the
[00:46] previous node memory location.
[00:49] So this conforms to our discussion that each LinkedList element represents a Node.
[00:54] And inside this Node, the LinkedList is going to store three different kinds of data.
[00:59] If you try to see the List of methods inside this LinkedList, majority of the methods may look familiar
[01:06] to you, like we have add related methods, which will help us to add the elements into the LinkedList.
[01:12] Similarly, we have addFirst(), addLast(), which are inherited from the SequencedCollection.
[01:18] We also have a clear() method contains() method get() method getFirst(),
[01:23] getLast() method.
[01:24] So there are good amount of methods we don't have to discuss about each one of them.
[01:29] Whenever you want to create the immutable List object, you can use these List.of() static method.
[01:36] Once the immutable List is created from these immutable List, if needed, you can also create an LinkedList
[01:42] object.
[01:43] Whatever we discussed inside the ArrayList around the immutable List.
[01:47] The same concept applicable for the LinkedList as well.
[01:51] After these methods we have methods related to peek().
[01:55] So peek() is a method which is inherited from the Deque interface.
[02:00] So what is the purpose of peek().
[02:02] So peek() is an operation inside the LinkedList which is going to retrieve the element.
[02:06] So if you try to look at the peekFirst() it is going to retrieve the first element inside the LinkedList
[02:13] .
[02:13] But it is not going to remove.
[02:14] So the purpose of peek() operation is always to fetch the element.
[02:18] Similar to the peek(), we also have poll() related method.
[02:21] Let's try to open the pollFirst() method documentation.
[02:25] You can see whenever we are using the poll related method it is going to retrieve the element.
[02:29] And at the same time it is also going to remove the element.
[02:33] So the main difference between peek() and poll() operation is peek() is only going to retrieve the element,
[02:39] whereas poll() is going to perform the retrieving and removing of the element.
[02:45] After the poll(), we also have pop() and push() method.
[02:48] pop() method is going to help you to pop an element.
[02:52] In other words, it is going to remove the first element.
[02:56] So this is similar to the removeFirst() method.
[02:58] Just like pop(), we also have push() method.
[03:01] The purpose of push() method is to push an element at the very first location.
[03:07] So this is equivalent to the addFirst() method.
[03:09] So this way there are many number of methods available inside the LinkedList.
[03:14] We are going to see that demo of the most important methods. For the same,
[03:18] let me try to create a new package inside the section.
[03:22] Since we are into the new section I have created this project.
[03:25] You can also find this project inside the GitHub repo.
[03:28] Inside this src folder.
[03:30] Let me create a package with the name com.eazybytes.List inside this package
[03:38] first let me create a class with the name LinkListDemo.
[03:43] As usual, inside this class we need to create the main() method post that
[03:47] first, I'm going to show you how to create the object of LinkedList.
[03:52] Anytime if you want to create an object of LinkedList, we can follow various approaches.
[03:56] The very first approach is on the both sides
[03:59] you can mention the LinkedList along with the type of data you are trying to store.
[04:04] So here if I want to store the integer elements, then I need to mention that data type as integer and
[04:09] the name I can give as nums.
[04:12] And on the right hand side
[04:14] like I said, we should invoke the constructor of the LinkedList on the right hand side
[04:18] we don't have to mention the integer one more time because it is going to be duplicate.
[04:23] We can use that diamond operator here by removing these integer information.
[04:28] So this is one style of creating an object of LinkedList.
[04:32] The next style is by using the List interface on the left hand side.
[04:37] So whenever you are trying to create the object ofLlinkedList, we can have the superclass reference
[04:42] on the left hand side.
[04:44] So since List is a superclass of LinkedList, there won't be any compilation error.
[04:48] Think like I'm trying to store the double data type element.
[04:52] That's why I need to mention double here, followed by I'll give the variable name as doubleNums and
[04:59] the right hand side
[05:00] I'm going to mention new LinkedList with the diamond operator.
[05:04] So these are second approach.
[05:06] The third approach is with the help of Var keyword.
[05:09] I can mention Var countryNames, and on the right hand side I need to mention new LinkedList.
[05:16] And inside the angle brackets I need to mention that data type which is String.
[05:20] Whenever you are using the var to create your LinkedList object, you need to make sure on the right
[05:26] hand side you are mentioning the data type of the element.
[05:30] We should not use that diamond operator whenever we are trying to use a var.
[05:34] So now I have various LinkedList object as a next step, let me show you how to add the elements inside
[05:41] these LinkedList object.
[05:42] It is going to be very similar to the ArrayList.
[05:45] Before I try to add the elements, maybe I can try to correct this variable name two countryNames.
[05:50] So using these countryNames variable, I can try to add various country details.
[05:55] Like I can try to first store India, followed by Canada.
[06:00] After the Canada I can mention USA and after the USA.
[06:07] I can mention Germany and after the Germany I can mention India again.
[06:13] So this way we can store any number of elements by using the add() method.
[06:18] With this, I'm assuming you got some clarity around the LinkedList.
[06:22] I know we are ready to discuss about more details around LinkedList, so let's try to explore all of
[06:26] them in the next lectures.
[06:28] Before I try to close this lecture, let me highlight you that inside this slide, I have mentioned
[06:33] all the important methods that we can use on top of a LinkedList object.
[06:38] By using all these methods, we can add the elements.
[06:41] We can fetch the elements, we can remove the elements.
[06:43] So we can perform various operations by invoking all these methods.
[06:47] I'm not saying we have only these methods inside the LinkedList.
[06:51] These are the most commonly used methods.
[06:53] You may find lot many other methods as well, but since it is not possible for me to mention all of
[06:58] them inside this slide, I'm just trying to highlight the very important methods.
[07:03] I hope it is clear,
[07:04] thank you and I'll catch you in the next lecture, bye.

----------------------------------------
