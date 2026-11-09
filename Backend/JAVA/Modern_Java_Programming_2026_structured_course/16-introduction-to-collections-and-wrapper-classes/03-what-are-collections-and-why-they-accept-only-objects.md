# 16.3 — What are Collections & why they accept only objects

> Section 16: Introduction to Collections & Wrapper Classes

[00:00] What are collections in Java?
[00:02] You may have this question, so let's try to understand the same inside this lecture. From many years
[00:07] computer scientists
[00:08] they are trying to address the drawbacks of arrays with their research computer scientists
[00:14] they are not able to identify a single universal solution.
[00:17] Instead, they have identified various clever techniques that can be used or incorporated in any programming
[00:26] language to store multiple elements that can grow dynamically based upon the elements that we are trying
[00:32] to add and remove.
[00:34] The same clever techniques are incorporated inside Java collections as well.
[00:39] With the various names.
[00:40] Like you can see we have various data structure or data types under the name collections
[00:45] these are List, Stack,
[00:48] Map.
[00:48] Set, Queue.
[00:50] All these data structures, they have their own use cases, or they have their own style of storing
[00:55] the data.
[00:57] Based upon our own business requirements, we need to choose one of them.
[01:01] For now don't worry about which one to use and what are the scenarios that you need to consider for
[01:06] each data structure or each data type that we have under collections, we are going to discuss about
[01:11] them in detail in the coming lectures.
[01:14] So when we say Java collection, it is not a single interface or a single class.
[01:19] It is an concept or it is an ecosystem under which we have many classes and interfaces that implement
[01:29] all the collection data structures that you see on the left hand side.
[01:32] So what are collections?
[01:33] They are very similar to arrays which are capable of holding the any number of objects.
[01:40] But the only difference between collections and arrays is, collections
[01:44] they can dynamically increase or decrease their size based upon the objects that we are trying to store
[01:51] or remove.
[01:51] On top of that, Java collections
[01:54] they support various data structures for storing and accessing the elements inside a collection.
[02:00] These data structures are like List, Set, Map, Stack and Queue.
[02:05] All the classes and interfaces around the Java Collections framework
[02:09] they are grouped under the same package, which is java.util package.
[02:14] So based upon our business requirements, we need to choose one of the data structure like List or Set
[02:20] or Map or Stack or Queue.
[02:23] Once we discuss everything in detail about these data structures, then you will be in a position to
[02:28] choose one of them based upon your business requirements.
[02:31] For example, I'll try to leak some information around these data structures very quickly.
[02:36] Whenever you are looking to maintain that data inside a collection, ignoring the duplicates, then
[02:42] you can always go with the Set.
[02:44] Whereas if you want to maintain the order of insertion into your collection, in such scenarios, you
[02:50] are going to use the List.
[02:51] Similarly, if you want to store your data in a dictionary format like key and value, then in such
[02:58] scenarios you can use the Map data structure.
[03:01] And similarly, if you want to follow the principle which is LIFO last in first out, then in such scenarios
[03:08] you can go with the Stack data structure.
[03:10] Whereas if you want to follow the first in first out principle, which is in short form, we can call
[03:16] it as FIFO.
[03:17] In such scenarios, you can obviously go with the Queue data structure.
[03:21] So data structures itself is a very big concept.
[03:24] We're not going to talk everything about the data structures, but instead we are going to discuss most
[03:30] commonly used data structures and their classes and how to use them and how to store the data inside
[03:35] them.
[03:36] So all those important concepts around the Java collections we are going to discuss inside this course.
[03:41] But whenever we are trying to use the Java collections, there is an very, very important point that
[03:47] you need to be aware, which is Java collections
[03:49] they will only allow you to store the objects.
[03:52] You can't store the primitive data type values like I can't store a primitive data type value like int,
[03:59] double, float, boolean, char because they are not objects, they are simply primitive data types.
[04:06] But with that, don't feel sad that we can't store the numbers and characters and boolean values inside
[04:13] the collections.
[04:13] There is a workaround we're going to discuss in the coming lectures.
[04:16] For now, please note that collections
[04:18] they will only allow you to store the objects inside them.
[04:23] Now you may have a question, which is why collections,
[04:26] they accept only objects.
[04:28] Why they are not accepting primitive data types.
[04:32] The reason is very simple Java team
[04:34] when they are trying to build a collections library with the help of lot many interfaces and classes,
[04:40] they have a problem which is inside Java
[04:43] we know we can store the data in two forms.
[04:46] One is with the help of primitive data types like int, float, double, char, boolean, short, byte,
[04:53] long.
[04:54] So these are the primitive data types which we can use to store the data.
[04:58] And the other side we can also store data with
[05:00] the help of objects.
[05:01] For example, with the help of a String object, I can store alphanumeric data.
[05:06] Similarly, with the help of a Person object, I can store all the person related information.
[05:11] So since there are two different ways to store the data inside Java Java team, they have a problem,
[05:17] which is they need to develop the collections framework considering the primitive data types and the
[05:23] objects.
[05:24] Since it is not going to make sense to develop the same library for two different purposes.
[05:29] What they have done is, they came up with a thumb rule, which is whenever someone wants to use the collections,
[05:35] they need to make sure they have their data stored in the form of object.
[05:40] Especially this rule came into the picture by considering the primitive data types.
[05:45] Developers they are not allowed to store that data with the help of primitive data types.
[05:50] But there is a workaround, which I'm going to discuss in few seconds on high level
[05:54] the reason why collections accept only objects is to keep these collections library more flexible and
[06:01] generic.
[06:02] On top of that, using only objects allows collections to support polymorphism that can operate on different
[06:10] types of objects.
[06:11] When we start using the collections, we can write some generic code that can be worked for any kind
[06:17] of objects that you are going to pass as an input.
[06:20] So based upon the input that you are trying to feed to your program, the program is going to behave
[06:25] differently.
[06:26] So that's a concept of polymorphism which we discussed long back.
[06:30] We are going to see a more powerful polymorphism by following collections in the coming lectures.
[06:36] Overall, like I said, the decision to accept only objects in Java collections is it was a design choice
[06:42] made to increase the flexibility and generosity, enabling them to store and manipulate a wide variety
[06:50] of objects.
[06:51] But with this discussion, you may have $1 million question which is running behind the scenes, which
[06:56] is how to store the primitive data types data using collections.
[07:01] So whenever we want to store a primitive data type value, we need to wrap that primitive data type
[07:08] as an object.
[07:09] And similarly, whenever you want to retrieve data from the collections, you need to unwrap the value
[07:15] from the object that you stored previously.
[07:18] So this wrapping and unwrapping process we are going to do whenever we are trying to store the primitive
[07:24] data type values inside collections.
[07:26] But this may look very complex to you, but don't worry, there are good amount of wrapper classes inside
[07:32] Java library to make our life easy.
[07:34] So from the next lecture, let's try to understand how to wrap and unwrap the primitive data type values
[07:40] while we are trying to deal with the collections inside Java.
[07:44] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
