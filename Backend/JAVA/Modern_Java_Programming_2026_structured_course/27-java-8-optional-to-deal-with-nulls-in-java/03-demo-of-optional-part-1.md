# 27.3 — Demo of Optional - Part 1

> Section 27: [JAVA 8] Optional to deal with nulls in Java

[00:00] Inside this lecture, let me show you how to leverage the optional class to handle the
[00:06] NullPointerExceptions gracefully.
[00:08] Since we are into the new section, I have created a new project with the name section_27.
[00:14] Inside this project, I'm going to create a package with the name com.eazybytes.optional.
[00:22] Inside this package
[00:23] let me create a new Java class with the name OptionalDemo.
[00:28] Now inside this OptionalDemo class I'm going to create a main() method followed by
[00:33] I'm also going to create a static method with the name public static and the return type as String,
[00:41] followed by sayHello() as the method name.
[00:44] So this method is going to simply return an String object.
[00:49] For example, from this method I can simply return a String object with the value hello world!
[00:56] So if anyone try to invoke this method from some other methods, they're always going to get an String
[01:03] as an output.
[01:05] So that's why I'm trying to catch with the variable name as message, the same variable I'll try to
[01:11] print out onto the console by invoking message.ToUppercase().
[01:17] So I'm trying to convert all the String content into the uppercase before I'm trying to print out onto
[01:23] the console.
[01:24] So if I execute this program, everyone is happy I'm going to get the proper output, which is hello
[01:30] world.
[01:30] So if you see in this scenario, my method is always going to give me a proper String object.
[01:36] There is no single scenario where I may return a null as an output from this method.
[01:42] So that's why there is no chance for me in getting a NullPointerException in these two lines of code.
[01:48] But now think like I'm going to change the logic inside the sayHello() method, where it is going to
[01:54] return a proper String object
[01:56] in some scenarios and in some other scenarios, it is going to return a null object to build a business
[02:02] logic that is going to behave randomly.
[02:05] What I'm going to do is first I'm going to generate a random integer with the help of Random class object.
[02:12] So that's why I'm trying to create the object of Random here.
[02:16] And using the same object, I'm trying to invoke the nextInt() method.
[02:20] So this method is going to give me some random integer value as an output, which I'm trying to catch
[02:26] on the left hand side with the variable name num.
[02:29] So I can also try to print out what is a num that Random class has generated.
[02:34] Now using these num
[02:35] whenever this is an even number, I want to send a proper String object as an output, which is hello
[02:42] world.
[02:42] Whereas if my number is an odd number, then I'm going to return a null object.
[02:47] So let me show you how to build that.
[02:48] So I'm going to build a if condition.
[02:51] And inside this if condition I'm going to check if my num is going to be exactly divisible by zero.
[02:59] If it is yes, then that indicates this is an even number.
[03:03] So in such scenarios I'm going to return a proper String object.
[03:07] Otherwise I'm always going to return the null object as an output.
[03:12] So I'm trying to return null itself.
[03:14] I hope you are clear about this logic.
[03:16] Now, the problem with this method is sometimes in the scenarios of even number, which is like a positive
[03:21] scenario, it is going to return a proper String object.
[03:24] Otherwise, in the negative scenario where an odd number is generated, it is going to return a null
[03:29] object.
[03:29] People who are trying to use these, they don't know that this method may potentially throw a null object.
[03:36] So without knowing that they'll try to use this method in their business logic.
[03:41] Like you can see here in the scenarios where this method is returning a null object using the null,
[03:46] they are going to invoke the toUppercase() method.
[03:49] With that they're going to get a famous NullPointerException.
[03:52] So let's try to execute this class so that we can see the surprise.
[03:56] So here you can see this is the number that got generated.
[03:59] And we are so lucky
[04:00] the first number that got generated itself is a odd number.
[04:04] And that's why we are getting the NullPointerException.
[04:06] Let me try to execute one more time.
[04:08] This time you can see the even number is generated.
[04:10] And that's why we are getting a proper output before Java age.
[04:14] What developers they used to do is they will check if this given message is a null or not.
[04:19] So they'll write a if condition
[04:21] he has to check if message is not equal to null, then only execute the System.out.println().
[04:31] Otherwise they will not execute the System.out.println().
[04:34] And with that the NullPointerException is handled.
[04:37] You can see here the number is generated is an odd number.
[04:40] But still we are not getting any output and we are also not getting any NullPointerException.
[04:45] So if you see this is a very painful process.
[04:47] This is just a simple program.
[04:49] And even in this small program also we are handling the NullPointerException with a ugly if block.
[04:55] And here I need to check only once because message is only a String object.
[04:59] But
[04:59] in real projects, you will get a object as an output, which is going to have so many embedded objects
[05:06] inside it, and you need to check each and every object if it is not null
[05:10] by writing lot many ugly if conditions.
[05:13] That's why to make our developer life easy optional is introduced inside Java 8.
[05:20] Let's try to update the same program in the next lecture by leveraging the optional and in the same
[05:26] process, I'm going to teach you about the advantages that we get whenever we use the optional.
[05:32] I hope you are with me so far.
[05:33] Thank you
[05:34] and I'll catch you in the next lecture, bye.

----------------------------------------
