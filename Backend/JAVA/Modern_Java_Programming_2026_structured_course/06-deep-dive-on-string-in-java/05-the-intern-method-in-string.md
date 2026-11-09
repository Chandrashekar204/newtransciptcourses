# 6.5 — The intern method in String

> Section 6: Deep dive on String in Java

[00:00] Inside this lecture let's try to talk about intern() method that is available inside the String class.
[00:07] What is the purpose of this method?
[00:09] This method you can use whenever you into a situation where you want to move, and String object that
[00:15] is created with the help of new operator into the string pool.
[00:19] For example, like you can see here.
[00:20] First I have created a String object with the very first literal approach String hello = "hello".
[00:27] Inside the second line, I have created another object with the name obj, and this object I'm trying
[00:34] to create with the help of new operator and the constructor.
[00:37] And to this obj
[00:38] also, I'm passing the same content which is
[00:40] hello.
[00:41] If I try to simply create obj just with the new operator and constructor based upon our previous discussion,
[00:48] this obj object is going to be created in a different location inside the heap memory.
[00:53] But if you have a requirement where you want these new object also to be created inside the string pool,
[01:00] then you can invoke the intern() method.
[01:03] So here I am trying to invoke the intern() method based upon the obj object that is created with the help
[01:10] of new operator.
[01:11] When we invoke this intern() method behind the scenes, the JVM will look whether this hello content is
[01:17] already available inside the string pool.
[01:20] If it is available, then this new object is also going to refer to the same memory location.
[01:26] That's why if you try to compare both the hello and obj object, you're going to get the output as true
[01:31] because they are both referring to the same memory location.
[01:36] I also gave another example here.
[01:38] First, I'm trying to create two different variables or object s1 and S2 with two different approaches.
[01:44] Once these two different objects are created, I'm simply trying to compare them with the help of double
[01:51] equal operator (==).
[01:52] And I'm going to get an output, which is false.
[01:55] Later on, I'm invoking the intern() method on top of the s2object, and the output from these s2.intern()
[02:02] intern I'm trying to assign to a new object with the variable name as s3.
[02:07] So if I try to compare s1 and s3, I am going to get an output as true.
[02:13] I hope you are clear.
[02:14] What is the purpose of intern() method?
[02:15] The name also for this method is very apt because like we discussed previously, the process of creating
[02:22] an object inside the string pool, we call it as String interning.
[02:26] So based upon the same String interning name, this method name has been provided, which is intern().
[02:32] As a next step, let's see the demo of this method by creating an example inside the IntelliJ.
[02:39] Here inside my IntelliJ, I'm going to create a new class the class name
[02:44] this time it is going to be internMethodDemo.
[02:49] So this is class name inside these class
[02:52] first I'm going to create the main method because we want to execute the program inside the main() method.
[02:58] First I'm going to create a String with the help of first approach at the literal approach.
[03:03] So here I'm trying to declare a code which is String = " hello ".
[03:08] After this statement I'm going to create another object of String with the help of new operator and
[03:14] constructor.
[03:15] And I'll try to save the same data, which is hello.
[03:18] Let me type String obj = new String().
[03:23] And what is a content that I want to save here?
[03:26] Here.
[03:27] If I simply terminate this statement with the help of semicolon, then this obj object definitely is
[03:33] going to be created in a different memory location compared to these
[03:38] hello.
[03:38] But we don't want that
[03:40] we want this new object also to be created or to be saved inside the string pool itself.
[03:46] So how to invoke the intern() method after the constructor of the String class, you can mention dot operator,
[03:52] and it is going to show you various methods that you can invoke.
[03:56] As soon as you press dot operator, your IntelliJ is going to provide some recommendations.
[04:00] What are the options that you have here?
[04:02] Like we discussed we want to invoke intern() methods.
[04:06] So let me invoke the intern() method.
[04:09] Now if I try to compare these two objects I'm going to get the output as true because they both are
[04:16] referring to the same memory location.
[04:19] So let me try to execute this program.
[04:21] You can see I'm getting the output as true.
[04:23] Let me show you the other example as well which we have discussed.
[04:27] First I'm going to create a String object with the name s1
[04:30] and to this I'm going to assign hello.
[04:33] Later on I'm going to create another object with the name s2.
[04:37] But this time the object I'm going to create with the help of new operator to the constructor of the
[04:44] String, I'm going to pass the same data, which is
[04:46] hello.
[04:47] If I try to compare these two objects, definitely the output is going to be false because as of now
[04:54] they are stored in a two different memory locations.
[04:57] As a next step, I can try to create a
[05:00] new String object with the name s3, and this new object I want to create from the s2 variable or the
[05:08] s2 object that we have created.
[05:10] So first I'll mention s2 object name post that I'm going to mention the dot, and here I'm going to
[05:17] invoke the intern() method.
[05:19] The return type from the intern() method is an String object.
[05:22] You can see here the return type is mentioned on the right hand side.
[05:26] The object from these intern() method I'm going to catch inside this variable s3.
[05:31] So this s3 is going to be created inside the string pool.
[05:36] Whereas this s2 is going to be inside the heap memory.
[05:40] We can combine these two statements with these approach.
[05:43] Like we can directly invoke that .intern() method.
[05:46] And with that the resultant obj object is always going to save inside the string pool.
[05:52] The difference between this approach and this approach is we are trying to avoid the intermediate object
[05:59] or variable, which is s2 with the first approach, whereas inside the second approach we have to create
[06:05] an intermediate object variable, and with that intermediate object variable we are trying to invoke
[06:11] the intern() method.
[06:12] So this is more readable code.
[06:14] Whereas this code is short only expert Java developers, they can understand these short code.
[06:19] Now at the end of this main() method I'm going to create System.out.println().
[06:24] This time I'm going to compare s1 and s3.
[06:27] The output is going to be true, false, true.
[06:31] Let's see the same inside the console.
[06:33] You can see we have true, false and true.
[06:35] I hope you are clear.
[06:36] What is the purpose of intern() method?
[06:38] If you want to read more details about the purpose of this intern() method, you can open this intern()
[06:43] method.
[06:44] This is a instance method or a non-static method which is available inside the String.
[06:50] You can read more details about the purpose of this method by looking at these javadoc comments that
[06:56] you have.
[06:57] Since this method is a non-static method or instance method, we can only invoke this method with the
[07:03] help of object of String.
[07:06] I hope this is clear.
[07:07] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
