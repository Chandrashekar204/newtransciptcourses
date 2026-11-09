# 17.4 — Deep dive on the List Interface

> Section 17: Lists and ArrayLists Unleashed – A Hilarious Journey through Data Structures

[00:00] Finally, we are going to discuss about List, which is one of the data structure supported by the Java
[00:07] collection framework.
[00:08] Like I said before, every data structure inside Java collection framework, it has its own characteristics
[00:15] on how it is going to store the data.
[00:17] So based upon our business requirements, we need to choose one of the data structure supported by the
[00:23] Java collection framework.
[00:24] Now let's try to understand what is a List and how it is going to store the elements inside a collection
[00:31] object.
[00:32] If you ask me that definition of the List, I would say list is an ordered collection which maintains
[00:38] the order of insertion, and whenever we are storing multiple elements inside a list, we will be able
[00:45] to access them with the help of their index value.
[00:49] On top of maintaining order of insertion
[00:52] List also supports duplicate elements.
[00:55] So whenever you have a requirement to maintain the order of insertion and to allow the duplicate values
[01:01] inside your Collection object, then always list is the go to data structure for you.
[01:06] Here you may have a question, which is when we try to store multiple objects or elements inside a List,
[01:13] how my List will know whether two different elements are equal or not.
[01:19] Suppose think like you're trying to store 100 different Person objects or 100 different Employee objects.
[01:26] In this kind of scenarios, list is going to check the equals() method that you might have overrated inside
[01:33] your Person or Employee class.
[01:35] So based upon the equals() method, it is going to identify whether two objects are equal or not.
[01:42] Even if they are equal or duplicate List is still is going to store them inside the Collection object.
[01:48] Like you can see here
[01:49] the very first element are object that you are trying to store
[01:52] it is going to be stored at the index zero.
[01:55] Similarly, the element two it is going to store at the index one followed by element three, just like
[02:01] arrays, even in the collections
[02:03] also, the very first index it is going to start at the zero. List is an interface inside the Java collection
[02:10] framework.
[02:11] So we can say this list is a concept which has its own characteristics.
[02:16] So what are the two unique characteristics of List.
[02:19] It is going to maintain the order of insertion, and it is going to allow the duplicate element under
[02:25] this List interface we have good amount of methods, but if you try to understand what are the important
[02:31] methods, the very first method is add() method to which you can pass your element as an input.
[02:37] So whenever you are trying to invoke this add() method, it is going to save your object at the next available
[02:44] index.
[02:45] Whereas if you are looking to add your element at a specific index, then you can invoke the second
[02:52] add() method which is going to accept two input parameters.
[02:56] One is what is the index value followed by what is your element value?
[03:00] Just like add(), we also have remove() method.
[03:03] So remove() method
[03:04] it is also going to accept the index value based upon the value of index that you're trying to provide.
[03:10] The corresponding element inside the List is going to be removed. After remove()
[03:14] we also have get() method, to this get() method
[03:17] when we pass a index value, it is going to return the element which is stored at a particular index
[03:24] inside a List object.
[03:26] After get, we have set() method.
[03:28] So set() method is very similar to this second add() method.
[03:31] But in the case of add() we are trying to add a new element at a particular index.
[03:37] Whereas with the set() index we are trying to replace the existing element at the specified index with
[03:44] the given element.
[03:45] After set(), we have a size() method which is going to return the number of elements in the List, followed
[03:50] by clear() method, which is going to remove all the elements from the List.
[03:54] If you closely look all these methods, they are derived from the Collection super interface.
[04:01] We know list extends Collection interface.
[04:03] Since List is one of the data structure present inside the Java collection framework, it has to maintain
[04:08] the same method signatures that is provided by the collection interface.
[04:13] But on top of that, this List interface or its implementation classes, they are going to provide their
[04:18] own business logic on how they are going to store the data or how they process the data.
[04:24] So every data structure inside the collection framework will add its own flavor to these method implementations.
[04:30] I said List is an interface, and with that you may have a question.
[04:34] Since List is an interface, we can't create the object of an interface, and without the object of
[04:39] this List we can't store the elements.
[04:42] Then what are the implementation classes of this List interface available inside the Java collection
[04:47] framework?
[04:48] This might be your question.
[04:49] The answer to this question is there are multiple implementation of list interface inside the Java collection
[04:56] framework, but there are two most commonly used
[04:59] implementations
[04:59] by the developers.
[05:01] The very first one is a ArrayList and the second one is,
[05:04] LinkedList.
[05:05] We are going to discuss in detail about this ArrayList and LinkedList in the coming lectures.
[05:10] For now, let's try to focus on this List
[05:13] interface.
[05:13] In the previous lecture we also discussed about SequencedCollection.
[05:17] So if you try to look at these SequencedCollection methods that are available on the left hand side
[05:22] of the table, all these methods, they are overrided inside the List interface with its own flavor
[05:28] of logic.
[05:29] For example, under the addFirst() method, the logic provided by the List interface is to add the given
[05:36] element at the very first index, whereas when someone invoke addLast() the equivalent method or the
[05:42] logic which is written inside the List interface is simply invoke the add with the element as an input.
[05:49] Similarly, for getFirst() they're going to invoke the get off first index, and for the getLast(),
[05:55] the logic is get size minus one.
[05:58] So what is the total size of the collection
[06:00] minus one will give you the last element inside your List object. For removeFirst()
[06:06] they're going to invoke the remove() method by using the zero as an index value.
[06:12] And for removeLast() they're going to invoke the remove() method using the size - 1 as an index value.
[06:19] The advantage that we are getting with the SequencedCollection method is regardless, you're trying
[06:24] to create a List object, or a Set object or a Map object, you're always going to get a consistency
[06:31] behavior in terms of methods that you need to invoke.
[06:35] You don't have to remember all these equivalent logic that is specific to the List, Set or Map.
[06:41] You just have to invoke these methods like addFirst(), getFirst(), removeFirst().
[06:47] On top of these methods, List Interface also implemented the reversed() method, which is extended from
[06:54] the SequencedCollection interface.
[06:56] So let's try to validate all our discussion by looking into the List interface inside IntelliJ.
[07:01] Here I'm trying to open the List interface available inside the java.util package.
[07:07] Like you can see here.
[07:09] This interface is extending the SequencedCollection interface and SequencedCollection interface,
[07:15] in turn extending the collection interface, which is the root interface inside the collection framework.
[07:22] If you try to look at the List of methods available inside list interface, majority of the methods
[07:28] are extended or derived or inherited from the collection interface, or from the SequencedCollection
[07:34] interface.
[07:35] So there are good amount of methods which we are going to discuss and use in the coming lectures.
[07:40] For now, I just wanted to show you the SequencedCollection related methods that are overridden with
[07:46] the logic specific to the List interface.
[07:48] You can see addFirst()
[07:50] method has a logic to add the given element
[07:54] at the zero index.
[07:55] We know the very first index always is going to be zero.
[07:58] That's why they are trying to use this logic very similarly
[08:01] you will be able to see the logic inside the addLast(), getFirst(), getLast(), removeFirst(), removeLast(),
[08:08] and at last
[08:09] we also have a logic for reversed() method.
[08:11] So this is the power that we are getting from the SequencedCollection.
[08:15] We as a developers don't worry about how to reverse the elements or how to get a last element, first
[08:21] element.
[08:22] So whenever you are trying to deal with the boundary elements, you can happily use the methods that
[08:28] are supported by the SequencedCollection interface.
[08:31] Now let's try to understand what are the implementation classes for List interface.
[08:36] For the same, you can select these List interface name and right click
[08:40] and here under the go to menu you can select the implementations option.
[08:45] And with that it will show you all the List of classes are abstract classes which implemented the given
[08:53] interface which is List.
[08:55] You can see there are many, many classes.
[08:58] We don't have to discuss all of them.
[09:00] I'm going to discuss two important implementation classes.
[09:03] One is ArrayList followed by LinkedList which are present inside the same package.
[09:09] I hope you are clear about List and how it is going to store the data from the next lecture
[09:14] let's try to discuss about the ArrayList, which is one of the famous implementation of List interface.
[09:21] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
