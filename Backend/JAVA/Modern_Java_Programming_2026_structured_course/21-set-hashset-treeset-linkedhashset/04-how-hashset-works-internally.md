# 21.4 — How HashSet works internally

> Section 21: Set, HashSet, TreeSet, LinkedHashSet

[00:00] Inside this lecture, we are going deep to understand how HashSet works internally.
[00:07] I'm pretty sure that most of the Java developers may not be aware that HashSet is internally implemented
[00:16] using HashMap.
[00:17] In order to understand how HashSet works, first, a developer has to understand how HashMap works internally
[00:23] using the same concepts of hashing hashCode() and equals() method HashSet
[00:29] also is going to operate.
[00:30] Since we already discussed about HashMap internal working in the previous section, I'm assuming there
[00:36] is no need to discuss one more time about how HashMap works internally.
[00:41] If you have any questions, or if you want to recall that discussion very quickly, you can refer to
[00:46] the previous section slides, or you can quickly rewatch the videos of previous section where we have
[00:52] discussed about the HashMap internal working.
[00:54] With this, you may wonder why HashSet, which stores only one objects, utilizes HashMap,
[01:01] which typically designed for key value pairs.
[01:04] So let's try to understand the same.
[01:06] We know HashSet implements a Set interface, and with that, HashSet has an responsibility to maintain
[01:13] the uniqueness of the elements. To accomplish the same,
[01:16] all the elements inside a HashSet
[01:19] they are going to be stored consistently as a keys inside an internal HashMap.
[01:25] We know that already HashMap allows only unique keys.
[01:29] The same is being exploited by the HashSet to maintain the unique elements.
[01:34] I know you may not still convince when I say HashSet internally uses HashMap.
[01:38] Let me show you some proofs or evidence so that you are going to believe me without any questions.
[01:43] Like you can see here.
[01:45] This is the code that you can find if you look into the constructor code of HashSet inside the constructor
[01:52] of HashSet, what is the code that we have?
[01:54] We are trying to create a new object of HashMap.
[01:57] Let's validate the same inside the HashSet class.
[02:00] So here you can see I'm trying to create the object of HashSet with the constructor of HashSet class.
[02:05] So let me click on this and with that you will be able to see inside this constructor of the HashSet
[02:11] we are creating a object of HashMap.
[02:15] So with this code we are going to get an empty HashMap.
[02:18] Even if you check the other constructors that we have here, you can see this constructor.
[02:23] It is going to accept a List as an input or any other collection object as an input.
[02:28] So behind the scenes with the items that we are sending as an input internally, it is going to create
[02:34] an HashMap with all the collection elements that we are trying to send.
[02:38] So that's why you can see here it is invoking a addAll() method which will add all the elements to this
[02:44] Map object.
[02:45] Very similarly, we also have other constructors inside the HashSet where we can try to provide what
[02:51] is the load factor?
[02:52] What is the initial capacity.
[02:53] So here also a HashMap is going to be created with the same initial capacity and load factor.
[02:59] So what is an initial capacity?
[03:01] Initial capacity is a value that represents with how many buckets a HashMap is going to get started.
[03:07] By default, the initial capacity is going to be 16.
[03:11] That means whenever we are trying to create an HashMap object very first time, it is going to start
[03:17] with the 16 buckets.
[03:18] Inside those 16 buckets, it will try to store the elements or objects, but when most of the buckets
[03:25] are full, either with the LinkedList or with the TreeMap, then in such scenarios, the HashMap buckets
[03:31] are going to be incremented based upon the load factor value.
[03:35] So by default the load factor value is 0.75.
[03:38] If needed, we can change the initial capacity and the load factor.
[03:41] By invoking these constructor.
[03:44] The same values are going to be feed to these HashMap.
[03:47] Object creation code.
[03:49] I hope you got a confirmation now that internally HashSet uses HashMap.
[03:54] Now let's try to solve another question that you may have, which is whenever we are trying to add elements
[03:59] to the HashSet object, we are only passing a single object.
[04:04] We are not passing the data in a key and value format.
[04:07] So with this kind of data, how it is going to stored in an HashMap format, to understand the same,
[04:13] you can open the add() method available inside the HashSet.
[04:18] Here you can see whenever we are trying to pass a element to this add() method behind the scenes, it
[04:23] is going to invoke the put() method with the element that you have passed as an key, and the value is
[04:30] going to be present.
[04:31] So all the keys inside this HashMap, they are all going to have the same value which is present.
[04:36] So this present is a constant inside the HashSet.
[04:40] So you can consider this present as a dummy value or a dummy object which is going to be associated
[04:47] against each element that you are going to store inside your HashSet.
[04:51] So with the code snippet that we have seen inside the add() method of the HashSet, it is evident that
[04:57] whenever we are trying to invoke the add() method of the HashSet
[05:00] I said internally, the JDK library is going to invoke the put() method of the Map.
[05:05] So let's try to visualize how this data is going to be stored.
[05:09] Like you can see here, I'm trying to store four different country names as elements inside my HashSet.
[05:15] So this is how we are feeding the information to the HashSet add() method.
[05:20] But by the time the add() method invocation is completed, all your data is going to be converted into
[05:26] an internal HashMap with the elements that you provided as key.
[05:30] And all of these elements are going to have the same value which is present.
[05:34] I hope this makes sense to you.
[05:36] Now moving on to the next important point, which is HashSet is not going to offer a direct method to
[05:43] retrieve a particular element or object.
[05:46] For example, whenever we are using the HashMap or Map implementations, we can use the get() method,
[05:52] and to the get() method, we can pass the key as an input and based upon the key, the get() method is going
[05:57] to return the value that we stored inside a HashMap. And similarly inside a List or its implementation
[06:03] classes
[06:03] we can invoke the get() method along with the index number where the given element is stored.
[06:09] So based upon the index number, the corresponding element is going to be fetched and the same is going
[06:14] to be returned.
[06:15] But coming to the HashSet, there is no direct way to read a particular object.
[06:19] The only way to retrieve and read the elements inside a HashSet is by iterating the entire HashSet.
[06:26] We can iterate the HashSet with the help of iterator for block, for loop, and for each.
[06:32] We cannot use the List iterator for HashSet, because we can use list iterator only if a particular
[06:38] implementation maintains the order of insertion.
[06:42] Since HashSet is not going to maintain the order of insertion ListIterator is not present or applicable
[06:48] for HashSet. So this is the code available inside the iterator() method of HashSet.
[06:53] If you closely look at this iterator() method logic, you can see behind the scenes we are first invoking
[06:59] the key set based upon the internal map, and from these key set we are getting the iterator.
[07:06] So this iterator is going to have all the keys in a set format.
[07:10] Since all the keys are the elements that we stored with the help of HashSet, by the time we tried
[07:16] to iterate all the elements with the help of iterator, we will be able to see all the elements present
[07:21] inside the HashSet. Inside HashSet,
[07:23] we also have methods like contains(), remove().
[07:27] We can use this contains() method to check if there is an element already present inside the HashSet
[07:32] with a given value.
[07:33] Behind the scenes
[07:34] this contains() method is going to invoke the equals() method present inside your element data type class.
[07:41] To compare the values and with the help of remove() method, we can eliminate the objects or elements
[07:47] from the HashSet.
[07:48] Since HashSet is greatly using or getting influenced by the concepts of HashMap hashing, it is very
[07:56] important to implement both equals() and hashCode() methods inside your element data type.
[08:02] As of now, we're trying to store the elements of String data type.
[08:06] String already have the hashCode() and equals() method implementations.
[08:10] But if you are trying to store the custom data type objects inside the Set like Person objects or Employee
[08:17] objects in all those scenarios, please make sure you are overriding the equals and hashCode() method
[08:23] efficiently.
[08:24] Otherwise, you're going to face some performance issues.
[08:27] I hope this discussion makes sense to you.
[08:29] Let's validate this iterator logic inside the HashSet class.
[08:33] Inside my HashSet I'm going to look for iterator() method.
[08:37] And here you can see we are trying to invoke the keySet() method on top of the InternalMap.
[08:42] And using this key set we are going to get an iterator.
[08:46] Let's validate contains() method logic as well.
[08:49] If I try to open the contains() method, you can see internally it is trying to invoke the Map.contains()
[08:56] key with the element data that we are trying to send as an input to
[09:00] this contains() method. In the similar lines, if you try to open the remove() method, this also invoking
[09:06] Map.remove() method with the input data that we sent.
[09:10] Even when we invoke this behind the scenes, the Map.clear() method is going to be invoked.
[09:15] Let's try to invoke few of these methods.
[09:18] Inside my HashSet I'm going to invoke the contains() method.
[09:23] So to this contains() method I'm going to pass the value which is Dubai.
[09:28] So this contains() method is going to return the boolean as an output.
[09:33] So that's why on the left hand side I'm going to accept the output with the variable name is Dubai.
[09:40] So the same I can try to print out unto the console so that we can validate if that Dubai element is
[09:46] present or not.
[09:47] You can see we are getting the value as true.
[09:49] That means Dubai element is already present inside this Set. Instead of Dubai
[09:54] if I try to mention Germany this time we should get the output
[09:59] as false.
[09:59] Like you can see here we are getting the output as false.
[10:02] In the similar lines we can also invoke the remove() method.
[10:07] So I'll try to remove the Singapore country details from my asset.
[10:13] And this remove() method also is going to return the output in a boolean value, confirming whether the
[10:18] remove operation is successful or not.
[10:19] So that's why on the left hand side, I'm going to catch the output with a boolean variable name as
[10:25] is removed, and post that I'm going to print it
[10:28] what do we have inside the isRemoved followed by
[10:31] I'm also going to print out the HashSet object to confirm whether the Singapore country details are
[10:38] deleted.
[10:39] So if I execute this program, you can see we are getting the true from the remove() method and post that
[10:45] from the Set.
[10:46] The Singapore country details are removed.
[10:48] So this way you can use all these methods based upon your business logic.
[10:53] I hope this all clear to you.
[10:54] Thank you,
[10:55] bye.

----------------------------------------
