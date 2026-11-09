# 21.2 — Introduction to Set in Java

> Section 21: Set, HashSet, TreeSet, LinkedHashSet

[00:00] As of now, we learnt everything about the List and HashMap which are available inside the Java collection
[00:07] framework.
[00:07] We have a very good understanding on how to use these List and HashMap data structure.
[00:12] Inside this new section, let's try to learn about another data structure available inside the Java
[00:19] collection framework which is Set.
[00:21] Set is also another interface inside Java collection framework.
[00:25] There are many implementations of Set interface.
[00:28] Inside Java library, we are going to learn about the most commonly used implementation of set throughout
[00:35] this section.
[00:36] So what is a Set?
[00:38] In Java,
[00:38] a set is an interface that extends the collection interface
[00:42] coming to the scenarios when you have to use this Set or its implementation class is whenever you have
[00:48] a requirements to store unique elements inside a data structure.
[00:53] In all those scenarios, you can use Set and its implementation classes.
[00:57] The primary character of Set and its implementation classes is it is going to maintain the uniqueness
[01:04] of your elements, which means it is not going to allow any duplicate elements.
[01:09] And typically most of the set implementation classes, they are not going to maintain the order of insertion,
[01:16] but there are few implementation classes where they are going to maintain the order of insertion, which
[01:21] you are going to discuss in the coming lectures.
[01:22] But any day, if someone is using set or its implementation class, the primary motivation that they
[01:28] may have is they want to maintain the unique elements, and they are not going to care about the order
[01:35] of insertion.
[01:36] Let's try to see how to create an object of Set like you can see here
[01:41] on the left hand side, we need to mention the Set interface followed by inside the angle brackets.
[01:45] We need to mention what is the data type of element that you are going to store inside an Set object.
[01:52] On the right hand side, we need to use one of the implementation of Set.
[01:56] Inside this example, I'm trying to use hash set along with the diamond operator.
[02:01] HashSet is a most commonly used Set implementation on day to day basis inside real projects set also
[02:09] stores similar to List.
[02:11] It is only going to accept a element.
[02:13] It is not going to store like a key and value like HashMap, but you can either use List or Set whenever
[02:20] you are trying to store only the elements without any key.
[02:24] But you need to be clear about your requirements whenever you are trying to choose the List are Set
[02:30] to implement your logic inside your program.
[02:33] If your primary requirement is around the order of insertion, then you can always go with the List
[02:39] and its implementation class.
[02:40] Whereas if your primary requirement is to maintain the unique elements inside your collection object,
[02:47] in such scenarios, you need to go with the Set and its implementation classes.
[02:51] We can also create and Set object from an List object. Like you can see here
[02:56] first, we can create a List object post that we can add some elements inside the List, and eventually
[03:04] using this List we will be able to create the Set object like you can see here.
[03:09] On the right hand side to the constructor of HashSet
[03:11] I'm trying to send the object of List, which is my List,
[03:16] so inside this List, if there are duplicate elements, then all those duplicates elements will be deleted
[03:22] by the time the elements are stored inside this HashSet.
[03:26] Let me show you an example on how to create an HashSet object like you can see here.
[03:32] First, I'm trying to create the object of HashSet, and inside this I'm trying to store the country
[03:37] names.
[03:38] The very first country name is India, USA, UK, France and India.
[03:43] You see, I'm trying to store the same element two different times like India and India.
[03:49] But behind the scenes, even though I'm trying to feed these kind of data which has some duplicate elements,
[03:55] by the time these elements are getting stored inside an HashSet, all the duplicate elements that are
[04:00] going to be removed.
[04:02] So here you can see we have only four elements because one of the duplicate element around India is
[04:08] removed.
[04:08] I'll also show you a demo about this in the next lecture.
[04:12] This HasSet also is going to work based upon the hashing mechanism and the hash table mechanism that
[04:19] we discussed as part of HashMap.
[04:21] With that you may have a question which is here we are only providing a value.
[04:26] There are no key involved.
[04:27] Then how these kind of data is going to be stored
[04:30] with the help of hashing mechanism and the hash table, you may have this kind of question.
[04:34] Don't worry about that.
[04:35] I'm going to discuss about this in detail in the coming lectures.
[04:39] For now
[04:40] please note that has set also going to work with the principle of hashing mechanism.
[04:45] And the hash table, just like HashMap allows a single null key very similarly has.
[04:51] It also allows you storing only one null value HasSet class is non synchronized.
[04:57] You should not be using for multithreading environment.
[05:00] You can consider storing your elements inside a HashSet.
[05:03] If you are looking to build a business logic around the search operations.
[05:07] If your code is going to do a lot of search operations, then you can happily use the HashSet object and
[05:13] inside it you can store any number of elements.
[05:16] Now let's try to understand about one important question that you may have, which is how HashSet is
[05:22] going to maintain the uniqueness of the elements for the same.
[05:26] Like you can see here, the steps are very simple.
[05:28] Like I said before HasSet it is going to leverage the hashing mechanism and hash table to store the
[05:34] data.
[05:35] So during the same process, whenever we are trying to provide an element to the HashSet, first it
[05:41] is going to calculate the hash code of the element.
[05:44] If there is an element already with the same hash code inside the hash table, then it is going to leverage
[05:51] the equals() method to compare the new element with the existing one, which has the same hash code.
[05:58] If the equals() method returns true, then it means we are trying to add a duplicate element into the
[06:04] Set.
[06:05] In such scenarios, the HashSet is not going to add your new element, it is going to simply ignore
[06:11] the new element.
[06:12] Whereas in the scenarios where the equals() method returns false, in such scenarios, the new element
[06:19] is going to be added under the same bucket in an linked list format or in a tree mapper format, because
[06:26] there are multiple elements with the same hash code.
[06:29] So it is going to work very similar to HashMap.
[06:32] If you can recall our HashMap discussion, hash maps are always going to have a unique key.
[06:38] The same concept is exploited inside hash to maintain the unique elements.
[06:44] With that, you may have a burning question or $1 million question, which is HashMap stores data in
[06:50] the form of key and value.
[06:51] But here with the HashSet we are only providing a value.
[06:54] There is no key, we're only providing a single element.
[06:57] Then how it is going to be stored as a HashMap internally.
[07:00] I got your question, I got you.
[07:02] Don't worry.
[07:03] I'm going to discuss about this in the coming lectures.
[07:05] I hope you are clear about this quick introduction about the Set and the HashSet
[07:10] in the next lecture.
[07:11] Let's see the demo around the HashSet.
[07:13] Thank you,
[07:14] bye.

----------------------------------------
