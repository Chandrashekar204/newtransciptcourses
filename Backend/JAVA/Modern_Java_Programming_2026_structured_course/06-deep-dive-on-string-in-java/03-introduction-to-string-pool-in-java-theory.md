# 6.3 — Introduction to String Pool in Java - Theory

> Section 6: Deep dive on String in Java

[00:00] In the previous lecture,
[00:01] I told you that String is a special data type compared to other primitive data types that we have in
[00:08] Java.
[00:08] Because string has its own charm and capabilities.
[00:12] Throughout this section, you're going to see and understand the charm of String.
[00:16] And by the end of this section, you're going to agree with me that String is something different compared
[00:22] to other primitive data types.
[00:24] I also told you that we can save data with the help of String data type by using two different approaches.
[00:31] The very first approach is by simply creating the literal or variable, by following the same syntax
[00:36] of primitive data type.
[00:38] The other approach is we can try to create an object of String class with the help of new operator and
[00:44] the constructor.
[00:45] But here you may have many questions,
[00:47] what is the difference between these two approaches and when to use which approach?
[00:52] That's why inside this lecture, let's try to understand the difference between these two approaches.
[00:57] Inside the very first approach, we can simply store the data inside the String variable by following
[01:04] the same syntax of primitive data types.
[01:06] Here I'm trying to assign a value hello to the variable str.
[01:12] So the declaration and the initialization is very simple here.
[01:15] So whenever I'm using these kind of syntax to store the data with the help of String data type behind
[01:23] the scenes, Java is going to create an object of the String.
[01:27] Don't assume that since we are using primitive data type syntax to store data here, the str variable
[01:34] is not going to be an object regardless of which approach you're going to use.
[01:39] Always remember inside Java, the data that we store with the help of String data type is going to store
[01:45] as an object.
[01:46] But when we use these primitive data type syntax approach, there is a concept called String pool
[01:52] come into picture. Whenever you are trying to store data with the help of this first approach.
[01:57] First, my Java JVM will check if there is any memory location where we have stored the same String
[02:04] data.
[02:04] If there is such memory location, then my JVM is not going to create a new object of String.
[02:10] Instead, the new variable that I'm trying to create to store the same data will be pointed to the memory
[02:17] location where we previously stored the same data
[02:20] inside the String pool.
[02:22] We'll come to the point why Java is using String pool in this scenario.
[02:26] But please note that whenever we are trying to store data with this first approach, which is the literal
[02:31] approach or variable approach behind the scenes
[02:34] every time my JVM is going to check if the String pool already has given String data stored.
[02:42] If yes, then it is not going to create new memory location.
[02:45] Instead, the new variable that I have created will be pointed to the memory location where we already
[02:51] stored the given String data.
[02:53] If there is no matching data inside your String pool, always the JVM is going to create some memory
[02:59] location inside the String pool and store these new data that you are trying to assign.
[03:05] I'll show you all this visually in few minutes so that it will be more clear for you.
[03:09] But before I try to do that, let me talk about the second approach.
[03:13] Inside the second approach, we are going to create the object of the String with the help of new operator
[03:19] and the constructor.
[03:20] Whenever I'm using this approach, regardless of if I'm trying to store the duplicate data using multiple
[03:27] objects, always my JVM is going to create a new object inside the " heap memory ".
[03:33] So there is no optimization in this scenario because even though you are trying to store duplicate data
[03:40] with the multiple objects, JVM simply is going to create different, different memory locations inside
[03:46] the heap
[03:47] memory.
[03:47] There is no concept of String pool in this approach.
[03:51] I'm assuming now you have at least some basic idea around these two approaches.
[03:55] Let me try to show more details about these approaches visually so that it can be clear for you.
[04:01] First, assume you have heap memory.
[04:03] So these are brand new heap memory.
[04:05] We know inside Java any object that we try to create will be stored inside this heap memory.
[04:11] First assume I'm trying to create some String variables, and I'm trying to store some data with the
[04:17] help of first approach.
[04:19] So here you can see I have created three variables.
[04:22] hello,
[04:23] hi,
[04:23] hey.
[04:24] If you closely observe inside the hello and hi variables, I'm trying to store the same data which is
[04:31] hello.
[04:31] So whenever we are trying to use this first approach where my String objects are going to store, they're
[04:36] going to store inside a special memory called String pool.
[04:40] And this String pool is a part of heap memory itself.
[04:44] Let's see how these variables and data is going to be stored inside the String pool.
[04:49] Like you can see here, there is a String pool inside the String pool
[04:53] there are multiple memory locations.
[04:55] At the first memory location, my JVM stored the String data
[04:59] which is hello.
[05:00] This memory location will be created during the first line of statement when we try to execute the second
[05:06] line of statement.
[05:07] Since my JVM is going to recognize the same hello, data is already present inside the string pool,
[05:13] it is not going to create a new memory location inside the String pool.
[05:17] Instead, it will simply make hi variable to point to the same memory location which is created for
[05:23] the hello variable.
[05:25] Whereas when we try to execute the third statement which is String hey = hey.
[05:30] Since there is no such data already available inside the string pool, a new memory location will be
[05:36] created and the same will be pointed to the hey variable.
[05:39] We can also confirm if both hello and hi variable
[05:43] they are pointing to the same memory location or not.
[05:46] How can we confirm that by using the double is equal to operator (==).
[05:50] Here you can see I have a System.out.println() statement.
[05:54] Inside the println() method I have provided a expression where I'm trying to compare two objects like
[06:01] hello is an object, hi is an object.
[06:03] So I'm trying to compare these two objects with the help of double equal operator.
[06:08] Whenever we try to use this operator behind the scenes, my JVM is going to compare the hash code or
[06:15] the memory location of these two objects.
[06:18] We know all the objects inside Java
[06:20] they are going to be stored inside a memory location inside heap.
[06:24] Since my hello and hi objects are variables, they are pointing to the same memory location.
[06:30] I'm going to get true as an output from this System.out.println().
[06:35] Now let's try to understand how the story is going to be with the second approach.
[06:39] Here you can see I'm trying to create multiple objects.
[06:42] Totally
[06:43] I have created three objects obj, obj1, obj2 and inside the three objects I'm trying to store
[06:50] various kinds of data like hello and hi.
[06:53] If you see here my first object which is obj and second object obj1.
[06:58] They both are storing the same data which is hello.
[07:02] But whenever we try to create an object of String with the help of new operator, there is no concept
[07:07] of string pool.
[07:08] My JVM is going to blindly create multiple objects with different memory locations without worrying
[07:16] about the optimization.
[07:18] Because we are telling to the JVM or Java, please create the objects.
[07:22] Don't bother about the string pool.
[07:24] I don't want any optimizations or performance improvements.
[07:28] That's why you can see inside my heap memory
[07:30] there are multiple memory locations are going to be created, and these memory locations are going to
[07:36] be referred with the variable names or the object names like obj or obj1 or obj2.
[07:43] Now in this scenario, if you try to run the same System.out.println() by trying to compare
[07:48] obj and obj1 with the help of double equal to operator, you are going to get false as an output,
[07:57] because both these two objects are stored at the two different memory locations.
[08:02] I'm also going to show you a small demo by using a Java program in the next lecture.
[08:07] But before I try to close this lecture, I want to share an very important point, which is whenever
[08:13] you are dealing with the string pool, we cannot directly access the string pool, and there is no option
[08:20] or mechanism inside Java where we can alter or remove the String objects that are stored inside the
[08:27] string pool.
[08:27] Whenever you want to destroy your string pool, the only option is to stop or restart your Java application.
[08:35] I hope you are clear with these two approaches.
[08:37] Please refer to these slides if you have any questions.
[08:40] Whenever you are trying to create the objects of String with the help of first approach, we can call
[08:45] that process as String interning.
[08:48] You can see I also mentioned this important point here.
[08:51] So inside interviews people can ask you what is String interning.
[08:55] So String interning is a process where you can create the objects of String by simply using literals
[09:01] and string pool concept.
[09:03] There will be no new operator or constructor involved in the String interning process.
[09:09] And here when I'm trying to explain about these two approaches, you might have a question which is
[09:14] when to use which approach.
[09:16] Let me try to answer this question very quickly.
[09:19] It is always recommended to use the literal style, or the first approach that we have discussed, to
[09:26] declare the objects of String instead of using new operator.
[09:30] Do you know why?
[09:31] Let's try to understand the same.
[09:33] The very first reason is using the string pool,
[09:36] the Java is going to save a lot of memory in real applications or real projects developers
[09:42] they are going to create lot many objects of String, and in that process they may end up storing duplicate
[09:49] data to handle these kind of scenarios and to provide some optimization, Java is going to use the string
[09:56] pool concept behind the scenes.
[09:57] And this optimization of the
[09:59] memory is going to be possible only if we use the literal style or the first approach that we have discussed.
[10:06] By following the literal style approach, we can save our JVM from creating unnecessary String objects
[10:13] and thus reducing memory usage for our Java application.
[10:18] There is also another reason why we should always use String pool approach.
[10:22] The reason is strings are immutable in nature.
[10:26] Immutable means something we cannot change once it is created.
[10:30] This is one of the important character of String.
[10:33] We are going to talk in detail about why string is made as immutable inside Java.
[10:38] All the details about immutability of String we are going to discuss in the coming lectures.
[10:43] Apart from saving memory for our Java application, we can also get one more advantage whenever we follow
[10:51] the string pool approach.
[10:53] The advantage is we can improve the performance of our application.
[10:57] Since this String interning allows the JVM to reuse the existing String objects indirectly, we are
[11:05] going to reduce that time and resources needed to create the new String objects, and this will result
[11:12] in faster code execution and improved overall performance of our application.
[11:17] On a high level, we should always use the String pool approach to save some memory and improve the
[11:23] performance by reusing the existing String objects wherever possible.
[11:28] So that's why my humble request is always try to create the strings with the help of string pool approach
[11:35] or literal style.
[11:36] Never try to use a new operator.
[11:38] Off course, there might be some business scenarios where you want to create brand new objects.
[11:43] In such scenarios
[11:44] definitely you can go with the new operator approach, but most of the times, please, please follow
[11:49] the literal style approach.
[11:51] Let's see the demo of these two approaches in the next lecture with the help of a Java example.
[11:57] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
