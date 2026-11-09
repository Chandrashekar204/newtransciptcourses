# 20.2 — Introduction to Map in Java

> Section 20: Deep dive on Map, HashMap, TreeMap, LinkedHashMap

[00:00] Why do we use dictionary?
[00:02] Whenever we want to understand the meaning of a given word, we will refer to that dictionary.
[00:07] The way the data are stored inside the dictionary is in the form of key and value.
[00:13] Whenever we are trying to look for a given word and its meaning, first we are going to search the dictionary
[00:18] for a given word.
[00:20] Later on, against that word, we will be able to identify the meaning of the same. In a similar manner
[00:26] in real projects
[00:27] also, we will get requirements to store the data in the form of key and value.
[00:33] For example, inside the e-commerce website, you may have to store the order details in the form of
[00:39] what is the product and what is the quantity of the product that is ordered by a given customer.
[00:44] To address all these kind of requirements, we have a data structure inside Java collections with the
[00:51] name Map.
[00:51] Compared to other data structures like List and Set, Map is going to store the data in a different
[00:57] format.
[00:58] That's why inside the collection framework hierarchy as well, you can see the Map interface and its
[01:03] implementations
[01:04] they are being maintained separately
[01:06] they don't have any relationship with the collection or iterable or any of the other data structures
[01:11] like List, Queue, Set.
[01:13] Understanding about the map data structure is very important for any Java developer.
[01:19] The same kind of data structure is available inside other languages as well.
[01:23] For example, inside Python we call this data structure with the name as dictionary, whereas inside
[01:29] the Java the same data structure which is capable of storing the data in the form of key and value,
[01:34] we call it as Map.
[01:36] And there are good amount of implementations around Map, and we are going to discuss few of them throughout
[01:42] this section.
[01:42] Inside this lecture, first, let's try to understand the basic details about the Map.
[01:47] In Java Collection framework.
[01:48] The Map is an interface which is used to represent a mapping between keys and values.
[01:54] We can store multiple elements and objects inside Map in the form of key and value, with the help of
[02:01] Map and its implementation classes, we will be able to store, retrieve, and manipulate data based
[02:08] upon keys.
[02:09] Like I said before, inside Java Collection framework Map interface has many implementation classes,
[02:16] but the most commonly used implementation classes are.
[02:19] HashMap, Treemap, LinkedHashMap.
[02:22] That's why inside this section we are going to focus on these three implementations.
[02:26] Let's try to take a scenario or an example to understand under which scenarios we need to use Map or
[02:33] its implementation classes.
[02:35] Think like you have a requirement to store the information about the countries and their respective
[02:41] capitals.
[02:42] In this kind of scenarios, Map data structure is going to be the perfect answer.
[02:47] Like you can see here
[02:48] under the key name we can store all the country names, whereas under the values we can store the capitals.
[02:55] Like for India the capital is New Delhi.
[02:57] Similarly for USA the capital is Washington, D.C..
[03:01] I hope this is making sense to you.
[03:03] Let's try to understand a few more details about Map like we discussed
[03:07] Map is a part of Java collection framework, but it does not extend the collection interface or Iterable
[03:13] interface.
[03:14] This Map interface is built with the help of generics.
[03:18] Inside Map interface, you will be able to see two parameterized types with the variables K and V.
[03:24] K represents the type of the key held by the Map, whereas we represent the type of the values that
[03:31] the keys are going to be mapped to.
[03:34] For example, if you're trying to build a Map object, which is going to store the key with the help
[03:39] of String data type and the values with the help of Person data type.
[03:43] Then in such scenarios inside these angle brackets, you need to mention two data types like String,
[03:48] Person.
[03:49] So the String data type is going to represent the key data type.
[03:52] Whereas Person data type is going to represent the value object data type.
[03:57] Inside the same Map interface we have another nested interface with the name entry.
[04:02] This entry nested interface is going to use to represent a single key and a value pair.
[04:10] I'll be showing this interface in few seconds.
[04:12] Before that, let me highlight about the most important methods
[04:15] inside Map interface.
[04:17] We can use put() method to add a new set of key and value pair inside the Map, whereas to read or to
[04:25] fetch the values, we can use the get() method.
[04:28] And to this get() method we need to pass what is the specified key.
[04:33] Whereas for the put() method, since we are trying to add a new pair of key and value, we need to pass
[04:38] both the key and the value.
[04:40] And whenever you want to remove a particular key and value pair from the Map object, you can invoke
[04:47] remove() method, and to this method you need to pass the specified key as an input.
[04:53] I hope this makes sense to you.
[04:54] As a next step, let's try to open this Map interface inside IntelliJ and try to understand
[05:00] about all the important data points that we have discussed so far. Inside my IntelliJ Idea
[05:05] you can see I have opened the Map.Java interface and it is present inside the same package.
[05:10] Like other collection data structures, the package is java.util.
[05:15] If you try to look at the class definition of these Map interface, you will be able to see two generic
[05:21] type parameters like K and V.
[05:23] Like we discussed, K represents the type of the keys maintained by the Map, whereas we represent that
[05:29] type of the mapped values.
[05:31] This interface also has good amount of methods.
[05:35] For example, with the help of the size(), we'll be able to know how many key and value pairs are stored
[05:40] inside a Map object.
[05:42] Similarly, we have a isEmpty() method.
[05:44] Let me open the list of methods available here.
[05:46] There are too many methods.
[05:48] We don't have to discuss all of them.
[05:50] Most of the times we will end up using most important methods that we are going to discuss inside this
[05:55] section.
[05:55] But if you have some special scenario or some special requirement which you cannot achieve with the
[06:01] help of most important methods, then you can always come into this interface and try to look for a
[06:07] method that is going to help you to implement your requirements.
[06:11] Inside this interface, we have put related methods which are going to help you to add and key value
[06:17] pairs.
[06:17] Similarly, like I said, get related methods
[06:20] they are going to help you to fetch the value based upon a given key.
[06:25] And at last we also have remove related methods.
[06:28] Let's try to check about the nested interface that we have inside these interface which is entry.
[06:34] So you can see there is an interface with the name entry.
[06:38] The purpose of this entry interface is it is going to be used to represent a pair which is key and its
[06:45] value.
[06:46] Inside this Entry interface we also have methods using which we'll be able to fetch,
[06:50] what is the key and what is the value.
[06:52] Similarly, we have Set values.
[06:54] You can think this Entry as an placeholder to hold both the key and the value details in a single object.
[07:03] I'm going to show you the demo on how to use this Entry interface inside your programming languages
[07:08] in the coming lectures, but with the discussion that we have done so far, I'm assuming you have some
[07:13] basic idea about the purpose of Map and how to store the data with the help of Map.
[07:19] Let's continue this journey of Map and its implementation classes from the next lecture.
[07:24] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
