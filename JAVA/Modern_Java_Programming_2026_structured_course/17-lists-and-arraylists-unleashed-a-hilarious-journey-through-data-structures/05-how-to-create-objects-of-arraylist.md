# 17.5 — How to create objects of ArrayList

> Section 17: Lists and ArrayLists Unleashed – A Hilarious Journey through Data Structures

[00:00] Okay
[00:01] we are going to discuss about ArrayList before we try to explore about ArrayLists.
[00:06] First, let me show you a couple of memes around ArrayList.
[00:09] These are very first meme like
[00:11] you can see ArrayList is a more advanced version are a cool version of arrays.
[00:17] We know arrays has a limitation, which is they support only a static size.
[00:21] Whatever you declare during the initialization, you have to live with the same size.
[00:26] If you want to change the size, you need to rework on recreating another Array object and shifting
[00:32] all your elements, or copying all your elements from old array to new array.
[00:37] So that's a very long story, and it has lot of disadvantages.
[00:41] That's why we are looking for the more cooler option which is ArrayList.
[00:45] ArrayList supports dynamic resizing at runtime based upon the elements that you are trying to add or
[00:53] remove.
[00:53] Accordingly, it is going to adjust the size by itself.
[00:56] That's why we can call ArrayList as a cooler version of arrays.
[01:00] So this is one more meme that I like around ArrayList.
[01:03] You can see ArrayList is a combination of Array and List the ArrayList class.
[01:09] It is going to work very similar to array and at the same time this ArrayList.
[01:13] It is also going to inherit or override all the methods available under this Collection,
[01:20] SeqencedCollection and a List interface.
[01:22] So with ArrayList you are getting the benefits from two different worlds.
[01:27] One is Array and the other one is List.
[01:29] This is the last meme that I want to show.
[01:31] Once you learn about the ArrayList, definitely ArrayList is going to become your best friend and
[01:37] you're going to end your friendship with array.
[01:40] But I would say don't completely end your friendship with array.
[01:43] Don't treat array as an enemy.
[01:45] There might be some scenarios where you may want to use array.
[01:49] For example, using arrays we can store the primitive data types like int, long, float, double without
[01:56] any autoboxing or wrapper classes help.
[01:59] That's why always go with the arrays.
[02:02] If you're looking for a static size, and if you want to store the primitive data elements, then in
[02:07] all such scenarios, arrays is the go to option.
[02:10] Whereas for dynamic size adjustments at runtime you can always go with the ArrayList.
[02:15] Now I came to the IntelliJ and here I'm going to open the class which is ArrayList.
[02:23] So you can see this is also present inside the java.util package.
[02:26] And it is extending AbstractList and implementing the List interface.
[02:32] Apart from this List interface, it also implements many other interfaces.
[02:36] As a next step, let's see the demo of these ArrayList class for the same
[02:40] you can see I have created a new project with the name section_17.
[02:44] Inside this first I'm going to create a new package which is com.eazybytes.List.
[02:53] Inside this package I'm going to discuss List related examples.
[02:57] Since ArrayList is an implementation of List, we can try to create a class inside the same package
[03:04] with the name ArrayListDemo.
[03:07] Inside this class
[03:08] first I'm going to create the main() method and inside this main() method.
[03:12] First let me create an object of ArrayList.
[03:15] Whenever you're trying to create the ArrayList object, you can see ArrayList class
[03:20] it is going to expect,
[03:22] what is the type of the data that you are trying to store.
[03:26] You can see inside the class definition.
[03:28] Inside the angle brackets we have an value E.
[03:31] E indicates the type of elements that we are trying to store inside this ArrayList object.
[03:36] So whatever e value that you are seeing inside the angle brackets, we call this concept as generics
[03:42] inside Java.
[03:44] Using generics, we can store some generic code.
[03:47] We're going to discuss in detail about generics in the coming sections.
[03:50] For now, please note that whenever we are trying to create an object of ArrayList, object or any
[03:56] other Collection object, we need to let the compiler know what kind of objects we are trying to store
[04:03] into these ArrayList.
[04:04] So here I'm going to mention the object type as Integer, followed by I'm going to give the name as
[04:12] nums and at last on the right hand
[04:15] also we need to mention new ArrayList.
[04:17] And inside the angular brackets I'm going to mention Integer.
[04:21] So whatever data type that you are trying to mention on the left hand side, the same you need to mention
[04:26] and the right hand side as well.
[04:27] If you try to mention some other data type, you can see you're going to get a compilation error.
[04:33] So let me revert to Integer.
[04:35] Here you may have a naughty thought, which is can I mention the primitive data type as an type to the
[04:41] ArrayList object.
[04:42] So let's try to do the same here instead of Integer
[04:45] I'm going to mention the primitive data type of int which is int.
[04:49] And you can see I'm going to get a compilation error because we know using collections inside Java we
[04:55] will be able to store only the objects but not the primitive
[04:59] data type values.
[05:00] That's why we are getting a compilation error saying that type argument cannot be of primitive type.
[05:06] So let me revert to Integer.
[05:08] There is another flavor that we can follow while we are trying to create the ArrayList object.
[05:14] This time I'll try to create an ArrayList object which is capable of storing
[05:18] the String elements or String objects for the same, this time on the left hand side.
[05:23] I am going to use the List interface and to this List interface I'm going to pass the data type as String.
[05:29] Inside this angle brackets.
[05:30] The variable name I'm going to mention is country names, because inside this List object I'm going
[05:37] to store the various country names.
[05:39] Now on the right hand side we should not use the List.
[05:42] Because List is an interface, we will not be able to create the object of List interface.
[05:48] That's why instead of List, we need to mention the one of the implementation of List interface.
[05:54] And here, since we are looking to create an ArrayList object, we need to mention ArrayList.
[06:00] And inside the angle brackets we need to mention String as an data type.
[06:06] So these are one flavor.
[06:07] Similarly, I can create one more List object with the name as characters.
[06:13] And inside this I'm going to store various char values.
[06:17] So that's why I need to mention the wrapper class of char, which is Character here.
[06:22] And if needed, we can also store the objects of our custom data types like Person, Employee.
[06:27] So here instead of character we just have to mention Person.
[06:31] So as of now I'm getting an error because I don't have a Person class inside my project.
[06:36] In the coming lectures, I'll show you how to store the custom data type objects inside List objects.
[06:42] For now, let me revert back to character.
[06:44] There is one more flavor of creating the object of ArrayList, which is majority of the developers
[06:50] using these days.
[06:51] This flavor involves var keyword that we discussed previously.
[06:55] So on the left hand side you can simply mention var after var I'm trying to give the variable name like
[07:03] double nums because to this double nums, I'm going to store a ArrayList object which is capable
[07:09] of storing double numbers.
[07:11] Now on the right hand side I need to mention new ArrayList, and inside these angle brackets I need
[07:17] to mention double.
[07:18] So this is majorly being used these days by the developers because it's very obvious, right?
[07:24] You just have to write very less code.
[07:26] You don't have to repeat the code on the left hand side just before the variable name.
[07:30] You just have to mention the var before your variable name and the compiler
[07:34] it is going to infer the data type of this variable based upon what you have mentioned on the right
[07:40] hand side.
[07:40] I hope you are clear about how to create an ArrayList object.
[07:45] What are the different options that we have?
[07:47] Please make sure after the angle brackets you need to mention these parentheses.
[07:51] This indicates the constructor that you are trying to invoke.
[07:55] If you try to open this, you will be able to go to the constructor present inside the ArrayList.
[08:00] So that's why always after the angle brackets, please make sure we have these parentheses.
[08:05] Also, if we don't have these you can see we are going to get a compilation error.
[08:09] As a next step, let's try to populate some elements or objects into these ArrayList object.
[08:16] Thank you
[08:16] and I'll catch you in the next lecture, bye.

----------------------------------------
