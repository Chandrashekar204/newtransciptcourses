# 21.3 — Demo of HashSet

> Section 21: Set, HashSet, TreeSet, LinkedHashSet

[00:00] Since we are into the new section, I have created a project with the name section_21.
[00:06] Inside the same
[00:07] I'm going to create all the Java classes related to our discussion around the Set and its implementation
[00:14] classes here.
[00:15] First, let me try to create the new package.
[00:18] The package name I'm going to mention as com.eazybytes.Set.
[00:23] Inside this package I'm going to create a Java class with the name HasSetDemo. Inside this class as
[00:31] usual
[00:31] first we need to create the main() method.
[00:33] Once the main() method is created, we can try to create the object of HashSet. For the same,
[00:39] first, on the left hand side, we need to mention Set followed by angle brackets.
[00:43] Inside this angle brackets, I'm going to mention the data type as String and the object variable name
[00:49] I'm going to mention as visitedCountries.
[00:52] Let's imagine I'm trying to maintain a Set with the country details that I have visited them. On the
[00:59] right hand side I'm going to mention new operator followed by HashSet, and at the end I'm going to
[01:04] mention semicolon.
[01:06] Before we try to add elements into this HashSet object, let me open the Set interface.
[01:11] This Set interface is available inside the java.util package and it is extending the collection interface.
[01:18] If you try to read the documentation of this Set interface, there are a lot of details available,
[01:23] but the most important information that we are interested is,
[01:28] this is a collection that contains no duplicate elements.
[01:32] This Set contains no pair of elements e1 and e2 such that e1.equals(e2), and at most one null
[01:41] element is accepted.
[01:43] The same Set interface is implemented by our HashSet class.
[01:48] So HashSet is a most commonly used implementation class of Set interface.
[01:54] Here, in order to open the source code of HashSet, we need to make sure we are selecting the all
[01:59] places in this drop down post that you should be able to see a class from the java.util package.
[02:05] Let me open the same here.
[02:06] You can see it is extending another class with the name AbstractSet and it is also implementing the
[02:12] interface like Set, Cloneable and Serializable.
[02:16] If you closely observe this HasSet
[02:18] it is not implementing the SequencedCollection related interface which is SequencedSet.
[02:25] The reason is very simple.
[02:26] SequencedCollections like SequencedSet can only be implemented by a class only if it supports
[02:34] order of insertion.
[02:35] Since HashSet is not going to maintain the order of insertion, then there is no meaning of implementing
[02:41] SequencedSet.
[02:42] That's why we are not seeing the sequence to set in the implements details.
[02:47] But there is another implementation of set which is going to maintain the order and implement the SequencedSet
[02:53] .
[02:53] We're going to discuss about the same in the coming lectures.
[02:56] For now, I'm assuming you are clear that Set is an interface and HasSet is one of the implementation
[03:01] of the Set.
[03:02] The main features of this HashSet implementation is it is going to make sure the elements that you
[03:07] store are unique and there are no duplicates allowed.
[03:10] And on top of that, it is not going to worry about the order of insertion.
[03:15] It is going to save the elements at a random places just like HashMap.
[03:19] Now let's try to add few elements into these visitedCountries
[03:23] object.
[03:24] First, I'll try to mention the very first country I have visited.
[03:28] By using the add() method to this add() method, I need to pass a String object.
[03:33] I'm mentioning the India.
[03:35] Off course it is obvious.
[03:37] Since I'm staying in India, I need to mention India as a very first visited country.
[03:42] Now I'm going to mention other random country names under these visitedCountries
[03:47] object. The second country name I'll just mention as USA, followed by Dubai, followed by Singapore,
[03:56] followed by France.
[03:58] And at last I'm going to mention India one more time.
[04:01] So these are the country names that I have populated inside the visitedCountries object.
[04:06] But in reality I have not visited any of these countries.
[04:10] I'm just trying to provide some random country names here.
[04:13] If you are fortunate enough to visit multiple countries, feel free to mention all those countries inside
[04:19] your example.
[04:20] If you see the beauty of collections, regardless whether you are trying to use List or Set, you can
[04:27] use the same method which is add() to add the elements.
[04:30] Similarly, we also have size() method, which you can use for all the data types which are implementing
[04:37] the Collection interface.
[04:38] So with the help of these size() method, I will be able to identify how many number of elements stored
[04:45] inside my HashSet object.
[04:47] And at last let me try to print out the visitedCountries objects as well.
[04:52] So if I try to execute this program, you can expect the size as five.
[04:56] So we are trying to store six different country names.
[05:00] Because there is a duplicate country which is going to be ignored by my HashSet.
[05:04] So let me execute this program.
[05:06] You can see here the size is five like we expect.
[05:09] And the country details are stored at a random locations.
[05:14] That's why when we are trying to display the HashSet object we are seeing the elements at random locations.
[05:21] The order of insertion is not being maintained by the HashSet.
[05:26] I hope you are clear about the demo around the HashSet object.
[05:29] I'm assuming you are clear on how to add the elements similarly if needed.
[05:33] If you want to remove an element, you can invoke the remove() method in the next lecture,
[05:39] let's try to understand how these HashSet is going to work internally.
[05:44] We discussed in the previous lecture.
[05:46] HashSet internally leverages hashing mechanism and HashMap.
[05:50] So let's try to understand about all those in the next lecture.
[05:54] Thank you,
[05:55] bye.

----------------------------------------
