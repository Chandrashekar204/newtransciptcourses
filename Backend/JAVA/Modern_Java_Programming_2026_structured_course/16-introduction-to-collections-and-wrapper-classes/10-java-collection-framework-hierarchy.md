# 16.10 — Java Collection Framework Hierarchy

> Section 16: Introduction to Collections & Wrapper Classes

[00:00] Finally, we discussed everything around the wrapper classes, autoboxing and unboxing, which is a
[00:07] prerequisite concept for Java Collections framework.
[00:11] Now we can happily get started with the Java Collections Framework.
[00:15] From now onwards, I'm going to use the framework jargon most Oftenly.
[00:19] With that you may have a question which is what do we mean by framework?
[00:23] Anytime if you hear the jargon framework, it means it is an ecosystem of libraries or classes or interfaces,
[00:32] which is going to help you in solving a problem.
[00:35] What are we trying to solve with the help of Java Collections Framework?
[00:38] Under these collections framework, we are going to have list of interfaces and classes, which is going
[00:44] to help us in storing the multiple elements with a single data type
[00:49] on top of that, we can overcome that
[00:51] disadvantages of arrays
[00:53] with the help of Java collection framework.
[00:56] I hope you are clear.
[00:57] Now let me show you the Java collections Framework hierarchy.
[01:01] You can see these are the most important interfaces and classes that we have under the Java Collections
[01:07] Framework hierarchy.
[01:08] I'm not trying to show you each and every class and interface inside this framework because it is unnecessary.
[01:14] And these framework also have hundreds and hundreds of interfaces and classes.
[01:18] I'm just trying to show you the most commonly used or most important interfaces and classes inside this
[01:25] slide
[01:25] whatever you see inside the green color, they represent the interface.
[01:29] Whereas whatever you see in the form of light pink or light peach color, you can call them as Java
[01:36] classes.
[01:37] First, let's try to understand what is there on the right hand side.
[01:39] On the right hand side we have an interface at the top which is iterable.
[01:44] The same is going to be implemented by collection.
[01:46] The collection interface is again implemented by List, Queue and Set.
[01:51] So using this List, Queue and Set we will be able to store any amount of elements or objects.
[01:58] But each of these interfaces and their implementation classes, they provide certain characteristics
[02:04] which you need to consider whenever you are trying to decide one of their implementations.
[02:09] For example, if you are trying to use the class of ArrayList to store your objects or elements, then
[02:14] you need to convince yourself why you are trying to use this class, but not the Set or Queue or Stack.
[02:20] I'm going to explain you what are the special characteristics of all these data structures.
[02:25] So based upon these special characteristics, you should use them to solve your business problem.
[02:30] So each of these interfaces classes like List, Queue and Set, they have good amount of implementation
[02:35] classes.
[02:36] We don't have to remember all of them because we're not going to use all of them on day to day basis
[02:41] throughout this course.
[02:42] Whatever is super important and whatever developers they are going to use on day to day basis, those
[02:48] classes and interfaces, I'm going to discuss them in detail in the coming lectures.
[02:52] So on the right hand side we have these kind of interfaces.
[02:55] But on the left hand side you can see we have a Map interface.
[02:58] So Map interface also has its own implementation classes.
[03:02] You may have a question which is why Map is not included inside this family under collection and Iterable.
[03:09] The reason is very simple.
[03:10] Map follows a different structure to store the data Map, always follow with the help of key and value
[03:18] format.
[03:19] When we discuss about Map in detail, it is going to make more sense to you.
[03:23] Whereas whatever you see on the right hand side, they always follow the same format.
[03:29] But all these interfaces, they have their own unique characteristics or features, which we need to
[03:35] consider while we are trying to use one of their implementation classes.
[03:39] Inside the next slide, I have mentioned all the important points around the Java Collections Framework
[03:44] hierarchy.
[03:44] From this slide, I just wanted to reiterate a few important points.
[03:48] The very first one is Collection.
[03:50] The Collection is the root interface for all the collection classes.
[03:53] So these Collection interface, it is going to have some abstract methods supporting the basic operations,
[04:00] such as adding an element, removing an element, and checking for the presence of an element inside
[04:06] a Collection implementation.
[04:07] So any implementation class that is implementing Collection interface, they should provide implementation
[04:14] logic on how to add an element, on how to remove an element, and on how to check for the presence
[04:20] of an element inside a Collection object.
[04:23] After Collection we have List interface.
[04:25] You should use List and its implementation classes only if you have a requirement where you want to
[04:31] maintain the order of insertion of the elements inside your Collection object, and on top of that,
[04:37] if you want to maintain the duplicate elements inside your Collection object.
[04:41] In such scenarios, you should use the List and its implementation classes. Whereas coming to the Set
[04:47] it is going to behave completely opposite to List.
[04:50] Set is not going to maintain the order of insertion, which means all the elements will be inserted
[04:56] at random positions in an unordered
[04:59] manor. On top of that Set
[05:01] it does not allow duplicates.
[05:03] Whenever you have a requirement where you don't want to maintain the duplicate elements, then in such
[05:08] scenarios, you can happily use the Set and its implementation classes.
[05:13] Coming to the Queue
[05:15] you need to use these interface or its implementation classes whenever you want to follow the principle
[05:20] which is first in, first out.
[05:22] So inside these Fifo principle, all the elements which are added first, they are going to be processed
[05:28] first, whereas Stack it is going to follow the completely opposite principle of Fifo which is lafoe
[05:35] last in, first out.
[05:36] So whenever you have a requirement where you want to process the last element first, in such scenarios,
[05:42] you can go with the Stack and its implementation classes.
[05:46] And at last we have a Map interface.
[05:49] You should use a Map and its implementation classes whenever you want to store the data in the form
[05:55] of key and value pairs.
[05:57] For example, if you want to store the numbers of your friends, definitely you first need to have a
[06:02] key, which is what is your friend name followed by value, which is what is his number.
[06:07] In such scenarios, we should use the Map which will allow us to store in the format of key and value,
[06:14] all these interfaces and classes they are going to present inside the package
[06:19] java.util.
[06:20] Like I said before, there will be hundreds of classes and interfaces discussing about each and every
[06:26] interface and class require a separate dedicated course.
[06:30] That's why what I am going to do is to make our life easy.
[06:34] I'm going to discuss most of commonly used collections and the implementation classes throughout the
[06:40] course.
[06:40] With that, you will be in a very safe hands by the time you are done with this course.
[06:45] I hope you are super clear and super excited to start the journey of collections.
[06:50] I'm also super excited to teach you about these complex concepts.
[06:54] Without learning collections, you can't climb yourself as a Java developer.
[06:59] That's why my humble request is please practice as much problems as you can around the Java collections.
[07:05] Thank you and I'll catch you in the next lecture, bye.


########################################
