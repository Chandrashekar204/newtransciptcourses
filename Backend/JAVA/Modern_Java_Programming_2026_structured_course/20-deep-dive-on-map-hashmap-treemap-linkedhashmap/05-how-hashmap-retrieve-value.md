# 20.5 — How HashMap retrieve Value

> Section 20: Deep dive on Map, HashMap, TreeMap, LinkedHashMap

[00:00] Let's try to understand what is the process that is going to happen behind the scenes.
[00:04] Whenever we are trying to retrieve a value by providing a key to the get() method. For the same, let's
[00:11] consider the same examples and data that we have discussed in the previous lecture.
[00:16] So these are all the data that are saved at multiple indexes are at multiple buckets at a couple of
[00:23] buckets like three and 11.
[00:25] The data is stored in the form of LinkedList.
[00:28] Let's imagine one of the developer, he invoked the get() method by using the HashMap object and to the
[00:35] same get() method
[00:36] he also provided a key as an input.
[00:39] With this behind the scenes, what is going to happen is the JVM is going to take the key object, and
[00:44] it is going to generate the hash code by invoking the hashCode() method using the same hash code, it
[00:49] is going to perform the same calculations to derive the index number, or to derive that bucket number.
[00:56] Once the bucket number is identified, it is going to check if at a given bucket
[01:01] if there is single element or multiple elements are stored.
[01:05] If there is single element, then there is no confusion.
[01:08] It is going to return the value of that particular single key.
[01:12] For example, think like
[01:14] the developer invoked the get() method by passing the France as an key.
[01:19] So with this behind the scenes, the hash code and index number calculation is going to happen, and
[01:25] the same index number is going to be calculated with is seven.
[01:29] Since at the seventh bucket or seventh index we have single element inside the LinkedList, it is going
[01:35] to simply fetch the value which is Paris, and the same is going to be given as an output to the developer.
[01:42] To make all these work without any issues, we need to make sure that our key data type object is immutable
[01:49] in nature.
[01:50] If you try to use a mutable objects as an key data type, then you may get different output.
[01:56] Think like one of the developer.
[01:58] While trying to store he given a key value, but before the developer tried to get the value by using
[02:05] the same key thing, someone, a developer himself or herself change the key object because it is a
[02:12] mutable in such scenarios, definitely, while you're trying to fetch the value, you're going to get
[02:17] a different hash code.
[02:18] With a different hash code, you're going to get a different bucket number.
[02:22] And if the JVM tried to search in a different bucket number, you're always going to get the value as
[02:27] null.
[02:27] So to avoid these kind of issues, we need to make sure we are using the immutable objects as a key.
[02:34] For example, here we are trying to use a String as a key data type, which is going to be immutable
[02:40] always.
[02:41] So this is a very happy scenario or simple scenario.
[02:44] Now let's try to discuss about the scenario where the index or the bucket number is calculated as
[02:51] 3 or 11.
[02:51] In this kind of scenarios, at a given bucket location, there are multiple elements inside your LinkedList
[02:58] .
[02:58] So how my get() method will identify which value it has to return.
[03:03] So for this kind of scenarios the get() method are the JVM is going to rely on the equals() method to check
[03:11] if the given key is matching with the keys present here, like India and UK.
[03:17] So that's why behind the scenes, whenever we have multiple elements inside a LinkedList, the equals()
[03:22] method is going to be leveraged by the HashMap to fetch the values for a given key.
[03:28] For example, think like we are trying to fetch the capital city for the country UK.
[03:33] So based upon this UK key value, the hash code and the bucket index value is going to be calculated.
[03:40] So the index value will be three.
[03:42] So at three there are two different elements inside the LinkedList.
[03:46] That's why my JVM is also going to check if this India is equals to UK.
[03:52] If not it will keep on moving to the next element.
[03:55] And once a LinkedList node or element identified with the same given key value, its corresponding
[04:02] value is going to be returned as an output.
[04:05] So this is how the hash collision scenarios is going to be handled in the scenario of get() method.
[04:11] I also have a flowchart for your reference.
[04:14] In the very first step, the developer is going to invoke the get() method by providing the key as an
[04:20] input object.
[04:21] Based upon this key, the hash code is going to be calculated and based upon the hash code and the length
[04:27] of the HashMap, the bucket index number is going to be calculated. Based upon the bucket index number
[04:33] the JVM is going to check if at a given bucket location.
[04:37] If there are multiple LinkedList nodes available.
[04:40] If there is only a single element is available, this no step is going to be executed, which is
[04:45] return the value object from the single node inside the LinkedList.
[04:49] Otherwise, if there are multiple elements or node present inside a LinkedList available at a given
[04:55] bucket index, it is going to keep on going to compare the given.
[05:00] And key object with the already present keys inside the LinkedList nodes using the equals() method.
[05:06] Once a match is found, the corresponding value is going to be returned.
[05:09] I hope this is clear.
[05:11] Before I try to close this lecture, I want to share a couple of more important points.
[05:15] The very first one is don't be under the impression the HashMap is always going to have the 16 buckets
[05:22] only.
[05:22] As you try to add more and more entries into your HashMap object at some point of time, based upon
[05:28] the load factor defined inside the JDK library, the buckets are going to be increased and the new indexes
[05:34] are going to be considered to store the new entries.
[05:38] At what time that is going to happen?
[05:40] It is going to be depend on the logic written inside the JDK library.
[05:43] We don't have to discuss so much in depth.
[05:45] I'm just trying to provide this information for your reference.
[05:48] And the second point is, you may have a question which is how many elements are nodes we're going to
[05:54] store inside a LinkedList, like inside this bucket three can I store 1 million elements if the same
[06:01] is allowed inside all the buckets, where we can have a LinkedList of any length elements, then we
[06:07] can always live with these 15 buckets only.
[06:10] Is that possible
[06:11] this might be your question, but this also we don't have any control.
[06:14] Developer is not going to control this behavior.
[06:17] There is a limit on how many elements we can store in each bucket.
[06:21] So based upon this limit defined inside the JDK library, more buckets are more indexes are going to
[06:27] be added to your HashMap object.
[06:30] I hope this makes sense to you,
[06:32] thank you and I'll catch you in the next lecture, bye.

----------------------------------------
