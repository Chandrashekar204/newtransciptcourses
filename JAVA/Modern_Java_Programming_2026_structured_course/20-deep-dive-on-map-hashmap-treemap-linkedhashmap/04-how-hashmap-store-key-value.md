# 20.4 — How HashMap Store Key, Value

> Section 20: Deep dive on Map, HashMap, TreeMap, LinkedHashMap

[00:00] So whenever you try to attend an interview around Java and if the question is around HashMap, the toughest
[00:06] question that you can expect around the topic, which is how a HashMap stores the data internally.
[00:14] In the case of List and Set, or any other data structure where they store a single element or a single
[00:20] object with respect to to those data structures.
[00:23] The storage mechanism is very simple.
[00:25] They will be stored somewhere in the heap location.
[00:28] But coming to the map, this is going to be something different every time.
[00:33] Whenever we are trying to store an entry inside the HashMap, the entry has to be stored in a key and
[00:38] the value format.
[00:39] And if we ask the HashMap by providing a key, it has to return the same value object that we initially
[00:46] stored.
[00:47] To make this work, behind the scenes, HashMap is going to do a lot of work.
[00:52] As a Java developer, you need to understand the internal working of HashMap.
[00:57] That's why inside this lecture, let's try to understand how HashMap store the key and the values inside
[01:03] the memory location are inside the heap memory.
[01:06] Whenever we try to create an object of HashMap behind the scenes my JVM, it is going to create few
[01:14] buckets like you can see here.
[01:16] The JVM has created 16 different buckets.
[01:19] Each of these buckets are going to be represented by an index number right from 0 to 15.
[01:25] So this is just a sample representation.
[01:27] With the sample representation.
[01:29] Don't be under the assumption that all the indexes and all the buckets, they are going to be stored
[01:35] in a SequencedManner.
[01:36] It's not going to happen that way
[01:38] the HashMap can create the buckets and indexes in any order.
[01:42] So once these buckets are created and the index numbers are tagged to these, each of these buckets
[01:49] inside these buckets and index numbers, only the key and values that we are trying to store inside
[01:54] a HashMap will be eventually stored.
[01:57] But here you may have a question which is how HashMap determines which bucket it has to store, or which
[02:04] index number it has to consider to store a particular key and value.
[02:08] So that's a great question.
[02:10] Let's try to answer the same behind the scenes HashMap is going to use the hashing principle or hashing
[02:17] algorithm, the HashMap.
[02:19] First it is going to calculate the hash code value of a given key.
[02:23] For example, here, if you try to store a key and a value which is India and New Delhi, first my HashMap
[02:30] .
[02:31] It is going to calculate the hash code of India String by invoking the hashCode() method present inside
[02:38] the String class.
[02:38] We know that String class has overridden the hashCode() method, which is inherited from the Object class.
[02:45] The same is going to be invoked by the JVM to calculate the hashCode() of a given string.
[02:51] In the case if your string is of type Person or Employee object, then definitely JVM is going to
[02:57] look.
[02:57] If you have any hashCode() method overridden inside your respective data type.
[03:02] Otherwise it is going to simply leverage the hash code present inside the Object superclass.
[03:08] Based upon our previous sections discussion, we know the default behavior of the hash code is to calculate
[03:13] the value based upon the memory location where it is stored inside the heap memory. So the memory location
[03:19] will be feed as an input to the hashing algorithm, and the output from this hashing algorithm will
[03:24] be the hash code, whereas with the String the behavior is going to change because the String class
[03:29] has overridden the hashCode() method to generate the hash code value based upon the content of the String.
[03:36] Let's imagine the hash code of the India String is 3492.
[03:41] By taking this hash code behind the scenes, the JVM will try to calculate the bucket index with the
[03:48] help of the hash code and with the length of the HashMap.
[03:51] As of now, you can see behind the scenes the JVM has created 16 different buckets.
[03:57] So that's why it is going to consider the maximum length as 16
[04:01] by using this maximum length and by using the hash code of the key element, it is going to calculate
[04:08] the bucket index value, which is going to be in the range of 0 to 15.
[04:13] Think like
[04:13] in our scenario the index is calculated as three.
[04:16] So with this calculation the India and its value which is New Delhi, it is going to be stored at the
[04:23] bucket or index three.
[04:25] The same kind of mechanism is going to repeat for all the remaining keys and values that you are trying
[04:32] to add.
[04:32] For example, think like this time I'm trying to add France and Paris.
[04:36] Based upon the above steps that we have discussed.
[04:39] Imagine this time the index is calculated as seven.
[04:43] So that's why the France and Paris is going to be stored at the index seven.
[04:48] Similarly, if you are trying to store Japan and Tokyo, and if the index is calculated at 11, the
[04:54] same is going to be stored at the 11th index or 11th bucket. In the scenarios
[04:59] where you are trying to send the key value as null.
[05:02] Then in such scenarios we can't calculate the hash code value.
[05:06] That's why whenever you are trying to pass null as a key, which you can do only once in these kind
[05:12] of scenarios, the key and its value is going to be stored at the index zero.
[05:17] That's why you can see we are storing the null, which is the key, and its value which is invalid at
[05:24] the zeroth index.
[05:25] As of now, this may look very simple to you, but there is some complex part which you need to understand.
[05:31] Let's try to understand the same.
[05:32] As of now, we have these kind of keys and values which are stored in different bucket index values.
[05:39] But like I said, there is a complex concept present inside the HashMap which is hash collision.
[05:45] Based upon our discussions around the hashCode() and the equals() method in the previous sections, we
[05:51] know that two different objects may have same hash code value.
[05:56] Ideally, if the hash code implementation inside a class is good, then obviously all the times you're
[06:02] going to get a unique hash code.
[06:04] But sometimes few classes are few data types
[06:07] they may result into same hash code value due to two reasons.
[06:12] One is due to the logic present inside the hashCode() method, or may be due to the reason that finite
[06:18] range of hash codes are available in comparison to the potentially infinite number of keys.
[06:24] We know hash code has a range which is equal to the range of Integer, but coming to the keys, we can
[06:31] store any number of keys.
[06:33] For example, if you take a String as an element data type using String, we can create infinite number
[06:40] of keys like I can have a string value a similarly b.
[06:43] Similarly, c I can write any number of keys with all the alphanumeric combinations.
[06:48] So with these two reasons, sometimes the JVM may calculate the same index number at the same bucket
[06:56] number for two different keys.
[06:58] So in those scenarios the hash collision is going to happen.
[07:02] So whenever these kind of hash collision occurs then obviously JVM has to look for a smarter mechanism
[07:09] to store multiple elements at a same bucket location or at a same index location.
[07:15] That's why to handle these kind of hash collisions, HashMap employs a strategy.
[07:20] One common strategy is, to use a data structure, like a LinkedList or binary tree, to store multiple
[07:28] key values in the same bucket.
[07:31] Let's try to understand the same by taking an example.
[07:33] Think like I have a country which is UK and it's a capital as London for some reason think like the
[07:39] hash code of this key, which is UK is 3492, which is same as for India.
[07:45] Since the hash codes are same, there is a very good chance that bucket index also is going to be calculated
[07:51] as three, where we already storing India.
[07:54] So with this hash collision my JVM, it is not going to override India with the UK.
[07:59] Instead it is going to convert these single element into a LinkedList. Like you can see here,
[08:06] this is how the UK and London is going to be stored.
[08:10] So this is a LinkedList where this is the first entry of the LinkedList followed by this is the second
[08:16] entry of the LinkedList.
[08:17] So that's why this first element is pointing to the address location of the second element inside the
[08:24] LinkedList in the similar lines think like
[08:27] this time I'm trying to store Brazil and its capital city for this
[08:30] also, let's imagine the bucket is calculated as 11 this time.
[08:35] Since the bucket index is calculated as 11.
[08:38] This Brazil and Brasilia is going to be stored after the Japan in the format of LinkedList, like you
[08:46] can see here.
[08:47] I hope you are clear about the process that HashMap follows to store a key and value.
[08:52] I also have a flowchart here for your reference.
[08:55] In the very first step, the developer is going to call the Map.put() method with the key and the
[09:00] value.
[09:01] So based upon the key and its data type, the hash code of the key is going to be calculated by invoking
[09:07] the hashCode() method present inside the key data type and using the same hash code behind the scenes,
[09:13] the index number or the bucket number is going to be calculated.
[09:17] Once the bucket number is calculated, my JVM is going to check if there is any key value
[09:22] pair is already present at a given bucket index.
[09:26] If it is no, then it is a straightforward scenario.
[09:29] The given key and value entries is going to be stored as a first element to node inside the LinkedList.
[09:35] Otherwise, if there is a hash collision, then my JVM first check if the key values are matching.
[09:41] There is a good chance that I may try to overwrite the value of a given key multiple times.
[09:47] In that scenarios, hash collision is always going to happen, so it is going to check if this is a
[09:53] true hash collision or the collision is happening just because we are using the same key value.
[09:58] So how it is going to check
[09:59] if we are using the same key value, it is going to check by using the equals method present inside
[10:05] your data type.
[10:06] Since in our example we are using the data type as String, it is going to invoke the equals() method.
[10:12] By using this key object and to the same, it is going to pass the existing key value present at the
[10:19] given bucket index.
[10:21] If both are equal, then that means we are trying to overwrite the value of a given key.
[10:26] Then in such scenarios this is going to happen, which is replace the existing node with the new value
[10:32] for a given key.
[10:33] Otherwise, if the key values are different, then obviously the new key and value is going to be added
[10:40] as a next node inside the LinkedList at a given bucket index.
[10:45] I hope you also realize the importance of hashCode() and equals() method that we discussed long back when
[10:51] we were trying to discuss about the Object superclass.
[10:54] So whenever you are trying to override the hashCode method, please make sure you are also overriding
[10:59] the equals() method and why we need these hashCode() and equals() method inside Object superclass.
[11:04] Because Map and its implementations like HashMap, they're always going to follow the hashing principle.
[11:11] So to make all these logic to work, every object or every data type inside Java, they should have
[11:17] the default hashCode() and the value() method inherited from the Object superclass
[11:22] in the worst case.
[11:24] The best case is they can overwrite this hashCode() and equals() method with their own respective logic.
[11:30] I hope you are clear on how the HashMap is going to store the key and values.
[11:34] In the next lecture, let's try to understand what is the process the HashMap is going to follow while
[11:40] it is trying to read the key and value from the existing buckets.
[11:45] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
