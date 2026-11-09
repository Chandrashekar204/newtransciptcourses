# 20.9 — Introduction to TreeMap in Java

> Section 20: Deep dive on Map, HashMap, TreeMap, LinkedHashMap

[00:00] Inside this lecture, let's try to discuss about another famous implementation of Map inside Java collection
[00:07] framework, which is TreeMap.
[00:09] There are few drawbacks with HashMap.
[00:11] One such drawback is HashMap is not going to support the sorting of elements.
[00:17] Whenever you're working on requirements to maintain your entries inside a Map in an sorting order,
[00:24] whether it can be an ascending or descending order.
[00:26] In such scenarios, you can use a TreeMap.
[00:29] TreeMap is a class inside Java collection framework which built based upon the red black tree.
[00:37] So there is a data structure in computer science with the name red-black tree.
[00:41] We already discussed about these tree while we are discussing about the HashMap improvements inside
[00:47] Java 8.
[00:48] In the previous lecture, I said HashMap.
[00:51] It is going to have the tree like structure to store the elements inside the same bucket.
[00:56] The same Tree data structure is going to be followed even with the TreeMap as well.
[01:01] Whatever key values that we are trying to store inside these TreeMap, they are all going to be stored
[01:07] in an sorted order based upon the keys that we provide.
[01:11] The sorting is always going to happen based upon the keys, but not based upon the values.
[01:15] This TreeMap is a class which is implementing various other interfaces like Map, SortedMap, Navigable
[01:23] NavigableMap.
[01:23] Let's try to see an example of this TreeMap.
[01:26] In order to create a TreeMap object, you can follow the same syntax like HashMap.
[01:31] Instead of HashMap, you need to mention TreeMap on the right hand side, whereas on the left hand
[01:36] side you can mention the Map interface, and inside the generics you need to mention what is the data
[01:41] type of your key and value.
[01:43] Here I'm trying to store all the keys in a numerical format.
[01:48] That's why I'm trying to mention that data type as integer, followed by value with the data type as
[01:54] String.
[01:55] Each of the key I'm trying to store with a corresponding value here.
[02:00] Using this 23 key, I'm trying to store its corresponding spelling.
[02:04] The same applies for 12, 42, 3, 19, 48, 76.
[02:08] If you see here this is the order of insertion.
[02:11] But by the time I try to iterate the entries inside this TreeMap with the help of EntrySet, and if
[02:18] I try to print their keys and values, I'm going to get the output in an ascending sorting order.
[02:24] So always the sorting is going to happen based upon the natural order of your key object.
[02:30] If needed
[02:31] you can also define your own comparator and define the comparison logic inside it and the same comparator
[02:37] you can feed it to this TreeMapper class.
[02:40] With the help of the constructor.
[02:41] We are going to explore all those in few seconds.
[02:44] But before we try to see the demo of this TreeMap, I want to highlight a few more important points,
[02:50] which is TreeMap cannot contain any null key because if you try to provide a null key to TreeMap,
[02:57] it cannot perform the sorting, whereas null key is always allowed for HashMap because hash map does
[03:03] not maintain any order or sorting.
[03:06] So always if you need to access the keys in a sorted order, TreeMap is a better choice.
[03:12] On top of this TreeMap
[03:13] also provides some efficient methods for searching your keys, like finding the very first key.
[03:20] Last key are finding the keys within a specified range.
[03:24] So all these kind of methods, they are going to be available inside TreeMap.
[03:28] And this is possible since all the keys are sorted by default inside the TreeMaps.
[03:33] Let me show you how these values they are going to be stored using these red black tree algorithm or
[03:40] data structure.
[03:41] If you try to take the same example that we have discussed before, this is how the data is going to
[03:46] be stored.
[03:46] The very first key, which is 23, it is going to be present at the top.
[03:51] So this is going to be top root element inside the tree, followed by the second key which is 12.
[03:57] Since it is less than 23 it is going to be stored on the left hand side and coming to the 42.
[04:03] Since this is greater than 23, it is going to be stored on the right hand side later on for three.
[04:08] Since it is less than 23, it is going to store on the left hand side and compared to two since it is
[04:14] less, it is going to store to the left of 12.
[04:17] After three we have 19.
[04:19] Since 19 is less than 23, it will come onto the left side compared to 12.
[04:24] Since it is greater, we are going to store on the right hand side.
[04:28] After 19 we have 48, this 48
[04:31] since it is greater than 23, it is going to store on the right hand side, but compared to 42 which
[04:36] is already present, since it is greater than 42, it is going to be stored on the right leaf or on
[04:43] the right side, and after the 48
[04:45] since this is also greater than 23, it will come on the right hand side, and since it is greater than
[04:50] 42 and 48, it will be stored to the right side of the 48.
[04:54] So this is how internally TreeMap is going to store the data in
[04:59] an sorted format.
[05:01] You can see everything that is greater than 23.
[05:04] We have on the right hand side. When we try to iterate the elements our entries inside a TreeMap, it
[05:11] is going to provide the keys in a natural sorted order, which is ascending order.
[05:16] I hope you are clear about this theory
[05:18] discussion around the TreeMap.
[05:20] In the next lecture, let's see the demo of this TreeMap by writing a program inside Intellige.
[05:25] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
