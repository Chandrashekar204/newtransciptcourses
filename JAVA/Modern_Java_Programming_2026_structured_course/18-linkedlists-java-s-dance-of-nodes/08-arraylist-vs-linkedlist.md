# 18.8 — ArrayList vs LinkedList

> Section 18: LinkedLists - Java's Dance of Nodes

[00:00] Let's try to discuss about the differences between ArrayList and LinkedList.
[00:05] With this discussion, you should get a clarity under which scenarios you should use
[00:09] ArrayList and LinkedList.
[00:11] The very first difference is we know ArrayList is an implementation of List interface, and it is going
[00:17] to store the elements in an contiguous block of memory or contiguous memory locations.
[00:24] Since the elements are going to be stored in a contiguous memory location, accessing an element or
[00:30] reading an element is faster compared to the LinkedList.
[00:34] Coming to the story of the LinkedList, LinkedList is also an implementation class of List interface,
[00:41] but it is going to store all the elements as nodes with a reference to the next node and the previous
[00:47] node.
[00:48] Since LinkedList is going to store the elements with the help of nodes, it is going to allow faster
[00:54] insertion and deletion of elements from the middle of the LinkedList or from any index inside the LinkedList
[01:01] .
[01:01] Do you know the reason why?
[01:02] The reason is very simple.
[01:04] The LinkedList has to update only the references of the affected nodes, whereas with the ArrayList
[01:10] all the subsequent elements, they are going to be affected and there needs to be moved either to the
[01:16] right hand side or to the left hand side to maintain that continuous memory location.
[01:21] The next difference is around the performance time whenever you are using the ArrayList, regardless
[01:26] of which index element you are trying to access, it can be 10,000 index elements or 1 million index
[01:33] element.
[01:34] You're always going to have a constant time off performance.
[01:37] For example, if the time taken by the ArrayList to read the very first index element is one millisecond,
[01:43] then the same one millisecond time is also required to read any element.
[01:49] It can be 10,000 element or 1 million element.
[01:52] But coming to the LinkedList, whenever you are trying to perform the read operation, it is going
[01:57] to take the linear time, which is O(n), which means if the LinkedList is going to take one millisecond
[02:05] to read the very first element, and if you are trying to read the 10th index element, then your LinkedList
[02:10] is going to take one into ten milliseconds, which is ten milliseconds.
[02:15] So based upon the index element that you are trying to access inside your LinkedList, the performance
[02:21] also is going to increase.
[02:22] ArrayList
[02:23] they are going to be slower than LinkedList only in the scenarios of adding or removing elements,
[02:29] especially from the middle of the List.
[02:31] That's why LinkedList is going to be a good choice whenever you need to frequently add or remove elements
[02:37] from the middle of the List, or from any location inside your List object.
[02:42] Overall, if you ask me what is the summary from this lecture, I would request you to remember one
[02:47] important point, which is always use ArrayList.
[02:51] If your code is going to do a lot of reading operation, whereas if your code is trying to perform lot
[02:57] of writing and deleting operations, please always use the LinkedList.
[03:02] If you are just dealing with the 100 elements or 1000 elements, you don't have to worry about ArrayList
[03:07] or LinkedList.
[03:08] You can use any of them.
[03:09] The performance issues only come into picture if you try to store thousands and millions of elements.
[03:15] I also mentioned few pictures here.
[03:17] You can see on the left hand side a person is trying to read the book.
[03:21] So please always remember this picture whenever you are trying to refer to the ArrayList.
[03:26] So that's why I have put this reading person on the left hand side where we are talking about
[03:32] ArrayList.
[03:32] But on the right hand side you can see a child is trying to write some sentences and he's trying to
[03:38] erase them if there is any mistake.
[03:40] So remember this picture whenever you are trying to recall about LinkedList.
[03:43] So for writing and removing scenarios, always LinkedList is the best option.
[03:48] With this, I am assuming you are clear about the differences between ArrayList and LinkedList.
[03:54] These are the very important concepts around collections.
[03:57] You may face many questions around them.
[03:58] Most of the students they don't know under which scenarios they should use the ArrayList and LinkedList
[04:04] .
[04:04] But with the discussions that we have done throughout this section, I'm assuming your super clear.
[04:09] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
