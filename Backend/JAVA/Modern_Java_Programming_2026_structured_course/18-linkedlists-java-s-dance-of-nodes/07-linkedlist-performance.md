# 18.7 — LinkedList performance

> Section 18: LinkedLists - Java's Dance of Nodes

[00:00] Let's try to understand about the performance of LinkedList objects.
[00:05] We need to understand under which scenarios
[00:07] LinkedList is going to work better and under which scenarios it is going to have some performance issues.
[00:14] We all know that arrays, they are going to store the objects or elements in an consecutive memory location.
[00:21] The same applies for the ArrayList as well.
[00:23] But coming to the LinkedList, we know that each object it is going to stored in a separate link or
[00:28] node.
[00:29] Inside this link or node, we are going to store a reference to the next link or the next node, and
[00:36] similarly to the previous node or the previous link as well, if it is not a first element.
[00:41] That's why, in other words, inside the Java programming language we can say all LinkedList are actually
[00:47] double linked.
[00:48] The reason why we call them as double linked is, each link or node
[00:52] it is going to point to the two other nodes.
[00:55] One is the next node and the other one is the previous node.
[00:58] One of the drawback of ArrayList or array is they are going to have lot of performance issues.
[01:05] If you try to do the random addition operation or remove operation, since they are going to store the
[01:11] elements in a contiguous memory location.
[01:13] If you try to remove the element from the middle of the ArrayList object in those scenarios, all the
[01:19] subsequent elements has to be shifted either to the left side or to the right side based upon whether
[01:25] you are trying to perform delete() operation or add() operation.
[01:28] But with the LinkedList we can overcome these
[01:31] drawback of ArrayList.
[01:33] Whenever we are using LinkedList, removing an element or adding an element from the middle of the linkededList
[01:39] or from any location, it is going to be an inexpensive operation.
[01:45] When I say inexpensive, it is going to be fast.
[01:48] Let's try to understand why it is going to be fast inside LinkedList.
[01:53] If you try to take an example like you can see here, think like I have four elements inside my LinkedList
[01:59] object.
[02:00] The very first element is India, followed by Canada, USA and Germany.
[02:05] So this is my link one or node one.
[02:08] Inside this we have the data India.
[02:10] Since this is the very first element inside my LinkedList, the previous node memory value, it is
[02:16] going to be null, whereas under the next it is going to store the memory location of the next link
[02:23] or the next node which is linked to. Coming to that link to ah, the second node inside the LinkedList.
[02:29] It is going to store the what is the data followed by under the next it is going to point to the memory
[02:35] location of the next link or the node under the previous
[02:39] you can see it is pointing to the memory location of the previous link at the previous node.
[02:43] So the same kind of logic applicable for the link three as well.
[02:47] Under the next it is pointing to the memory location of link four
[02:50] under the previous, it is pointing to the memory location of link two, and at last we have the last
[02:56] element with the name link four or the node four.
[02:59] Inside this under the data we have Germany, but under the next we are going to have null value because
[03:06] there is no next node or there is no next element.
[03:09] That's why always for the last node or for the last element, the next value is always going to be null.
[03:16] But under the previous it is going to point to the previous element which is link three.
[03:21] So this is how the link list is going to store the data.
[03:25] Now think like I want to remove a random element which is link three.
[03:30] If I try to remove the USA element from my LinkedList object, all this entire link 3 or
[03:37] node 3 is going to be removed. With that
[03:40] this is how it is going to look like.
[03:42] You can see only the surrounding links or nodes
[03:46] they are going to be affected.
[03:47] All the remaining nodes are not going to be affected.
[03:50] When I deleted these link 3 or node 3 and add the link to the next element address is going
[03:57] to be updated, which is link 4.
[03:59] Similarly, under the link 4 the previous information is going to be pointed to the memory address
[04:05] of link 2.
[04:06] So that's why I have link 2 instead of link 3.
[04:09] So this should give a confirmation to you that whenever we are trying to perform a random remove() operation,
[04:16] only the surrounding two nodes are its elements
[04:19] they are going to be affected remaining all the nodes or the elements
[04:23] they are not going to be affected.
[04:25] Think like you have 1000 elements or 1 million elements inside your LinkedList.
[04:29] If you try to randomly remove an element at a particular position, only the surrounding two elements
[04:35] are going to be affected.
[04:36] That's why whenever we are trying to use the LinkedList, the remove() operation is not going to be expensive.
[04:42] It is going to be super fast.
[04:44] The same kind of logic you can also consider for addition of an element randomly in the middle of the
[04:50] LinkedList.
[04:51] Whenever you are trying to add a element inside your LinkedList at a random location in that scenario
[04:57] also, it is going to be super fast because
[05:00] only the surrounding elements
[05:02] information has to be updated, whereas inside the ArrayList all the elements has to be moved to the
[05:08] right hand side by one index.
[05:11] So with this we are able to overcome the drawback of ArrayList using the LinkedList, but don't come
[05:17] into the conclusion that LinkedList is always better than ArrayList.
[05:21] LinkedList also has its drawbacks, so let's try to understand what is its drawbacks.
[05:26] If you try to consider the scenario of reading an element randomly from an LinkedList, it is going
[05:33] to be an expensive operation.
[05:35] It is going to have some performance issues compared to the ArrayList.
[05:39] So let's try to understand why LinkedList is going to suffer a lot whenever you are trying to read
[05:45] an element randomly.
[05:46] So if you try to see here I have four different elements which are stored under four different links
[05:52] or nodes.
[05:53] Think like I want to read the last element, which is Germany.
[05:58] In this kind of scenarios, my LinkedList does not have any clue where these Germany is stored inside
[06:05] the LinkedList, because we know inside LinkedList all the objects that are going to be stored at
[06:10] a random locations.
[06:11] My LinkedList object
[06:13] it is always going to have only the memory location of the very first node or very first link.
[06:19] So in order to read these link for first my link 1, it has to look for what is the memory location
[06:26] of link 2 by looking into this next data.
[06:29] Once it is able to access the link 2, then it is going to look what is present under the next.
[06:35] So from link 2 the navigation will go to link 3.
[06:38] So now my link 3 only knows that how to access that link 4 and its data.
[06:44] So from link 3 under the next it is going to read the memory location of the link 4.
[06:49] And it will go to this memory location and try to fetch the element from this data field.
[06:55] So anytime inside your LinkedList, if you want to access a random element, it always needs to start
[07:02] right from the first element inside your LinkedList.
[07:05] So it is going to keep on asking what is the memory location of the next link?
[07:10] So it is going to keep on asking the same question until it reaches to the target link or target node.
[07:16] Whereas with arrays, regardless of whatever index element that you are trying to access, it is always
[07:21] going to be super fast because inside ArrayList, all the elements are going to be stored in a contiguous
[07:27] memory locations.
[07:28] My ArrayList object
[07:29] it can directly jump from the first index to the target index by performing some addition.
[07:35] That's why inside ArrayList always reading a random element is fast compared to the LinkedList.
[07:42] I hope now you are clear about the LinkedList performance.
[07:45] As a next step, let's try to understand the differences between LinkedList and ArrayList in the next
[07:52] lecture.
[07:52] Thank you,
[07:53] bye.

----------------------------------------
