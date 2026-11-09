# 19.5 — Generics methods in Java - Demo

> Section 19: Generics in Java

[00:00] In the previous lecture, we have created a generic class with the name GenericPair. Based upon our
[00:06] previous lecture discussion
[00:07] you may have a question which is just like how we are writing a class with the help of generics.
[00:12] Can I write a method as well with the help of generics?
[00:16] So this can be your doubt.
[00:17] Let's try to answer the same inside this lecture.
[00:20] If you can open any of the collection interface or class like List.java, here you can see they
[00:26] are using generics inside the interface definition.
[00:28] Similarly, we can also use this generics as part of the class definition.
[00:32] This confirms that the generics is not specific to only class.
[00:36] They can be used for interfaces as well.
[00:38] Now coming to our question, which is can we use a generics for the methods?
[00:43] The answer is yes.
[00:44] We have some live examples as well.
[00:47] Inside this interface you can see there are many methods like add() which are accepting a generic data
[00:54] type as an input parameter.
[00:56] So here you can see they are trying to refer to the same input data type that we have as part of the
[01:02] class definition.
[01:03] So this is one style of writing methods with the help of generics.
[01:08] In this kind of approach, the data type of your generic elements, they are going to be inferred based
[01:14] upon the object of the class that you are going to create.
[01:16] We have many live examples here and how to write methods with the help of generic.
[01:21] We also have a get() method which is going to return a data type of type E.
[01:26] With this you may have another question which is can I define methods with the generics in a normal
[01:34] class?
[01:34] When I say normal class, the class definition does not have any generics.
[01:38] But is it possible to define a method with generics in these kind of normal classes?
[01:45] So that can be your question.
[01:46] The answer for your question is yes.
[01:48] Let me show you a demo as well.
[01:50] I'm going to create a new Java class which is GenericMethodDemo.
[01:56] Inside this class, I'm not going to define any generics as part of the class definition.
[02:02] Let me try to create a main() method directly after the main method I'm going to define a static method.
[02:09] So I'm going to type public static void printArray().
[02:14] So the name of the method is going to be printArray(). To this printArray() method
[02:19] for now let's define input parameter as array of String objects.
[02:24] So the same array of String objects.
[02:27] I am going to print them with the help of
[02:29] for each loop I'll just mention String element colon array and at last inside the for loop I'm going
[02:38] to write System.out.println().
[02:40] And with this this out I'm going to print the element.
[02:42] So this is a normal method which is going to accept a array of String objects.
[02:48] And all the String objects available inside the array.
[02:51] They are going to be printed. Inside the main() method
[02:53] what I'm going to do is I'm going to create an object of Array, which is going to store String objects.
[03:00] The variable name I'm going to give it as stringArray.
[03:04] And inside this I'll just try to store a couple of string objects.
[03:08] The very first one is hello, followed by inside the second one.
[03:12] I'm going to store world.
[03:13] From this main method, I can try to invoke the printArray method and to the same
[03:19] I'm going to pass the stringArray as the input parameter.
[03:22] So if I execute this program you'll know what is output we are going to get.
[03:26] We are going to get the hello and the world as the output inside the console.
[03:30] As a next step, let's try to convert this printArray method as a generic method with the help of generics.
[03:36] So here instead of String I'm going to mention a generic type which is t the same I can mention here
[03:43] as well.
[03:43] But with that I'm going to get a compilation error saying that cannot resolve symbol T.
[03:48] The reason why we are getting this error is we are not using the generics inside the class definition.
[03:54] We are trying to define a generic method directly inside a normal class in this kind of scenario
[04:00] to resolve this error, just after you are modifiers like public and static, you need to mention the
[04:06] generic symbol which is angle bracket and inside the angle brackets we need to mention T.
[04:12] With that you can see the compilation error is resolved.
[04:15] If you are creating a normal non-static method.
[04:18] In that scenario, you will not be mentioning the static
[04:21] you can mention these angle brackets and inside the angle brackets you can mention the T just after
[04:26] your access modifier which is public.
[04:28] But now since we are trying to build a static method, I'm going to mention static keyword.
[04:34] Now we have built a generic method which is capable of printing any kind of array elements.
[04:41] That's why here you can see I'm not getting any compilation error as well.
[04:45] If I try to execute this program this time
[04:47] also, I'm going to get the same output since I'm trying to send the stringArray as an input, this
[04:53] T is going to be inferred as a String based upon that declaration that we have done here.
[05:00] As a next step
[05:01] this time I'm going to create an Integer array for this, the variable name I'm going to keep it as
[05:07] intArray.
[05:08] Inside this intArray I'm going to store the integer values like I'll just try to store
[05:16] 1, 2, 3, 4, 5.
[05:16] If I send this intArray as an input to this printArray() method, this t is going to be inferred as
[05:23] an integer based upon the declaration that we have defined here.
[05:27] So if I execute this program, we'll be able to see the output like hello world 12345.
[05:33] So this way you can always develop the generic methods as well based upon your business requirements.
[05:40] Everything that we discussed around the generic methods, along with the example I have highlighted
[05:45] inside this slide for your reference.
[05:47] I hope this makes sense to you.
[05:49] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
