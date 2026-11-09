# 20.11 — Demo of LinkedHashMap in Java

> Section 20: Deep dive on Map, HashMap, TreeMap, LinkedHashMap

[00:00] The next most commonly used Map implementation is LinkedHashMap.
[00:06] LinkedHashMap is a class that extends HashMap class and implements SequencedMap.
[00:13] If you are looking for an Map implementation which is going to maintain the order of insertion, then
[00:20] you can happily use LinkedHashMap with the LinkedHashMap implementation,
[00:25] we are going to get the features or the characteristics from two different worlds.
[00:31] One is from the hash table and the other one from the LinkedList.
[00:34] Since this LinkedHashMap is going to maintain the order of insertion, you can see it is able to implement
[00:41] the SequencedMap, whereas the previously discussed map implementations like HashMap and a
[00:48] TreeMap.
[00:48] Since they are not going to maintain the order of insertion, we cannot implement the SequencedMap.
[00:54] Let's see an example on how to use this LinkedHashMap.
[00:57] Like you can see here
[00:58] on the right hand side, we just have to invoke the constructor of the LinkedHashMap class.
[01:04] Post that using the same LinkedHashMap object, you can try to add any number of entries like with
[01:11] their keys and values.
[01:12] Whatever order you have followed while inserting the Map entries, the same order is going to be retained.
[01:19] And when you try to iterate these key and values, you will be able to see the output in the same order.
[01:25] Here you can see we have added the key and the values with an order of 4, 1, 7, 2 the same we are able to
[01:32] see on the output.
[01:34] Let's try to validate this example of LinkedHashMap inside Intellige.
[01:38] Inside my IntelliJ Idea, I'm going to first look for LinkedHashMap.
[01:43] And here you can see it is extending the HashMap like whatever HashMap is providing you.
[01:49] This LinkedHashMap also is going to provide on top of that, since it is trying to implement the SequencedMap
[01:55] it is going to retain the order of insertion.
[01:59] Let's see the demo on how to create the object of this class.
[02:02] For the same, I'm going to create a new Java class with the name LinkedHashMapDemo.
[02:10] Once this class is created, we can try to create the main method by typing the shortcut which is PSVM.
[02:17] .
[02:18] Now I'll try to create an LinkedHashMap object by just typing Map Integer, String followed by
[02:28] the variable name as linkedHashMap.
[02:31] Post this on the right hand side
[02:33] we can type new operator followed by LinkedHashMap
[02:37] default constructor.
[02:38] Now using these variable name, I can try to invoke the put() method to add the elements.
[02:46] The very first element I'll try to insert here is with the key four and it's spelling
[02:52] f o u r
[02:53] So let me do the same for the key one as well.
[02:57] So here in the place of four I'm going to type one followed by o n e.
[03:01] After this I'm going to type seven followed by spelling of seven, which is s e v e n, followed by two
[03:10] with its spelling.
[03:11] So now what I am going to do is I'll try to iterate these LinkedHashMap by using its EntrySet.
[03:18] So let me type LinkedHashMap.EntrySet.
[03:23] Once this entrySet() method is invoked on the left hand side, I'll try to invoke Map.Entry and to
[03:30] this I'll try to pass the data types as Integer, String with a temporary variable name as entry.
[03:40] Now inside my
[03:41] for each loop, I can try to print out the key and its value.
[03:46] In order to print the key details, we need to invoke the getKey() method with the help of entry.
[03:53] After this, I'm going to mention append operator, which is plus followed by String with a colon.
[03:59] And after this string I'm going to mention plus symbol again.
[04:02] And at last I can try to invoke the getValue() method to print the value associated to a given key.
[04:11] Now, if I try to execute this program, you can see I'm getting the output in the same order that we
[04:18] have inserted the key and the values.
[04:20] So this confirms LinkedHashMap is going to maintain the order of insertion. If needed,
[04:27] you can also invoke the methods available inside the SequencedMap, but in order to do the same,
[04:34] you just need to make sure on the left hand side.
[04:36] Also, you are mentioning the LinkedHashMap so that using this variable we can try to invoke the methods
[04:44] like reversed, which will reverse the elements inside this HashMap.
[04:48] After invoking this reversed() method on the left hand side, I should be catching the output with a variable
[04:56] name as reversedLinkedHashMap().
[05:00] But the return type of the reversed() method is SequenceMap.
[05:03] That's why not to resolve this compilation error, we need to mention SequencedMap here.
[05:09] Now, using this reversedLinkedHashMap(), I can try to iterate the elements present inside these
[05:15] reverseLinkedHashMap. For the same,
[05:17] let me copy these for each loop.
[05:20] Here instead of this LinkedHashMap, I'm going to mention the variable name as reversedLinkedHashMap.
[05:25] Now, if I try to execute this program, you will be able to see that the output is also printed in
[05:32] the reverse order.
[05:33] So this confirms we should be able to use all the methods available inside the SequencedMap.
[05:40] So inside the SequencedMap, we have methods like reversed(), firstEntry(), lastEntry(), pollFirstEntry(),
[05:46] pollLastEntry(), putFirst() and putLast().
[05:50] All these methods we should be able to use whenever we are trying to use the LinkedHashMap object.
[05:56] I hope you are clear about the discussion around the LinkedHashMap.
[05:59] Please use this LinkedHashMap in the scenarios
[06:02] whenever you are looking for an map implementation option that is going to retain the order of insertion.
[06:08] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
