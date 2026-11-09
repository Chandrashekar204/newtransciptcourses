# 6.6 — The concat method in String

> Section 6: Deep dive on String in Java

[00:00] In this lecture, I'm going to show you a demo of concat method available inside the String.
[00:06] By the same, let me create a new Java class, and the Java class name is going to be ConcatMethodDemo
[00:14] .
[00:15] I'm assuming you're also creating these classes along with me.
[00:19] My humble request is please create the Java classes, and please try to create the methods and the Java
[00:25] code that I'm trying to explain inside the course.
[00:27] This way, when you try to create the Java code with your own hands and try to run inside your local
[00:33] system, you're going to understand Java in a better manner.
[00:37] And sometimes if you face any issues, you can try to fix them.
[00:41] And from the mistakes, you can learn more about Java.
[00:44] Now we have this empty class as usual
[00:47] first we need to create the main() method.
[00:49] Inside this main() method
[00:50] first, I'm going to create an object of String with the name hello.
[00:54] And using this hello object, I'm going to store the data which is hello itself.
[01:00] Now this is simple Java statement where we are trying to store the String data with the help of this
[01:06] hello object.
[01:07] Think like maybe inside my business logic.
[01:10] After few lines of code, I want to add more data to my String.
[01:14] Maybe I want to change the value from Hello to Hello world.
[01:18] In such scenarios, there are two ways to append the new content are to concat new content to the existing
[01:26] String object.
[01:27] Let's try to understand how to achieve the same.
[01:29] So in the next line, I'm going to append the new content to the hello object content with the help
[01:37] of plus operator.
[01:38] And after the plus operator.
[01:40] I'm going to mention what is the new content that I want to add?
[01:44] The new content that I want to add is world.
[01:46] With this, I'm trying to add the new content to the existing hello content, but this is not a complete
[01:53] Java statement.
[01:54] That's why I'm getting an error.
[01:56] To make this as a complete Java statement, I need to assign these new output value to one of the String
[02:02] object.
[02:03] I can create a new String object, or I can try to simply assign to the same String object, which is.
[02:09] hello, I hope you're not getting confused here.
[02:11] First, we are trying to append the new content to the existing hello object, the whole new content
[02:19] we are trying to assign back to the same object reference name, which is
[02:24] hello.
[02:24] Previously I was telling you that String is immutable.
[02:28] That means once we have created an object of String, we cannot change the content of the String object.
[02:33] But here I'm able to change it
[02:35] does that mean whatever I said previously is wrong?
[02:38] No
[02:38] whatever I said is correct here with this statement, we are only having the illusion that we can manipulate
[02:45] the string content behind the scenes
[02:47] there is a lot of work is going to happen to make the String as immutable.
[02:51] I'm going to talk about immutability of String objects in the coming lectures
[02:55] for now, please don't worry about these immutability concepts. As a next step
[03:00] what I'm going to do here is I'm going to print the content of the hello object by just passing hello
[03:07] object to variable to the println() method.
[03:09] If I try to execute this program, I'll get an output which is HelloWorld!
[03:14] You can see there is no space between Hello and World because we have not provided the space anywhere.
[03:20] So to provide the space, there are two options.
[03:23] I can change this World to space World.
[03:26] And with that you'll be able to see a space in the output, which is Hello World.
[03:31] The other option that we can follow is, we can append one more string between Hello and World.
[03:37] And this new String object can hold an a space value.
[03:41] So let me show you how to achieve that.
[03:43] So here I'm going to append the new String content which is space.
[03:48] And after mentioning the space String value I'm going to mention +
[03:52] with this you can see for the hello content
[03:56] first I'm trying to add space post that I'm going to add world.
[04:00] This way we can try to append any amount of data with the help of this + operator.
[04:07] So now if I try to execute this program you will be able to see the space here.
[04:12] Plus is the only Arithmetic operator symbol we can use inside String object.
[04:18] Apart from plus we cannot use any other Arithmetic operator symbols like minus, division, multiplication.
[04:26] So such symbols we cannot use inside any of the Java objects, including the String objects.
[04:33] Only String objects has a flexibility to use this plus Arithmetic operator to append the new content,
[04:40] or to concatenate new content.
[04:42] Apart from using this plus symbol, we can also append the new content to the existing String with the
[04:49] help of a method called concat().
[04:51] Let me show you that approach as well.
[04:53] Here I'm going to copy all the existing code and paste at the end of the method.
[04:58] Since the object names are same, we are
[05:00] getting a compilation error.
[05:01] Let me change this hello object name to hello1 and let me change in all the remaining places.
[05:07] And with that we have two different objects.
[05:10] One is hello and hello1. For the second object I want to use the concat() method.
[05:16] So what is a process
[05:17] to use a concat() method after the object, which is
[05:20] hello1
[05:21] I can mention dot operator followed by concat(), to this concat() method
[05:26] you can see we can pass and String value and the output from these concat() method is also going to be
[05:32] a String object.
[05:33] So let me invoke this concat() method.
[05:36] And to this concat() method I'm going to pass space
[05:40] and with this I'm just trying to append the space character to my Hello content.
[05:45] And the new content is assigned to the same object, which is hello1.
[05:49] If I want to add more new content, it's very simple.
[05:53] I need to mention dot operator and invoke the concat() method one more time.
[05:58] This time I can pass the content which is world with this
[06:02] now our String object is going to hold Hello Space world!
[06:07] I can also try to run this command and show you the output.
[06:11] You can see we have two outputs and both of them they are looking same.
[06:15] So these are the two approaches that we can use to append the new content to the String.
[06:21] So this process we can call it as append or concat. Like you can expect
[06:26] this concat() method is also an instance method or a non-static method.
[06:31] That's why we are invoking it with the help of String object.
[06:35] So here
[06:36] hello1
[06:36] is a String object and on top of this object I'm invoking the concat() method.
[06:42] So if I take this hello1.concat() method.
[06:45] This highlighted expression is going to give me an String object as an output.
[06:51] That's why on top of this new object that is going to be formed behind the scenes, I'm able to invoke
[06:57] concat() method one more time.
[06:59] This confirms as long as you have a String object in your hands, you can always invoke concat() method
[07:06] any number of times.
[07:07] You can read more details about the purpose of concat() method by going to the String class.
[07:13] So there are good amount of details about what this concat() method is going to do, so please read the
[07:18] same if you are looking for more information around this method.
[07:22] Before I try to close this lecture, I want to share one more important information about String.
[07:28] With the help of String, we can create an empty String value as well.
[07:33] For example, here I'm trying to create an empty String object.
[07:37] The object to reference name is emptyString itself.
[07:40] Inside this emptyString I'm simply storing an empty value.
[07:45] I'm just giving double quotes and I'm not even giving a space.
[07:49] So this represents an empty string.
[07:51] Why we are calling this an empty string?
[07:53] Because my string does not hold even one character as well.
[07:57] If I try to give space here, then that means it is not an empty string because my String hold and character
[08:04] of type blank space.
[08:06] That's why whenever someone asks you to create an empty String, create a String just with the double
[08:12] quotes.
[08:12] Don't even give the space in between the double quotes, and the empty string is different from the
[08:18] null object.
[08:19] For example, I can create an String object and store null inside that String object.
[08:26] Let me show you how to do that.
[08:27] The object name that I have given here is nullString to this null string object
[08:31] I'm trying to assign a null value.
[08:34] So what is a null value?
[08:35] Null inside Java indicates there is nothing stored inside that object reference.
[08:41] We just gave a name to the object reference, and this object reference is not going to hold any data,
[08:49] which means indirectly, it is not going to refer to the any memory location inside the heap memory.
[08:55] So there is a clear difference between these two objects.
[08:59] Empty string is always going to have some representation inside the heap memory.
[09:03] Like inside heap memory, there is going to be a memory location, and inside that memory location the
[09:09] JVM is going to hold the empty string value, and the same memory location is going to be pointed to
[09:16] this variable name, which is empty string.
[09:18] But coming to the null string, it does not have any value assigned.
[09:22] That's why JVM is never going to create any memory location for this object.
[09:27] That means it is an orphan object reference variable name which is created inside JVM for the future
[09:35] usage inside your Java program.
[09:37] I hope you are clear with the differences of empty string and null string.
[09:41] Whatever we discuss inside this lecture.
[09:44] For your reference, I have mentioned inside this slide.
[09:47] So please read this slide as well to revise this concept one more time and post that.
[09:52] please, please try to run the same examples inside your Java project as well.
[09:58] Thank you and I'll catch you in the next lecture
[10:00] bye.

----------------------------------------
