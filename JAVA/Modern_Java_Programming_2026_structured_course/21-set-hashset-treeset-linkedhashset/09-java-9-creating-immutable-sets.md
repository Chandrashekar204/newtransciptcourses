# 21.9 — [JAVA 9] Creating Immutable Sets

> Section 21: Set, HashSet, TreeSet, LinkedHashSet

[00:00] Inside this lecture, let's try to understand how to create immutable sets.
[00:05] In the previous sections, we also discussed very similar topic to to create immutable List objects
[00:11] and immutable Map objects in the similar lines.
[00:14] Set interface also provide static factory methods with the name of().
[00:19] There are multiple overloaded of() methods which you can use to create immutable Set objects, but these
[00:27] are for static factory method.
[00:29] It is only introduced from Java 9.
[00:32] Before Java 9
[00:33] developers
[00:34] they first used to create the Set object post that they used to provide these Set object as an input
[00:41] to the UnmodifiableSet() method available inside the collections class.
[00:46] So this is a static method.
[00:48] So when we provide a Set object to this method, it is going to convert that object as an immutable
[00:55] or unmodifiable object.
[00:57] Let's see the demo of these methods very quickly inside our intelligJ
[01:01] I'm going to create a new Java class with the name ImmutableSetDemo.
[01:08] Inside this class we are going to create main() method followed by
[01:13] I'm going to create a Set object with the data type as String and the variable name I'll set as String
[01:21] set to this object on the right hand side I'm
[01:24] first I'm going to invoke the default constructor of HashSet.
[01:28] To this default constructor of HashSet.
[01:30] I can pass a List which I built with the help of aslist() method available inside arrays.
[01:36] So to this asList() method, I'm passing multiple elements like a, b followed by C.
[01:43] With this line of code, I'm able to successfully create an Set object, but this is not going to be
[01:49] an unmodifiable or immutable object.
[01:53] Anyone should be able to add new elements to this Set object.
[01:57] I can also show you that demo around this. For the same,
[01:59] I'm going to build a method which is public static void processSet().
[02:05] To this method, we can pass the Set object as an input, which is capable of storing String data type
[02:12] elements.
[02:13] So let me accept the same as an input and post that
[02:16] inside this I'm going to build a for each loop with the temporary variable name as String element,
[02:23] followed by stringSet.
[02:25] Now inside this for each block, I can try to print out my elements by converting them into uppercase.
[02:32] For the same, I just have to invoke the element.toUpperCase() method.
[02:36] We can try to test this method by invoking from the main() method and passing the input variable, which
[02:44] is StringSet.
[02:45] If I execute this method, you will be able to see all my elements a, B, c in completely capital letters.
[02:51] So this method
[02:52] it is not trying to modify my Set objects, but with the current Set object we will not be able to control
[02:59] this method, making any modifications to our Set object.
[03:03] I can also show you a demo here.
[03:04] What I can do is with the help of StringSet, I can invoke the add() method and I can pass D as an element.
[03:12] If I execute this class, you will be able to see I'm able to successfully add an element. To handle
[03:18] these kind of scenarios, where you don't want other methods to be able to modify your Set objects.
[03:25] There are two approaches.
[03:26] The very first approach is we can use the collections class, and inside this class there is a static
[03:32] method with the name unmodifiableSet(). To the same
[03:36] we can pass this stringSet as an input and the output
[03:40] also we can catch with the same variable name.
[03:43] Now what I can do is I can try to bring these method invocation logic to the next line.
[03:49] With this we are going to get a runtime exception which is UnsupportedOperationException.
[03:55] So this is the legacy approach that you can use before Java 9.
[03:59] And you can see this approach has two steps involved.
[04:02] One is creating the Set object followed by converting that Set object into an UnmodifiableSet.
[04:08] But like we discussed from Java 9, there is a better approach, which is with the help of of static
[04:15] factory methods.
[04:16] Let me try to show you that approach as well.
[04:18] For the same, I'm going to create another Set object which can store string elements.
[04:24] This time I'm going to mention the name as StringSet1 and on the right hand side, with the help
[04:30] of Set interface, I'm going to invoke the static method, which is of(). To the same
[04:35] I can pass all these elements, this stringSet1 object
[04:39] it is going to be created as a unmodifiable or immutable object.
[04:45] I can confirm the same by copying these line of code and pasting here.
[04:50] Here in the place of stringSet1, I'm going to pass stringSet1 and let me remove all these gaps.
[04:58] This time
[04:58] also if I try to execute this
[04:59] class, I'm going to get the UnsupportedOperationException because this method is trying to be over
[05:06] smart and it is trying to modify my Set object.
[05:09] So that's why we are getting these RuntimeException.
[05:12] But if I comment this line of code, you're not going to get any exception.
[05:17] We are going to get the proper output.
[05:19] I hope this makes sense to you.
[05:21] And you are clear on how to create the immutable or unmodifiable Set objects.
[05:27] If you are using Java 9 version, always prefer these are for static factory method to create the
[05:33] immutable Set objects.
[05:35] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
