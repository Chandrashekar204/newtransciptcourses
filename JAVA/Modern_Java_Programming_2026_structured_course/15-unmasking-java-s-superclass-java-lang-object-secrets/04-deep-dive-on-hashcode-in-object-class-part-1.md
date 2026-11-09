# 15.4 — Deep dive on hashCode() in Object class - Part 1

> Section 15: Unmasking Java's Superclass(java.lang.Object) Secrets

[00:00] The next method that we are going to discuss from object class is hashCode().
[00:04] Before I try to discuss about this method, let me share an update related to getClass() method.
[00:10] Whatever we have discussed in the previous lecture, I have mentioned the same inside this slide
[00:15] for your reference.
[00:16] I forgot to mention about this in the previous lecture.
[00:19] That's why I'm trying to provide an update here.
[00:21] Now let's move to the hashCode() method.
[00:24] So what is a hashCode(),
[00:26] hashCode() is a special number that is calculated based upon the input information that we provide using
[00:34] a specific method, or a hash function, or a hash algorithm.
[00:38] In other words we can call this hashCode() as hash sum or hash value also.
[00:44] So it is a way of turning your information into an unique number. Like you can see here,
[00:50] first, I'm trying to provide some input data to my hash function or hash algorithm behind the scenes
[00:57] my hashing algorithm
[00:58] it is going to perform some good amount of calculations based upon the input data that I provide and
[01:04] accordingly it is going to provide me an output value which is an Integer value.
[01:09] So this output value which got generated with the help of hashing algorithm, we can call it as
[01:16] hasCode().
[01:17] In computing world, calculating a hash code is a one way process.
[01:21] When we create a hash code based upon a given input, it's like turning it into an secret code that's
[01:28] hard to turn back into the original String.
[01:31] That's why you can see in that diagram
[01:32] also, I have mentioned the arrow in only one direction.
[01:36] If someone has my hash code value, they will not be able to derive the original input data that is
[01:42] used by my hashing algorithm. In computing world hashing, used in many places, especially to store
[01:49] the passwords in a storage system.
[01:51] So if I try to store my password with the plain text inside a database, if someone steals my database
[01:57] records, they will be able to understand what is my password.
[02:01] So in all such scenarios, enterprise organizations, they will go with the hashing process where an
[02:06] end user, when he's trying to register into a website, his plaintext password will be converted into
[02:12] a hash value before storing into the database, so that even if someone steals my database records,
[02:19] they will not be able to understand what is my original password text. In the similar lines Java people
[02:26] also they are using the hashing process or hashing algorithm to calculate the hash code of an object
[02:33] based upon its content.
[02:35] The purpose of hashCode() method that we have inside the Object class is to simply return the hash code
[02:41] value of your object.
[02:44] In other words, the return type of this method is going to be an int value.
[02:48] Java framework provides a default implementation for these method, like whenever you're trying to compute
[02:55] an hash code for your given object behind the scenes Java
[02:59] by default it is going to convert the memory address of the object into an hash code value.
[03:05] We know inside Java each and every object it is going to be stored inside an heap memory at a memory
[03:12] location.
[03:12] The same memory location is going to be feed as an input data to the hashing algorithm, and whatever
[03:19] output that we get, it is an hash code value which generated based upon the memory location of the
[03:26] object.
[03:26] So this is the default behavior provided by the Java.
[03:30] If needed, we can override these default behavior.
[03:34] I'm going to show you how to override this default behavior in the coming lectures.
[03:38] For now, let's try to analyze this hash code method inside the Object class.
[03:43] Inside my Object class I'm going to look for hashCode() method.
[03:47] You can see this method also has native keyword, which means the actual implementation of this method
[03:55] is written inside the native language.
[03:57] That's why the native keyword is present.
[03:59] But compared to the getClass(), you will be able to see there is no final keyword.
[04:04] That means the subclasses
[04:06] if needed, they can override these hashCode() method.
[04:09] The return type of this method is going to be int value.
[04:13] We can also read more details about this method inside the comments that we have
[04:17] on top of this method, it is going to return a hash code value for the object.
[04:22] Along with that, we also have some other details, which I'm going to discuss in few seconds.
[04:27] With all the discussion that we are doing around the hash code, it is pretty clear that hashCode() method
[04:33] is used to calculate the hash code value of an object.
[04:37] With that you may have a question, which is why should we calculate the hash code of an object?
[04:43] What is the reason that we want to calculate the hash code value of an object?
[04:47] It's a great question.
[04:48] Let me try to answer the same.
[04:50] We can use the hash code value as a label that can help us in organizing and finding information quickly.
[04:59] Like I said before
[05:00] there is an advanced concept inside Java with the name collections using certain type of Java collections
[05:06] like HashMap() and HashSet, we should be able to store any amount of Java objects, for example
[05:13] using HashMap or HashSet data structures, I will be able to store any amount of objects.
[05:20] It can be thousand objects, 10,000 objects or 1 million objects.
[05:24] There is no limit.
[05:25] You can store any amount of objects inside these data structures like HashMap and HashSet.
[05:30] So these Java collections like HashMap and HashSet, they follow hash based data structure behind
[05:37] the scenes.
[05:37] So whenever we are trying to store thousands and billions of objects inside these collection classes,
[05:43] it is pretty obvious we should have an efficient solution to store the object at a given location,
[05:49] and similarly, we should be able to fetch the object from the same location very quickly. In these kind
[05:56] of scenarios, to efficiently store and fetch the object from the collection data structures like
[06:01] HashMap and HashSet, we are going to calculate the hashCode() value.
[06:05] For example
[06:06] this is how my hash map is going to look like behind the scenes inside the memory.
[06:11] As of now, you can see my hash map has eight buckets, but in real projects it can have 1000 buckets
[06:18] or 10,000 buckets or 1 million buckets based upon how many objects you are trying to store inside these
[06:24] HashMap.
[06:25] HashMap is a part of Java Collections framework.
[06:28] Whatever I'm going to discuss right now, it may not be super clear for you at this point of time because
[06:34] we are ready to discuss about HashMap, how it stores the data.
[06:37] For now, please try to observe whatever information that you can, but the only point that I'm trying
[06:42] to highlight from this discussion is inside Java hash
[06:45] code of an object needs to be calculated to store our objects inside data structures like HashMap
[06:52] and HashSet.
[06:53] Coming to the original discussion around the HashMap, whenever we want to store an object inside an
[06:59] HashMap, we are going to store in a format key and value.
[07:03] HashMap always allow you to store by providing a key and value.
[07:07] For example, I can provide the key as Monday and the value as weekday, and similarly I can also have
[07:15] a key which is Saturday and the value as weekend.
[07:19] So this way we can always store the data inside and hash map using key value structure.
[07:25] So whenever we are trying to store thousands of objects inside HashMap buckets, HashMap will be clueless
[07:31] about under which bucket it has to store your given value that you are trying to store with the help
[07:37] of a key.
[07:38] This is where hashCode() method comes into picture.
[07:41] So behind the scenes, whenever we are trying to store an object inside a hash map with the format of
[07:47] key and value my JVM, it is going to calculate the hash c code of my key object.
[07:53] Once the hash code is calculated based upon the hash code, it is going to identify one of the bucket
[07:59] inside hash map where it is going to store the given value object.
[08:03] So this process, it is going to do continuously for each and every key value object that you are trying
[08:10] to store inside the hash map.
[08:12] In future, whenever you want to retrieve your value object based upon a key in that scenario.
[08:18] Also, JVM is going to first calculate the what is the hash code value of a given key value, and accordingly
[08:25] it is going to find the bucket where your value object stored.
[08:29] There might be some special scenarios where two different key objects may have same hash code value.
[08:35] In such scenarios, and at the same bucket the value objects, they are going to be stored in an linked
[08:42] list data structure format.
[08:44] I know it might be too complex right now to understand.
[08:47] For now
[08:47] don't worry about hash map.
[08:49] I am going to teach you everything about hash map in the coming sections, but at least I'm assuming
[08:53] you are clear about the need or the necessity on calculating the hash code of an object inside Java.
[09:00] I hope it is clear.
[09:02] Let's continue the discussion around hash code in the next lecture as well.
[09:06] Thank you,
[09:06] bye.

----------------------------------------
