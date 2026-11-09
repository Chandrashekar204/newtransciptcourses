# 20.10 — Demo of TreeMap in Java

> Section 20: Deep dive on Map, HashMap, TreeMap, LinkedHashMap

[00:00] Let's see the demo of Treemap inside this lecture.
[00:03] Before that, let me open that Treemap interface which is present inside that java.util package.
[00:09] For more details about the Treemap, you can always read the documentation that we have here.
[00:14] It is a red black tree based NavigableMap implementation.
[00:18] The Map is sorted according to the natural ordering of its keys, or by a comparator provided at the
[00:25] map creation time, depending on which constructor is used.
[00:30] This means if you are trying to use the default constructor of the TreeMap, then it is an indication
[00:36] to the TreeMap to always use the natural ordering of the key.
[00:41] For example, if you are trying to use integer as a key inside integer since it is going to implement
[00:48] the Comparable interface this integer class, it is going to have the comparison logic by overriding
[00:55] the compareTo() method.
[00:57] So based upon these
[00:58] compareTo() logic, the default sorting of that TreeMap elements is going to happen.
[01:03] Otherwise, you can define your own comparator.
[01:06] Whenever you are trying to define your own comparator, you need to provide the comparator information
[01:11] to the TreeMap during the object creation.
[01:13] If you try to look for the constructors present inside the TreeMap, there is a constructor that is
[01:20] going to accept the comparator as an input.
[01:22] So the object of your comparator you can pass to this TreeMap constructor.
[01:27] While you are trying to create the object of the TreeMap.
[01:30] If you are trying to provide the Comparator object to the constructor of the TreeMap, then the sorting
[01:35] is always going to happen based upon your comparator logic, but not based upon the default Comparable
[01:41] logic.
[01:42] I hope this makes sense.
[01:43] Now let's try to see that demo of TreeMap by creating a new Java class with the name TreeMapDemo.
[01:52] Inside this class, as usual, we need to create the main() method post search
[01:57] I'm going to create a object of TreeMap by mentioning Map, Integer, String and the left hand
[02:05] side.
[02:06] I'm going to give a name to this object, which is numbers.
[02:09] Now coming to the right hand side, I'm going to invoke the default constructor of TreeMap with the
[02:15] diamond operator.
[02:16] After this I'm going to write numbers.put() and to this put() I'm going to pass key as 23, followed
[02:25] by the value which is 23.
[02:29] Post that I'm going to repeat this line of code this time instead of 23, I'm going to mention 12, followed
[02:36] by spelling 12.
[02:39] After 12, I'm going to insert the 42 integer against to this 42, I'm going to mention the spelling
[02:47] as 42.
[02:49] After the 42, I'm going to insert the integer key, which three along with its spelling.
[02:55] After three it is going to be 19.
[02:58] Let me mention the spelling as well
[03:01] after the 19 key, the spelling is 19, followed by I'm going to insert 48 with its spelling as 48,
[03:13] followed by 76 with its spelling, which is 76.
[03:19] So you can see we randomly inserted all these keys and its values, but by the time we tried to iterate
[03:25] the entries inside the TreeMap, we are going to get the output in an sorted order.
[03:30] So what I'm going to do is, I can write a for each loop using this
[03:35] for each loop, I'm going to iterate all the entries inside these numbers TreeMap object.
[03:40] So I'm going to invoke numbers.EntrySet.
[03:44] And on the left hand side I'll just mention Map.Entry.
[03:48] And inside this angle brackets I can mention Integer, String, and the variable name I'll mention
[03:54] as entry.
[03:55] So now what I'm going to do is with the help of System.out.println(), I'm going to first try
[04:01] to print the key details with the help of getKey() method, followed by inside the String I'll just have
[04:09] hyphen, and after the String, I'll try to append the value details corresponding to a particular key.
[04:16] With the help of this getValue() method, I should be able to get the value details.
[04:20] So now if I try to execute this program, you'll be able to see the output in an sorted order.
[04:27] So all your keys
[04:28] they are sorted based upon the natural ascending order like 3, 12 19, 23, 42, 48 and 76.
[04:37] I hope this discussion makes sense to you whenever you are looking to iterate your Map entries in an
[04:44] sorted order, then always go for the TreeMap instead of HashMap.
[04:48] If you don't have any sorted requirements inside your business logic, you can happily go with the HashMap
[04:53] implementation.
[04:55] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
