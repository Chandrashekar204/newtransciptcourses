# 20.7 — Iterating HashMap using keySet() and entrySet()

> Section 20: Deep dive on Map, HashMap, TreeMap, LinkedHashMap

[00:00] As of now, we know how to create an object of HashMap and how to store entries inside an HashMap,
[00:06] and how to read the values inside HashMap.
[00:09] As a next step, let's try to understand how to iterate the entries that we have stored inside a HashMap.
[00:15] To show you the demo, I'm going to create a new Java class with the name
[00:21] HashMapIterationDemo.
[00:23] Inside this class I'm going to create main() method post that
[00:28] I'm also going to create multiple static methods.
[00:32] Here I'm trying to type first public, followed by static, followed by void followed by approach one.
[00:39] Inside this method, I'm going to explain you about the approach, one that we can follow to iterate
[00:44] the entries inside an HashMap.
[00:47] As of now, you can see my main() method has empty logic.
[00:50] Maybe what I can do is, I can try to copy this logic up to the France and Paris, and the same I can
[00:56] paste here.
[00:57] So now I have my HashMap ready the same
[00:59] I'm going to send as an input to my approach one method.
[01:04] So here I'm going to invoke the approach1() method to the same
[01:07] I'm going to pass the CountryMap as an input and getting a compilation error.
[01:11] I can click on this to resolve this issue.
[01:14] You can see a new method input parameter is added of type HashMap with the key and the value data type
[01:21] as String.
[01:22] So now inside this approach one, I'm going to show you the very first approach that we can follow to
[01:27] iterate the entries of a HashMap.
[01:29] There are multiple approaches, but we're going to discuss most commonly used approaches.
[01:34] Inside this approach we are going to invoke the method which is keySet(). This keySet() method,
[01:41] it is going to return all the keys present inside your HashMap in a form of Set.
[01:47] We're ready to discuss about set, but this should be super easy to understand.
[01:51] On the left hand side, I need to type set and inside the angle brackets I need to mention the what
[01:58] is a key data type, which is String followed by variable name
[02:01] I'm going to mention as keys.
[02:02] Using these keys, I can iterate all the keys with the help of Iterator or for each loop.
[02:10] So first let me show you how to iterate with the help of for each.
[02:14] So I'm going to mention String key as a temporary variable followed by keys.
[02:19] And inside the
[02:20] for each loop I'm going to write a logic, which is to fetch the value based upon a key.
[02:26] What is the variable name of HashMap?
[02:27] It is CountryMap.
[02:29] Using this, I'm going to invoke the get() method and to the same.
[02:33] I'm going to pass the key as an input, and the output I can catch on the left hand side with the variable
[02:40] name as capital.
[02:42] So the same I'll try to print out with the help of System.out.println().
[02:47] Maybe what I'll do is, first I'll try to print out the key, followed by I'm going to have a colon,
[02:54] followed by what is a capital.
[02:57] So if I try to execute this program you'll be able to see all our countries along with their capital
[03:04] cities in the console.
[03:05] This is the code that we can follow to iterate the elements using for each.
[03:10] Whenever we are using the keySet() method, let me show you the other style as well.
[03:15] For the same, I'm going to comment this code for your reference.
[03:18] This time I'm going to fetch the iterator from the keys.
[03:23] So keys is a Set.
[03:25] Using these keys Set object I'm going to invoke the iterator.
[03:29] So let me invoke the iterator on the left hand side.
[03:32] I'll try to create the object variable name with the interface Iterator.
[03:38] And inside this angle brackets I'll just mention the key data type which is String followed by variable
[03:44] name which is iterator.
[03:45] So using these iterator I can build a while loop whenever the iterator has next value.
[03:54] Inside this while loop, I can try to fetch the key first with the help of iterator.hasNext()
[04:00] Uing the same key, I can try to fetch the capital for the same.
[04:05] I can copy these two lines of code and mention here.
[04:08] So you can see I'm trying to fetch the capital value by passing that key to the get() method.
[04:15] And after that, I'm trying to print both the key and the capital.
[04:18] If I try to execute this program, I'm going to get the same kind of output.
[04:22] So this is the approach one where we can use the key Set method to iterate all the keys inside an HashMap,
[04:30] and using the same keys, we are going to fetch the values.
[04:34] Now let me show you the approach to for the same
[04:37] what I'm going to do is, I'll try to copy this entire method inside the same class, but this time I'll
[04:43] try to change this method name to approach to inside the approach two instead of key Set, we are going
[04:49] to invoke the entrySet() we know inside HashMap, each entry is going to be represented with an interface
[04:57] name Entry.
[04:58] So inside this
[05:00] entry we are going to have key and value stored. Am getting a compilation error,
[05:03] to resolve this, I'm going to click on this solution.
[05:07] You can see now my Set data type is changed to Map.Entry().
[05:12] So Entry is an inner interface inside the Map.
[05:14] That's why we need to invoke with the help of Map.Entry and post the entry inside the angle brackets
[05:20] we need to mention String, String.
[05:22] Because key and values are represented by String, String inside the HashMap that we are right
[05:28] now using.
[05:29] Maybe what I can do here is instead of keys, I can use the variable name as entries.
[05:34] Using the same entries, I can invoke the iterator when I'm invoking the iterator using entries on the
[05:41] left hand side, and getting a compilation error.
[05:43] To resolve these, I can change the data type from Iterator String to Iterator Map.Entry String,
[05:51] String.
[05:52] Now using the same iterator, I'm going to invoke the hasNext() method.
[05:56] And whenever we are trying to invoke the next() method, we are going to get an Map.Entry object.
[06:03] That's why on the left hand side, what we have to do is we need to type map dot entry and inside the
[06:10] angle brackets I'm going to mention String, String followed by variable name which is entry.
[06:17] Now using this entry I'm going to get the key and value.
[06:21] How to get the same.
[06:23] It's very easy.
[06:24] You just have to invoke the getKey() method and the output from these get.
[06:29] You can catch on the left hand side with the variable name key.
[06:31] Similarly here I'm going to invoke Entry.get() value.
[06:38] We don't have to pass the corresponding key to get the value, because a Entry object is always going
[06:44] to have a single key and its corresponding value.
[06:47] Now we can try to execute this class and observe the output.
[06:51] But before that, inside the main() method, we need to change this from approach one to approach two.
[06:56] With that, if I execute this program, you will be able to see the same kind of output. If needed,
[07:03] we can also use the for each loop whenever we are using the Entry Set.
[07:07] Let me show you how to do that as well.
[07:09] For the same, let me uncomment this for each loop code.
[07:12] So here instead of keys, I need to use the entries.
[07:16] Whenever I'm using these entries inside my
[07:19] for each, I need to create a temporary variable of type Map.Entry String, String with the
[07:26] variable name as entry.
[07:28] Now using this entry, we can have the same code that we have inside the while loop.
[07:33] So let me copy the same.
[07:35] And with that we are going to get the same kind of output that we have received with the while loop.
[07:40] So let me comment this while loop.
[07:42] Post that I'm going to execute this program.
[07:44] And even with the for each loop we are going to get that similar output.
[07:48] So as of now we discussed two different approaches.
[07:51] Let's try to continue this discussion in the next lecture as well.
[07:55] Thank you,
[07:56] bye.

----------------------------------------
