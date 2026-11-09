# 20.12 — [JAVA 9] Creating Immutable Maps

> Section 20: Deep dive on Map, HashMap, TreeMap, LinkedHashMap

[00:00] Sometimes we may have a requirement to create immutable map objects, so that no other business logic
[00:08] or no other method can add or remove entries from a given Map object.
[00:13] To handle these kind of scenarios, you can happily use the static factory methods available inside
[00:20] the map interface.
[00:21] Just like how we have of() static methods inside a List interface.
[00:25] Very similarly, we also have often static factory methods inside Map interface as well.
[00:31] Apart from of() method, we also have another static method inside Map interface which is off entries
[00:38] in few seconds.
[00:39] We are going to discuss on how to use these static factory methods in order to create an Immutable Map
[00:46] object.
[00:46] But before that, let me highlight these half and half entries.
[00:50] Map static factory methods.
[00:52] They are introduced only from the Java 9. Before, in order to make a Map object as an immutable or
[00:59] unmodified object.
[01:01] This is the process that developers use to follow.
[01:04] First, they will create the Map with the given key and the value data types.
[01:08] Once they populated all the required entries inside the Map, they are going to send the same Map as
[01:15] an input to the method unmodifiableMap(), which is present inside the Collections class.
[01:21] So this unmodifiableMap() is a static method which is going to return the immutable or unmodifiable version
[01:29] of your Map object.
[01:31] But like you see, this is a two step process.
[01:34] Instead, from Java 9, we can happily use the static factory methods with the names half and half
[01:41] entries to directly create the immutable or Unmodifiable Map object.
[01:47] Let's see a few example on how to use these static factory methods, which are introduced in JDK nine
[01:53] or Java 9.
[01:54] Here you can see I'm trying to invoke the half static method with the help of Map interface to the same
[02:00] I'm trying to send the same data that we have here, so the very first one is the key one, followed
[02:06] by value one followed by key two
[02:08] value two,
[02:09] Key three, value three.
[02:10] This way there are multiple overloaded half static methods.
[02:14] Using these multiple overloaded methods, we will be able to easily create the immutable Map objects.
[02:22] There is also one more flavor which is off entries, so this is also a static factory method available
[02:28] inside Map interface.
[02:29] So whenever you are trying to invoke this method, you can pass any number of entries.
[02:36] There is no limit.
[02:37] You can pass thousand or 10,000 because this method, it is going to use the variable arguments as an
[02:44] input.
[02:45] So to this method, whenever we want to send the key and value, we need to invoke another static method
[02:51] available inside the Map interface, which is Map.entry to the same entry() method
[02:55] we need to pass what is the key and the value.
[02:57] So this approach you can always use whenever you have more than ten key value pairs that needs to be
[03:04] created inside a Map object.
[03:06] Whereas if your requirement is only to create key value pairs which are less than or equal to ten,
[03:12] then you can happily use the half static method, regardless of which approach you are trying to use
[03:18] to create the unmodifiable or immutable Map object.
[03:22] If anyone make an attempt to add a new entry or remove an existing entry, or someone is trying to update
[03:28] the value against a key in all these kind of scenarios, they are going to get a unsupported operation
[03:35] exception because your map right now is a immutable object.
[03:40] Let's see the demo of these approaches very quickly.
[03:43] Inside my intellig, I'm going to create a new Java class with the name ImmutableMapDemo. Inside this
[03:49] class
[03:50] first let me create the main() method followed by
[03:53] I'm also going to create one more static method which is public static void, and the method name I'm
[04:01] going to mention as processMap().
[04:03] To this method, I'm going to pass the input of type map with the key data type as String, followed
[04:10] by integer and parameter name.
[04:12] I'm going to keep it as StringIntegerMap.
[04:15] Inside this Map, I'm going to iterate all the entries that we have inside the Map object that this
[04:22] method is going to accept.
[04:24] For the same, I can try to use for each block.
[04:27] So first I'm going to mention Map.entry and inside the angle brackets I need to mention the same
[04:34] data types like String, Integer followed by variable name as entry followed by colon, followed
[04:40] by using the StringIntegerMap object.
[04:43] I'm going to invoke the EntrySet. Later on
[04:47] inside the for loop, I'm going to build a System.out.println(), which will print both the key
[04:54] and value details.
[04:55] So let me mention a String in between with the colon value and
[05:00] post that I'm going to invoke the getValue() method as well.
[05:04] So now my method is ready.
[05:06] I'm going to invoke this method from my main() method here
[05:09] first I'm going to create a Map object of type String, Integer and the variable name
[05:17] I'll mention it as StringIntegerMap.
[05:19] To this, I'm going to assign the immutable Map object that we are going to create with the help of
[05:24] of() method.
[05:25] So you can see there are multiple overloaded of() methods.
[05:28] You can use any of these of() method, but the maximum number of key and value pairs that you can send
[05:34] is up to ten pairs.
[05:36] Beyond that, we need to use off entries approach here
[05:40] first, let me send the key which is a followed by value of this key, which is one post that I'm going
[05:48] to type B, which is the key two, followed by value two, which is two, followed by C, which is going
[05:54] to act as a key three.
[05:55] And at last I'm going to mention three, which is going to act as a value three.
[05:59] So if I try to open this, I'll be able to open a static factory methods, which is capable of accepting
[06:06] three different keys along with their values.
[06:09] Similarly, we have many other overloaded methods.
[06:12] Like I said, at max we can send ten different keys with ten different values.
[06:17] Beyond that, we need to use the of() entries method.
[06:21] Now we can try to send this object as an input to this method.
[06:25] For the same, I'm going to invoke the processMap() method and send the StringIntegerMap object as
[06:31] an input.
[06:32] So if I try to execute this program, there won't be any errors.
[06:36] You can see we are getting the keys along with their values. But think like inside this method
[06:42] I'm trying to make some changes to my Map object.
[06:46] Maybe I'm trying to add a new entry by invoking StringIntegerMap.put().
[06:53] And to this put() method I'm sending the key as d followed by value as four.
[06:58] This time, if I try to execute this program, I will get an runtime exception which is
[07:04] UnsupportedOperationException.
[07:06] Since this is an unchecked exception, the compiler is nowhere forcing us to handle this exception.
[07:12] Similarly, if you are trying to remove also, you're going to get the error this time.
[07:17] Let me invoke this remove() method and to the same I'll pass the key value as a.
[07:22] So if I execute this program this time also, you can see I'm getting a UnsupportedOperationException.
[07:27] Similarly, if I try to update the same key with a different value
[07:31] also, I'm going to get a same runtime exception.
[07:35] This time you can see for the same key a I'm trying to send a different value, which is 11.
[07:40] So if I execute this program, you can see I'm getting the same exception.
[07:44] So this confirms that we are able to create the immutable or unmodifiable Map object with the help of
[07:51] these of() static factory method.
[07:54] So let me remove this line.
[07:56] Now this time I'm going to show you the demo of the second approach.
[08:00] For the same,
[08:00] let me copy the same method inside the same class.
[08:04] This time I'll keep the method name as processMap1().
[08:08] To this processMap1(), I'm going to send a Map object, which is going to store the key as an integer
[08:15] followed by value in the String format method input parameter I can change to IntegerStringMap.
[08:23] The same I can use inside the method logic as well.
[08:26] Here inside the Map.entry
[08:28] also, we need to swap the data types to Integer, String.
[08:33] As a next step inside my main() method, I'm going to invoke the Map.ofEntries() method.
[08:40] So this ofEntries() method is capable of accepting any number of entries because it is using the variable
[08:48] arguments as an input parameter.
[08:51] So whatever number of entries that you are trying to send, all of them, they are going to be iterated
[08:56] inside this method.
[08:57] And at the end you are going to get a Map object which is of type immutable or unmodifiable.
[09:03] I hope this makes sense.
[09:05] Let me go to my main class and here to this ofEntries() method.
[09:09] We need to send the entry details by invoking the entry method which is available inside the Map class.
[09:16] So here I'm going to mention the value as key as one followed by name, which is term.
[09:23] Think like
[09:23] I'm trying to build HashMap indicating my best friend details.
[09:27] So the term is the my first best friend.
[09:31] This way we can mention any number of entries, but instead of invoking these entry() method every time
[09:37] with the help of Map, what we can do is we can try to import it by just mentioning import static
[09:45] java.util.Map.Entry.
[09:50] So once the static method is imported, we can directly mention entry.
[09:55] Similarly, I'm also going to make the second entry with the help of
[10:00] entry() method to this method, I'm going to pass the key as two, followed by my second best friend who
[10:06] is Dick.
[10:06] Next, I'm going to make one more entry by copying the same code, and this time I'll just mention the
[10:12] entry as three, followed by a name which is Harry.
[10:17] This way we can pass any number of entries to these ofEntries() method, and on the left hand side we
[10:24] can try to create a variable of type Map Integer, String and the map object name as Integer
[10:33] IntegerStringMap.
[10:34] So now I can pass the same IntegerStringMap object as an input to the method, which is processMap()
[10:41] one and post that
[10:43] if I try to execute this program, I'll be able to see the output.
[10:47] Now let's imagine inside this processMap1() method
[10:51] I'm trying to make some changes to these IntegerStringMap by invoking the put() method.
[10:57] So to this put() method I can pass a key as four followed by a name which is John.
[11:03] So if I execute this program, obviously you can expect a runtime exception.
[11:08] I'm trying to execute this program.
[11:10] You can see we are getting a UnsupportedOperationException. This way
[11:13] using these two approaches you can always create the immutable Map objects, so feel free to use them
[11:21] based upon your business requirements.
[11:23] I hope this makes sense to you.
[11:24] Thank you and I'll catch you in the next lecture, bye.


########################################
