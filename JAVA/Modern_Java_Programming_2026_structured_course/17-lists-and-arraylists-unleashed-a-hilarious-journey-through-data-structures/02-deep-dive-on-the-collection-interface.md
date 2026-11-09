# 17.2 — Deep dive on the Collection Interface

> Section 17: Lists and ArrayLists Unleashed – A Hilarious Journey through Data Structures

[00:00] Welcome to the new section.
[00:02] Inside this section we are going to talk in detail about one of the collection data structure which
[00:08] is List.
[00:09] So List is an concept inside Java collection framework.
[00:13] So we can treat this List as an interface.
[00:15] Under this interface we have many implementations like array List, LinkedList, Vector, Stack.
[00:23] So throughout this section we are going to talk in detail about how List is going to work.
[00:27] And we'll also take couple of implementation of List like ArrayList and LinkedList.
[00:33] And we'll try to see few demos around them and try to understand how to store objects using them and
[00:39] how to read them, how to process them.
[00:41] So this section, it is going to be super interesting and challenging.
[00:45] But before we try to explore about List and its implementation classes, first I want to spend few minutes
[00:52] making you understanding about the mother of all collections, which is collection interface.
[00:58] So let's try to understand what is this Collection interface?
[01:02] Why majority of the data structures inside Java?
[01:05] They are extending these Collection interface.
[01:07] You can see the same Collection interface is being implemented or extended by majority of the data structure
[01:14] supported by Java collection framework like List, Queue, Deque.
[01:19] So all of them they are extending or implementing the collection except the Map.
[01:24] The reason why Map is developed separately inside Java collection framework is it is going to store
[01:30] data in a different style compared to all these data structures like List, Queue and Set.
[01:36] When we talk in detail about Map, you will come to know about the speciality of Map and how it is going
[01:42] to store the data.
[01:43] For now, let's try to focus on these interface which is collection, just like how we are living inside
[01:49] the Mother Earth planet.
[01:51] Very similarly, inside the Java collection framework, all the data structures except Map, they are
[01:58] going to live under the umbrella, which is Collection interface.
[02:02] We can call this collection interface as an root interface inside collection framework.
[02:08] In general, in Java, collection refers to a group of objects known as its elements.
[02:14] So using collections we can store any number of objects.
[02:19] Some collections they will allow duplicate elements while others do not.
[02:23] In the similar lines, some collections they maintain the order of elements, while the others they
[02:29] don't maintain the order.
[02:30] Collections
[02:31] objects which are going to maintain the order of elements are order of insertion.
[02:37] They are generally subtypes of other interface, which is sequence to collection interface.
[02:43] This sequence to collection interface is introduced in Java 21 version.
[02:48] It is introduced very recently in 2023.
[02:52] We are going to talk in detail about sequence to collection in the next lecture.
[02:56] For now, if you try to understand the purpose of this collection interface inside the Java collection
[03:01] framework, the purpose is very simple.
[03:03] Using these interface Java team, they are outlining the fundamental functionalities that are expected
[03:10] from any collection implementations except Maps.
[03:14] Inside these interface we have various abstract methods default methods which are majorly categorized
[03:20] into four categories.
[03:21] The very first set of methods.
[03:24] They are going to provide you a contract or a specification around how to add elements into a collection
[03:31] object.
[03:31] Very similarly, the second category of methods, they are going to provide guidance around how to remove
[03:37] elements from a Collection object.
[03:40] And the third category is around the how to query the contents of the Collection object.
[03:45] And at last, the final category is how to make your elements available for additional processing.
[03:52] These are all the important methods inside the Collection interface.
[03:56] So let's try to open the Collection interface inside Intel Edge and try to explore all these methods
[04:01] inside my IntelliJ I'm going to open the Collection interface.
[04:06] Please make sure you are opening the Collection, but not the collections. Collections, which is a plural
[04:12] form of Collection.
[04:13] It is a utility class which is built for the Java collection framework.
[04:18] But we are talking right now about the Collection interface.
[04:22] So let me open the same.
[04:23] This is present inside the java.util package.
[04:27] If you try to understand about this interface, you will be able to see that these interface is available
[04:34] right from first to version of Java.
[04:37] Using these interface only lot many other interfaces and classes, they are inheriting the properties
[04:44] either directly or indirectly.
[04:46] So all these classes and interfaces, they are inheriting the behavior or the specifications from these
[04:54] root interface inside the collection.
[04:56] So this interface it is extending another interface.
[04:59] Which is Iterable.
[05:01] Iterable is another interface inside collection framework, which is going to help us to iterate the
[05:06] elements inside the Collection object.
[05:09] We're going to talk about Iterable and how to iterate the elements in the coming lectures.
[05:14] For now, let's talk about Collection interface.
[05:17] So inside these Collection interface, if you try to look at the list of methods available, first we
[05:22] have add related method which will help you to add elements into an any Collection object.
[05:29] You can see these are abstract methods.
[05:31] That means anyone who want to build a collection data structure inside the Java programming language,
[05:38] they need to make sure they are adhering to the signature of these abstract methods.
[05:42] Similarly, clear is going to help you to clear the elements of your Collection object contains and
[05:47] containsAll()
[05:48] will help you to identify whether a given object is present inside a Collection object, and equals()
[05:54] is getting inherited from the object.
[05:56] Superclass after equals()
[05:58] we have other methods like forEach(), hashCode() which are inherited from other interfaces like Iterable
[06:04] and object isEmpty() is going to help you to identify whether a given collection is empty or not.
[06:11] iterator(), parallelStream().
[06:13] They are going to help you to iterate the elements of a collection object and process them.
[06:19] We also have remove related methods, which is going to help you to remove the elements inside an collection
[06:25] object after remove related methods, we have retainAll() method.
[06:30] Using these retainAll() method, we can retain only the elements that you are trying to pass as an input.
[06:37] All the remaining elements will be removed from your collection object.
[06:40] size() method is going to help you to identify what is a size of your collection.
[06:45] How many elements or objects you have stored inside your collection object.
[06:50] Split iterator stream
[06:51] they also help you to iterate the elements and process the elements.
[06:55] We are going to talk about them in the coming lectures,. And at last we have three toArray() overloaded
[07:01] methods, which is going to help you to convert your collection object into an array.
[07:07] Sometimes inside your programming language, you may have requirement to convert to a collection object
[07:13] into a normal array.
[07:15] So in all those kind of scenarios, we can use these toArray() overloaded methods available inside the
[07:22] Collection interface.
[07:23] The implementation logic for these methods is going to be provided by the actual collection data structures
[07:30] like List, Queue, Set.
[07:32] All these collection data structures, they are going to inherit the specifications or the guidelines
[07:38] from these root interface.
[07:39] By following these method signatures, they are all going to provide their own business logic.
[07:45] But from an external developer perspective, they'll have a consistency in terms of method names and
[07:51] in terms of how they accept the input and how they return the output.
[07:56] I hope you are clear about these methods.
[07:58] We discussed on a high level about the size() method.
[08:02] So size() method is an abstract method inside a collection interface.
[08:05] This method needs to be implemented in all the subsequent collection classes.
[08:11] So what do we get from this method?
[08:13] When we invoke this method, we should get the number of elements that we stored inside a collection.
[08:19] If your collection contains more than maximum value supported by the Integer, then it is going to always
[08:26] give the same maximum value.
[08:29] Whatever list of elements that you store beyond the maximum value of Integer, they are all going to
[08:34] be ignored.
[08:35] But we should be fine, because if you look at the max value of Integer using this we will be able to
[08:42] store 2 billion elements.
[08:44] Are 2 billion objects inside a collection.
[08:47] That should be more than enough for any project.
[08:50] That's why even Java team also they made their return type of this size() method as an int, but not the
[08:57] long because with int max value we should be fine to store up to 2 billion elements.
[09:03] And at last, like we discussed, we have three different overloaded methods of toArray() using which
[09:09] we can return an array containing the elements inside a collection.
[09:14] I hope you are clear about the root interface inside the collection framework, which is collection.
[09:19] In the next lecture, let's try to understand about the sequence to collection interface.
[09:24] This is very important and it is recently introduced as part of Java 21 version.
[09:30] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
