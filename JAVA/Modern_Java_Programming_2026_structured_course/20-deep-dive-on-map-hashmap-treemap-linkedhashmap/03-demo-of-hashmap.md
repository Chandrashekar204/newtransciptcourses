# 20.3 — Demo of HashMap

> Section 20: Deep dive on Map, HashMap, TreeMap, LinkedHashMap

[00:00] Let's see the demo on how to create an Map object inside this lecture.
[00:05] Since we are into the new section, I have created a Java project with the name section_20
[00:10] the same
[00:11] I'm going to upload inside the GitHub repo for your reference inside this project.
[00:15] As of now you can see we don't have any package.
[00:18] Let me try to create a new package with the name com.eazybytes.map.
[00:25] Inside this package, I'm going to create a new Java class with the name hash MapDemo.
[00:32] Since Map is an interface, we can't create an object of Map.
[00:37] Instead, we need to look for the implementation classes of the Map interface.
[00:41] One such famous implementation class is HashMap.
[00:46] If you're not able to see the HashMap inside the JDK library, please make sure to change the value
[00:51] inside these drop down to all places.
[00:54] With that, you will be able to see the HashMap class which is present inside the java.util package.
[01:00] Here you can see this HashMap is extending various abstract classes and implementing various interfaces
[01:07] like Map, Cloneable, Serializable.
[01:09] And at the same time it is also extending the abstract class with the name Abstract Map.
[01:14] So let's try to create an object of Map with the help of these implementation class.
[01:20] Here first I'm going to create the main() method inside the main() method.
[01:24] First I'm going to type Map and inside the angle brackets I'm going to mention the key data type as
[01:31] String followed by value data type as String.
[01:35] Close that I'm going to give the name to my Map object variable.
[01:39] So the name I'm going to give here is CountryMap to this
[01:43] on the right hand side I'm going to mention the code which is new HashMap.
[01:47] And at last I can mention semicolon.
[01:50] You can see on the right hand side I'm trying to use the diamond operator.
[01:53] That's why I'm not trying to mention the same String, String on the right hand side.
[01:58] So this is one approach to create and Map object with the help of HashMap.
[02:02] There are multiple other approaches like on the left hand side you can mention the same HashMap as
[02:07] well
[02:07] that also works.
[02:08] Otherwise you can simply use the var keyword as well.
[02:11] Like here
[02:12] you can mention var CountryMap.
[02:14] And whenever you are using var to declare a HashMap object, you need to make sure you are mentioning
[02:19] the type details on the right hand side like you can see here.
[02:22] So this is one approach.
[02:24] So these are all very similar to what we have discussed as part of ArrayList and LinkedList.
[02:29] There is nothing new here.
[02:31] The only difference is for HashMap you need to provide two data type values.
[02:36] Since HashMap is going to store the data in the form of key and value.
[02:41] Now using these CountryMap object, I'm going to store some data.
[02:45] With the help of this CountryMap, I can invoke the put() method using put() method,
[02:50] we can add the elements or objects into the HashMap object.
[02:55] So first I'm trying to store the details about the India and its capital city.
[03:01] So the first element are the object that I need to mention here is India.
[03:06] So this is going to act as a key inside your HashMap followed by I'm going to mention the value corresponding
[03:12] to its key.
[03:13] So here I'm going to mention the value as New Delhi in the similar lines.
[03:18] I'm also going to add details around USA and its capital city.
[03:24] So the capital city of USA is Washington, D.C..
[03:28] Let me try to add one more country details.
[03:30] This time I'm going to mention the country name as France, followed by its capital city, which is
[03:37] Paris.
[03:37] HashMap also allows you to define a null key and a null value.
[03:42] Let me try to do the same, like here.
[03:45] I'm going to mention CountryMap.put() and the key I'm going to mention as null followed by value.
[03:51] Also I'm going to mention as null.
[03:53] But please note that we can't define the null key or any key value more than one time.
[03:58] That means the HashMap or any of the Map implementation, as they are not going to allow the duplicate
[04:05] key elements.
[04:06] The values can be duplicated for different different keys.
[04:09] For example, here for the France we have Paris if needed
[04:13] for India
[04:14] also, we can maintain the value as Paris.
[04:17] This is completely allowed, but if you try to do the other way for key, then it is not allowed for
[04:23] the key
[04:23] duplicate elements are not allowed if you try to repeat the same code.
[04:27] And for India, if you're trying to mention that a different value, maybe New Delhi 1.
[04:34] In such scenarios, whatever value that you have stored previously in the very first place, the same
[04:40] is going to be Overrided.
[04:41] And this is going to be the latest value, which is going to be considered by your Map object.
[04:46] So whenever you try to use the same key name multiple times, the value is going to be overrided against
[04:53] that key.
[04:53] So this confirms that we cannot use a duplicate key elements, but we can have duplicate
[05:00] values.
[05:00] And with that, it also makes sense that only a single key can have a null value, whereas any number
[05:07] of values they can have null as an value.
[05:11] One more important character of HashMap is, HashMap is not going to maintain the order of insertion.
[05:17] Here, the very first element we have inserted is India, followed by USA followed by France.
[05:23] The same order is not going to be followed by the HashMap.
[05:26] When it is trying to store all of them inside a memory location. They can be stored at a random locations
[05:32] when you try to loop all these elements inside a HashMap, you will get random elements because HashMap
[05:39] never stored them in a proper insertion order.
[05:43] But this doesn't mean we can't store the elements inside a Map in a sequenced order
[05:48] there are other implementation classes like LinkedHashMap, which is going to help us to store the
[05:54] elements in a Map object in the same insertion order.
[05:58] We are going to see the Demo of LinkedHashMap in the coming lectures.
[06:02] Since HashMap is not going to maintain the order of insertion.
[06:06] If you see hash map is not going to implement the interface which is SequencedMap.
[06:12] Whereas if you look for the other implementation which is LinkedHashMap, it is going to implement
[06:18] the SequencedMap.
[06:19] So the basic requirement whenever a data structure want to implement sequence related interfaces like
[06:26] SequencedMap is, they need to maintain the elements based upon the insertion order.
[06:32] Otherwise they can't implement these sequenced interfaces.
[06:36] That's why for HashMap we are not seeing any implementation around the SequencedMap.
[06:40] I hope this makes sense.
[06:41] As of now, we are only trying to add the elements into the HashMap.
[06:46] As a next step, let me show you how to fetch a value based upon a given key.
[06:50] For the same we have a get() method.
[06:52] Let me try to get the values based upon a key and print the same onto the console.
[06:58] So here I'm going to invoke the CountryMap.get() method.
[07:03] To this get() method, I'm going to pass the same key that I have mentioned in the above code.
[07:08] I'm going to mention the key value as India.
[07:11] So if I try to execute this program, I'll be able to see New Delhi in the output.
[07:16] Similarly, we can also try to invoke the remove() method.
[07:19] Maybe I can try to remove the element inside my HashMap by providing the key as null.
[07:26] And with that, this entry which we have with the value null comma null is going to be removed.
[07:32] Post that I can try to check the size of my HashMap object with the help of CountryMap.size(),
[07:39] so we should get the size as three.
[07:42] Here you can see with this code we added four different entries inside my HashMap object, but with
[07:49] the remove code we are going to delete one of the entry with the key null and its value also null.
[07:55] That's why when we execute this code, we are going to get the output as three.
[07:59] So let's confirm the same by executing the program.
[08:01] And you can see we are getting the expected output.
[08:04] So this is a demo on how to invoke the most important methods available inside Map data structure.
[08:10] In the coming sections I'm going to teach you how to iterate the elements inside a Map object.
[08:17] But before that, we need to understand about an important concept or important topic around Map.
[08:23] This topic is super, super important from interviews perspective, so let's try to understand the same
[08:29] in the next lecture.
[08:30] I'm going to reveal about this topic in the next lecture.
[08:34] So I'm going to keep you waited around this.
[08:36] Thank you
[08:37] and I'll catch you in the next lecture bye.

----------------------------------------
