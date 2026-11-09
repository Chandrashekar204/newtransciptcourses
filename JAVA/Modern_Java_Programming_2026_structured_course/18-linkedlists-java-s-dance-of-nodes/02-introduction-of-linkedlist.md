# 18.2 — Introduction of LinkedList

> Section 18: LinkedLists - Java's Dance of Nodes

[00:00] Have you seen the movie frozen?
[00:02] I saw this movie with my daughter more than ten times, and my daughter might have saw this movie more
[00:07] than 100 times.
[00:08] Inside this movie, there are two sisters with the name Elsa and Anna.
[00:12] They are the daughters of the same parents.
[00:15] They both have their own strengths and weaknesses.
[00:18] The reason why I'm discussing about these sisters is in the previous section we discussed about ArrayList,
[00:23] and now inside this section we are going to talk about the sibling of ArrayList which is linkedList.
[00:29] They both have the same parent which is List, but the way they store the elements is very different.
[00:35] With that they have their own weakness and strengths.
[00:38] As of now we have a very good understanding about ArrayList, but in the next few lectures let's try
[00:44] to learn about LinkedList as well.
[00:46] Like I said before, Java LinkedList is also a data structure that represents a list of elements.
[00:54] Using these data structure
[00:55] also, we can store multiple elements or objects and these LinkedList also is capable of dynamically
[01:02] increasing or decreasing in size during runtime based upon the elements that we are trying to add or
[01:08] remove at runtime.
[01:09] So this LinkedList also present inside the same package like ArrayList.
[01:13] It is present inside the java.util package.
[01:16] Compared to the ArrayList.
[01:17] LinkedList is going to store the elements in a different manner.
[01:22] We saw inside the ArrayList
[01:23] all the elements that are going to be stored in an contiguous or contiguous memory locations,
[01:29] but LinkedList is going to follow a different approach, which we are going to discuss in few minutes.
[01:34] Before that, let me try to explain you about other important details around the LinkedList.
[01:39] So whenever you want to create an object of LinkedList, you can follow the same syntax that we have
[01:45] discussed.
[01:46] For ArrayList
[01:47] just in the place of ArrayList, you need to use the LinkedList class.
[01:51] So here you can see I'm trying to create a LinkedList object which is capable of storing the String
[01:57] objects or String elements.
[01:59] And I also use that diamond operator on the right hand side.
[02:02] Here you may have a question, which is why we have LinkedList inside Java when we are already able
[02:08] to store elements inside an ArrayList.
[02:10] It's a great question, I like that let's try to answer the same.
[02:13] When we store that data inside an ArrayList, we know either ArrayList or array.
[02:19] They are going to have a major drawback, which is whenever we are trying to perform the removing of
[02:25] an element from the middle of the ArrayList or array, it is going to be super expensive operation
[02:31] because all the array elements beyond the removed one must be moved to the left hand side by one index.
[02:38] The same applies if you try to add a new element at a random location inside an ArrayList.
[02:43] With these drawbacks, we can't use ArrayList.
[02:46] If our Java program is going to perform lot many deletions and insertions at runtime, we are going
[02:53] to overcome that challenge with the help of LinkedList.
[02:56] In the coming lectures, we are going to talk in detail about the LinkedList performance in the same
[03:01] lecture
[03:01] I'm going to share you all the details around the performance.
[03:04] Coming to the other important point, just like ArrayList, LinkedList also maintain insertion order
[03:10] and it also allows duplicate elements to store inside it.
[03:14] Just like ArrayList, LinkedList also does not allow you to store primitive data type values like
[03:20] int, float and char.
[03:22] Whenever we want to store some elements inside the LinkedList, it has to be a proper object.
[03:28] If you want to store primitive data type values, then definitely you need to convert them into the
[03:33] wrapper objects.
[03:34] Off course, we don't have to perform any boxing manually, but behind the scenes boxing is going to
[03:40] be done by the Java since it is going to be done automatically from developer perspective, we don't
[03:45] have to bother much about it, but whenever we are trying to declare the object of LinkedList, we
[03:51] just have to make sure we are mentioning the data type as a wrapper class, but not the primitive data
[03:56] type like you can see here at the end of the slide.
[03:59] First, I'm trying to create the LinkedList object by just mentioning the int, which is the primitive
[04:04] data type.
[04:05] With that, my compilation is going to fail.
[04:07] Instead of int, we should use its corresponding wrapper class, which is Integer.
[04:12] Most of the syntaxes that we are going to discuss around the LinkedList.
[04:15] You may feel very similar to the ArrayList, but there is no harm discussing one more time all those syntaxes.
[04:21] So that you can get used to these process of creating the Collection objects.
[04:25] So let's try to see more details around the LinkedList like you can see here
[04:30] these are the various approaches that we can follow to create the object of LinkedList.
[04:35] On the left hand side we can mention the List instead of LinkedList.
[04:39] That's perfectly fine because LinkedList implements List interface.
[04:44] If you want to use a Var and the left hand side, you are more than welcome to use it.
[04:49] But please make sure on the right hand side inside the angle brackets you are mentioning a proper element
[04:55] data type.
[04:56] Now let's try to understand how to add the elements
[05:00] into an LinkedList.
[05:01] In order to add the elements into the LinkedList, we are going to use the same add method like you
[05:07] can see here
[05:08] I'm trying to add various country names into the LinkedList by using the same add() method, but whenever
[05:13] we are trying to store the elements inside an LinkedList object, the way they store is going to be
[05:19] different compared to the ArrayList.
[05:20] So let's try to understand how the elements are going to be stored by looking at this visual explanation
[05:27] that I have inside this slide.
[05:28] Inside LinkedList, each element is going to be stored inside a node.
[05:33] So you can think this square box as a node.
[05:36] Inside this node there are three different kinds of information is going to be stored by the
[05:41] LinkkedList.
[05:41] The very first and the main value it is going to store is the actual element data that you are trying
[05:47] to store.
[05:48] So you can see here India, Canada, USA, Germany, India.
[05:52] The same values LinkedList.
[05:54] It is stored inside the node as a primary data.
[05:57] After this actual element value LinkedList to node, it also going to store the address location of
[06:04] the next element and the previous element, but the first element
[06:08] since there won't be any previous element, it is not going to store any previous element information.
[06:15] So whatever you see these 41, 92, 24, 9, 13 these are the random memory locations inside your heap memory.
[06:23] I just give some random numbers to these memory locations.
[06:26] With these it should be clear for you that LinkedList
[06:29] they are not going to store in an contiguous memory locations.
[06:33] They are going to be stored at a random locations inside your heap memory.
[06:38] So whenever these elements are getting stored at a random memory location, each node has to know about
[06:44] the memory locations of its next node and the previous node.
[06:48] For the first node, since there is no previous node, it is not storing any previous node information,
[06:54] but coming to the next node, you can see it stored the memory location of the next node, which is
[07:00] inside the node.
[07:01] Moving on to the next node here inside this node, since there is a previous element, it is trying
[07:07] to store the previous element memory location as well, like 41 coming to the next element memory location.
[07:13] It also stored the 24.
[07:15] This way all the nodes are elements inside a LinkedList except the boundary elements or boundary nodes.
[07:22] They are going to store three different kinds of information, like what is the actual element, what
[07:28] is the previous node memory location, and what is the next node memory location.
[07:33] But coming to the boundary nodes are elements.
[07:36] They're going to store only the next node if it is available, and the previous node if it is available.
[07:42] For example, for the first node, since there won't be any previous node, the previous node memory
[07:47] value, it is going to be null.
[07:49] Similarly for the last node, since there won't be any next node memory address, the next node memory
[07:55] address value is going to be stored as a null behind the scenes.
[07:58] So this is how LinkedList is going to store the elements inside Java.
[08:03] So there are few advantages and disadvantages
[08:06] with this approach we are going to talk in detail about the performance related advantages and disadvantages
[08:12] in the coming lectures.
[08:13] For now, please note that LinkedList
[08:15] they are not going to store their elements in contiguous memory locations.
[08:20] Instead, they are going to store at a random memory locations and each of the LinkedList element is
[08:26] going to be stored inside a LinkedList node, along with the element value.
[08:30] They are also going to store what is the next node memory address and what is the previous node memory
[08:37] address value.
[08:38] We as a Java developers, we don't have to deal with these complexity.
[08:42] A developer, he just have to invoke the add() method.
[08:45] And behind the scenes, all this complexity is going to be taken care by the JDK libraries.
[08:51] The first node that we have inside the LinkedList, we can also call it as head of the LinkedList
[08:57] and the last node
[08:58] we can also call it as tail of the LinkedList.
[09:00] The head node is the entry point into the LinkedList, whereas the tail node is the end of the LinkedList
[09:07] .
[09:07] Coming to the point, which is how to iterate the elements and how to sort the elements inside LinkedList
[09:13] .
[09:13] It's very easy.
[09:14] They are going to work in a very similar manner like ArrayList, so they are going to use the same iterator
[09:20] list iterator for each for looping.
[09:22] And we can also use the Comparable and Comparator related methods for sorting with this quick introduction.
[09:29] About LinkedList, I'm assuming you got some clarity about LinkedList from the next lecture.
[09:34] Let's try to practice few programs by trying to store elements with the help of LinkedList.
[09:39] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
