# 18.4 — Demo of LinkedList

> Section 18: LinkedLists - Java's Dance of Nodes

[00:00] Let's try to explore more details about the LinkedList.
[00:03] What I'm going to do is I'm going to first print out this LinkedList with the name countryNames,
[00:09] with the statement I'm trying to validate if my LinkedList is maintaining the order of insertion and
[00:15] duplicate values.
[00:16] So let me execute this program and you'll be able to see inside the console all the country names they
[00:22] are getting displayed in the same order that we have added.
[00:25] And this gives confirmation to us that the LinkedList also is going to maintain the order of insertion.
[00:31] On top of that, it is also displaying the India country name a couple of times, and this should give
[00:37] a confirmation to you that LinkedList also allows duplicate values.
[00:42] Off course, it has to follow all these specifications because it is trying to implement the List interface.
[00:49] As a next step, I'm going to show you the demo of setter method.
[00:53] So with the help of set() method we can replace an element at a particular index.
[00:58] So I'm going to mention the index as four.
[01:01] And at the four index I'm going to set the element Spain.
[01:05] After making these changes let me copy the System.out.println() statement towards the end of the program
[01:11] and run this program.
[01:13] And with that you can see the element present at the fourth index is replaced with the Spain, which
[01:19] is the new element that we are trying to add.
[01:22] Now I'm going to show you the demo of remove().
[01:25] To show you the demo of the remove(), I'm going to invoke the remove() method.
[01:29] And to this remove() method I'm going to pass the value which is India.
[01:33] So this is going to remove the first occurrence of the India element.
[01:37] So since inside my LinkedList as of now I have only a single occurrence.
[01:42] You can see it is going to remove that single occurrence.
[01:45] And my LinkedList.
[01:46] It is going to have the values like Canada, USA, Germany and Spain.
[01:50] I hope this makes sense.
[01:51] As a next step
[01:52] what I can do is I can try to show you the demo of the SequencedCollection methods, for example by
[01:59] using these LinkedList object, I can try to invoke the getFirst() method.
[02:04] Similarly, I can also invoke the getLast() method. On the left hand side
[02:09] I'll try to catch the elements with the name first element, followed by
[02:15] in the next line
[02:16] I'm going to mention the variable name as last element.
[02:20] So if I try to keep a breakpoint at the last line and execute this program, you'll be able to see under
[02:26] the first element we have Canada.
[02:28] And under the last element we have Spain.
[02:30] You can see first element is Canada and the last element is Spain.
[02:34] This way we can invoke all SequencedCollection related methods.
[02:38] If you try to open this get first, you can see the logic inside this method is overrided.
[02:44] Inside this LinkedList class with the logic specific to the LinkedList.
[02:48] The way we retrieve the first element is going to differ from data structure to data structure.
[02:53] Inside the ArrayList, the logic is just to invoke the get() method with the zero index, whereas inside
[02:59] the LinkedList the
[03:00] logic is different.
[03:01] So previously the developers, whenever they are trying to deal with the boundary elements, they have
[03:06] to handle all this complexity.
[03:07] But from Java 21, with the introduction of SequencedCollection, we are going to have consistent
[03:13] method names.
[03:14] As a developer, we can just invoke these methods regardless whether you are using ArrayList or LinkedList
[03:21] or any other List implementation.
[03:24] You as a Java developer, you don't have to worry about the logic to fetch the boundary elements, or
[03:29] to add the boundary elements, or the remove the boundary elements
[03:32] or to perform the reverse() operation, you can simply invoke the methods which are available as part
[03:38] of the SequencedCollection interface.
[03:40] I hope it makes sense to you.
[03:42] Now let me show you the demo of reversing. For the same,
[03:46] we just have to invoke same method name which we have invoked while we are testing ArrayList.
[03:51] The method name is reversed on the right hand side
[03:54] I can try to catch the reversed LinkedList object with the name reversedCountryNames.
[04:03] I'll try to print out the same unto the console, so that we can validate if the reverse operation is
[04:08] successful or not.
[04:09] So let me remove this breakpoint and execute this program.
[04:12] In a debug mode you can see all my country names
[04:16] they are reversed because I invoked the reversed() method.
[04:20] I hope this gives some confidence to you that as long as you learn about ArrayList, it is going to
[04:26] be very similar with the LinkedList as well.
[04:28] So from the developer perspective, there are no major differences, just that the way they stored the
[04:33] elements behind the scenes is going to vary.
[04:36] And with that, the performance also is going to vary for various scenarios.
[04:40] We are going to discuss about performance in the coming lectures.
[04:43] But before we try to do that, let's try to see the demo of iteration of LinkedList in the next lecture
[04:50] Thank you,
[04:50] bye.

----------------------------------------
