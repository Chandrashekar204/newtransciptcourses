# 17.3 — [JAVA 21] Deep dive on the Sequenced Collections

> Section 17: Lists and ArrayLists Unleashed – A Hilarious Journey through Data Structures

[00:00] Let's try to understand
[00:01] what do we have under the sequenced collections under the name sequenced Collections, there are three
[00:08] different interfaces are introduced.
[00:10] These three interfaces are SequencedCollection, SequencedSet, and SequencedMap.
[00:17] Before I try to explain about these three interfaces, first let me provide some clarity around why
[00:23] these three interfaces are introduced from Java 21, why they are not present before, and why the need
[00:30] came to introduce as part of Java 21.
[00:33] We know under collections there are many implementations and data structures.
[00:37] Few of them they maintain the order of insertion and few of them they don't maintain the order.
[00:43] For example, if you try to start inserting ten different elements, few data structures, they are
[00:49] going to retain the order in which you have inserted your ten elements. Whereas other set of data structures
[00:57] where they don't maintain the order they're going to have the elements at random locations in a jumbled
[01:03] manner, which means the order of insertion is not going to maintain.
[01:08] With this, it should be clear for you that the data structures are divided into two categories one
[01:13] category which maintains the order of insertion.
[01:16] The other category which does not maintain the order of insertion.
[01:19] Let's forget about the data structures which does not maintain the order of insertion, because the
[01:25] sequenced collections that we are going to talk, they're only applicable for all the data structures
[01:30] which maintain the order of insertion. For all the data structures or the collection objects which maintain
[01:36] the order of insertion.
[01:38] They don't have a common parent or a common interface, which can be used by the developers to write
[01:45] some generic code using the data structures that maintain the order of insertion.
[01:51] That's a very first drawback on why these sequence to collections are introduced.
[01:56] The second reason why these interfaces are introduced is, in all the data structures or the collection
[02:01] objects, where they maintain the order of insertion, there is no uniform or consistent way to fetch
[02:07] the first element or the last element, because the most common requirement for the developers on day
[02:14] to day basis is to deal with the first element or the last element.
[02:18] So in these kind of scenarios, to fetch the first element or last element, different data structures,
[02:24] they follow different business logic. Around this as well
[02:28] java team they want to provide a uniform approach.
[02:31] So this is the second reason why these SequencedCollections are introduced.
[02:36] The third reason is there is no uniform or a proper or a direct way of reversing the elements inside
[02:43] the Collection object, or inside a data structure where the order of insertion is maintained before
[02:49] SequenceCollections.
[02:50] If someone wants to reverse the elements inside a Collection object, they have to manually write some
[02:55] business logic, and this logic will different from the Set data structure and the Map data structure.
[03:01] That's why to overcome all these three drawbacks or three challenges, these sequence to collections
[03:07] are introduced from Java 21.
[03:09] So if you see under the Collection interface we have the first interface which is SequenceCollection.
[03:16] The same is extended again by one more interface which is SequencedSet.
[03:21] Whereas under the Map we have SequenceMap interface.
[03:25] Like we discussed, Map will follow its own style of storing the elements or objects.
[03:31] That's why Map alone has its own interface, which is SequenceMap.
[03:35] Coming to the SequenceCollection, you can see the SequenceCollection is directly being implemented
[03:40] or extended by List and Dqueue.
[03:43] Whereas coming to the Set data structure for this Set data structure, there is a separate interface
[03:49] has been introduced with the name SequenceSet.
[03:51] This SequenceSet, it is extending the properties from SequenceCollection itself.
[03:56] So let's try to understand these three interfaces.
[03:59] What do we have inside them?
[04:00] Post that it is going to make sense to you.
[04:02] Inside my IntelliJ, I'm going to open the very first interface which is SequenceCollection.
[04:08] You can see the SequenceCollection.
[04:11] It is extending Collection interface.
[04:14] And this interface is introduced as part of Java 21.
[04:18] So these are fresh and hottest feature that introduced in 2020 3rd September.
[04:24] You can read the documentation of these interface to understand the reason why this is introduced.
[04:29] We already discussed all of them just a couple of minutes back.
[04:33] If you try to see what is there present inside these SequenceCollection, it has so many methods.
[04:39] Let me try to uncheck these inherited members.
[04:42] And with that you will be able to see the abstract methods or default methods available inside these
[04:48] SequencedCollection interface.
[04:49] So if you see you have six different methods which will help you to deal with the first element and
[04:56] the last element of your collection data structure or
[04:59] Collection object.
[05:00] Whenever you want to add the a given element or a given object at a first position, you're going to
[05:07] invoke the add first.
[05:08] Very similarly, for last position, you're going to use the addLast().
[05:12] After the add related methods, we have get related methods, which will help us to retrieve the elements
[05:18] from an Collection object, which are located either at the first location or at the last location,
[05:24] and the similar lines.
[05:25] We also have remove related methods which is present at the first location and the last location.
[05:31] And at last we have a reversed method, which is going to help us to reverse the elements that we have
[05:37] inside a Collection object.
[05:39] Why these methods are introduced as part of SequencedCollection.
[05:42] The reason is very simple.
[05:44] Before SequencedCollection, there is no uniform approach or consistency approach either to reverse
[05:50] the element or to deal with the boundary elements.
[05:53] What are boundary elements?
[05:55] The first element and the last element.
[05:57] Those are called as boundary elements.
[05:59] If you closely look at these methods, only the reversed method is an abstract method, whereas remaining
[06:05] all the methods, they are default methods.
[06:08] So inside these default methods they are trying to throw an exception.
[06:12] The reason why they are trying to throw an exception is if some collection data structure or interface,
[06:18] if they are not overriding these methods, and if they're not providing their own logic, then anyone
[06:24] who is trying to invoke these addFirst() or any other methods available inside these interface, they're
[06:29] going to get a runtime exception which is unsupported operation exception.
[06:33] That means the data structure or the Collection object that you are trying to use.
[06:38] It does not overrided
[06:39] these default methods.
[06:41] That's why you are going to get a UnsupportedOperationException.
[06:44] But don't worry Java team, they take care of overriding these default methods in all the applicable
[06:51] collection data structures or collection classes.
[06:55] I hope you are clear.
[06:56] Now let's go to the SequencedSet this time
[06:59] so I'm going to open the SequenceSet like you can see here this interface.
[07:03] It is extending the functionality from the SequencedCollection and the Set interface.
[07:08] Let's try to see what is present inside this SequencedSet
[07:11] To set inside these SequencedSet, you can see we only have a reversed() method which is overriding
[07:18] the signature received from the SequencedCollection.
[07:21] Of course, the SequencedSet it is also going to inherit all the methods present inside the SequenceCollection
[07:28] like addFirst() all those methods it will obviously inherit, but it is trying to override
[07:34] the method related to the reversed().
[07:37] The reason it is trying to override the reversed related method is if you closely look at the reversed()
[07:44] method available inside the SequencedCollection, the return type of this method is SequencedCollection
[07:49] of data type E, the E that you see inside the angle brackets
[07:54] it indicates the data type of your objects, whether you are trying to store the Person objects or String
[08:01] objects, you need to convey that to the collection framework while you are trying to create the objects
[08:07] of collection.
[08:08] I'm going to discuss more about this in the coming lectures.
[08:10] For now, if you try to look at these reverse() method, it is returning the SequencedCollection,
[08:15] whereas inside the SequencedSet it is trying to return the SequencedSet, which is the subclass
[08:22] of SequencedCollection itself.
[08:23] That means SequencedSet
[08:25] it is trying to provide the signature which is more specific to the Set data structure.
[08:31] You may have a question why can't they use the same SequencedCollection inside the SequencedSet?
[08:36] The reason is very simple the way other collection data structures like List and the Queue which are
[08:42] directly inheriting SequencedCollection.
[08:45] The way they work is different compared to the Set.
[08:48] That's why there is a special interface developed with the name SequencedSet, and inside these the
[08:54] only abstract method that they are trying to override from the SequencedCollection is reversed() method.
[09:00] And inside this reversed() method, the return type is SequencedSet, which is the child of
[09:06] SequencedCollection.
[09:07] That's why we are not getting any compilation error.
[09:09] Please remember our inheritance related discussions.
[09:12] While you're trying to override the parent interface methods, you can always use the same data type
[09:19] or the sub data types.
[09:21] So here we are trying to use a sub data type as an return type.
[09:24] I hope you are clear about the SequencedCollection and SequencedSet.
[09:28] Now let's try to see what do we have around the SequencedMap. We discussed SequencedMap is specific
[09:35] to the Map data structure.
[09:36] That's why it is extending the Map interface. Inside Map always the elements are the objects that are
[09:42] going to be stored in a format of key and value.
[09:46] That's why you are able to see these K and V representing two different data.
[09:51] Type K represents the data type of your key, V represents the data type of your value object inside
[09:58] these interface
[09:59] also we
[09:59] similar kind of methods inside the Map
[10:03] we don't call the objects that we stored as an element, we call them as entry.
[10:08] That's why we have first entry, last entry to fetch them.
[10:12] Similarly, pollFirstEntry() and pollLastEntry() poll related methods will help us to remove the first
[10:19] entry and last entry.
[10:21] Polling is a jargon which is equivalent to remove() inside Map. Coming to the put, put is same as adding
[10:27] an element or adding an entry into the Collection object.
[10:31] So these putFirst() and putLast().
[10:34] They are going to help you in adding the first entry and the last entry.
[10:38] And at last we have reversed() method also, which is going to help us to reverse the mapped entries that
[10:44] we have.
[10:45] Everything that we discussed around the SequencedCollections I have mentioned in these slides.
[10:51] Please refer them whenever you want to revise very quickly around the SequencedCollections.
[10:56] If something is not clear, don't worry, it is all going to make sense to you.
[11:01] Once we started using these concepts as part of our demos, I hope you're having fun.
[11:06] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
