# 4.11 — Introduction to method signature

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] Inside this lecture, let's try to discuss a very important topic which is method signature.
[00:06] Every Java method is going to have a method signature.
[00:09] And this method signature is very helpful in the concepts of method overloading and overriding that
[00:16] we are going to discuss in the coming sections.
[00:18] So what is a method signature?
[00:20] Each method is going to have a signature.
[00:23] This signature is going to help to uniquely identify a method within a specific context or within a
[00:31] specific class.
[00:32] So how the method signature is calculated.
[00:34] The method signature is composed of four important elements.
[00:39] What is the name of the method?
[00:41] What are the types of input parameters?
[00:43] What are the number of input parameters and the order of the parameters?
[00:48] Using these four elements, only a method signature is going to be calculated by your Java compiler.
[00:55] Apart from these four elements, we also have other elements like modifier, return types, parameter
[01:01] names and Throws class as part of the method syntax.
[01:05] But these are not going to be part of the signature of the method.
[01:09] Regardless of which modifier you have mentioned,
[01:11] what is the return type of the method,
[01:13] what are the parameter names that you have discussed, and what is the type of Throws class that you
[01:17] have used?
[01:18] So all these components are not going to be considered to calculate your method signature.
[01:23] And like we discussed, the signatures of a method help us to uniquely identify the methods within a
[01:30] class.
[01:30] It is not allowed to have more than one method in a class with the same signature.
[01:35] I'm going to show you this in that demo in few minutes with this quick introduction about the method
[01:40] signature
[01:41] now let me give you some method declaration examples and the equivalent method signature.
[01:46] So here you can see I have a table.
[01:48] In the first column I'm going to show you the what is the method declaration.
[01:52] And in the second column I'm going to show you the what is the corresponding method signature.
[01:57] So the very first method that I have here is " public int add( int num1, num2)".
[02:05] So when you follow this syntax to declare your method, the method signature is going to consider only
[02:11] your method name, number of parameter, types of parameter, and order of parameters.
[02:17] That's why public is ignored,
[02:18] return type int is ignored, only add is considered, and the name of parameters also is not going to
[02:25] be considered.
[02:26] Regardless
[02:26] you mentioned num1, num2 or any other name.
[02:29] The method signature doesn't care about the parameter names.
[02:32] It is only consider how many input parameters you have, what is the order of parameters and what is
[02:39] the data type of your parameters.
[02:41] So for this method, the signature is going to be simply add int, int.
[02:46] Now let's see that different method declaration.
[02:49] So here you can see I just changed the name of my parameters from num1 to num3, num2 to num4
[02:55] .
[02:55] In this scenario the signature is going to be the same because like I said before, the name of the
[03:01] parameters will not be considered to calculate the method signature.
[03:05] Now let me show you the next method declaration.
[03:08] So here there is no identifier for this method declaration.
[03:12] Since the identifier like public is not going to be considered for the method signature, you can see
[03:18] the signature of the method is going to be still the same, like add int, int.
[03:22] Let me show you the next method declaration.
[03:25] This time I have added the Throws class to the method declaration.
[03:29] Since my Throws class also is going to be ignored in the method signature calculation, the method signature
[03:35] is going to be still the same, like add int, int.
[03:38] I hope you are clear.
[03:40] Moving on to the next method declaration.
[03:42] Here the method declaration is void prinMessage( String message).
[03:46] So how to calculate the method signature?
[03:49] First we need to mention what is our method name, which is printMessage and what is the data type
[03:54] of your parameter.
[03:55] So the data type of your parameter is going to be String.
[03:58] And since there is only one parameter we have inside the signature, also we mentioned only String.
[04:03] After this we have a method which is public double add (int num1, double num2.)
[04:10] For this, obviously the method signature is going to be add int, double because the first input
[04:17] parameter data type is int the same
[04:19] we have to mention followed by what is the data type of your second input parameter, which is double.
[04:25] If I try to change the order of the input parameters like you can see in the next method.
[04:30] First, I have mentioned the double for num1, whereas for num two I'm mentioning the data type as
[04:35] int.
[04:35] So here the method signature is going to be different.
[04:39] After the add you can see first double came followed by int.
[04:43] So whenever you change the order of parameter your method signature is going to be different.
[04:48] And these two methods are not going to be treated as same methods.
[04:52] And at last I have a method which is public void
[04:55] sayHello().
[04:56] For this method you can see there are no input parameters
[04:59] I'm trying to pass.
[05:01] So the method signature is going to be simply sayHello(), which is the name of the method followed by
[05:07] empty parentheses.
[05:08] This way we should be able to calculate the method signature of any given Java method, because sometimes
[05:14] your Java compiler is not going to accept you defining multiple methods with the same method signature.
[05:20] And these method signature concept also is very important for the concepts that we are going to discuss
[05:26] in the coming sections.
[05:27] That's why I'm trying to put some efforts here. From this table
[05:31] I'm assuming this is very clear, but please note that like I highlighted the order of the parameter,
[05:37] the number of parameters and the data type of the parameters is very important during the calculation
[05:43] of method signature.
[05:44] So whenever the order is changing or the data types of parameters is changing or the number of parameters
[05:50] are changing, then the method signature is going to be different for the given methods. With this quick
[05:55] introduction about the method signature.
[05:57] Now let's try to explore more about method signature inside the Java classes that we have created.
[06:03] So here I have a Java method inside ArithmeticOperations.
[06:07] The method name is sum().
[06:08] So if I try to copy the same method, since the method signature is going to be same, you can see I'm
[06:15] going to get an error saying that so and so method is already defined.
[06:19] So here the IntelliJ is showing your method signature.
[06:23] First we are going to have what is the method name which is sum() followed by your parameter details like
[06:27] int, int.
[06:28] For example, if I try to change this variable names from num1, to num3 and num3 to num4,
[06:36] I'm going to get a compilation error inside the method body, because my method body does not
[06:41] have any clue about this num1 and num2.
[06:43] So I need to mention the same values here.
[06:46] As soon as I mentioned the same values and resolve the error inside the method body, you can see I'm
[06:51] getting an error saying that the same method is defined inside the ArithmeticOperations class.
[06:57] This is because the method signature is same for both the methods, even though parameter names are
[07:02] different.
[07:03] Very similarly, if I try to change the method name from sum to sum1, then the compilation error
[07:08] will be resolved.
[07:09] Because the method signature is going to have different method names.
[07:13] Let me revert this name back to sum and we'll get compilation error.
[07:17] The other way is to make sure to have different method signatures is by following the different data
[07:24] types for your method input parameters.
[07:26] So here I have int num3 and into num4.
[07:30] Instead I can make it as byte num3.
[07:34] With that you can see my compilation error is resolved because the signature is very different here
[07:39] the signature is some int, int where
[07:42] here the signature is going to be sum (byte, int).
[07:45] If I revert back to the int, I'll get the compilation error again.
[07:49] This time I will try to show you this modifier does not going to play any role inside your method signature
[07:55] calculation.
[07:56] I can confirm that by removing this public and you can see I'm still having the problem here.
[08:01] And very similarly, the return type also is not going to be considered for your method signature calculation.
[08:09] So here instead of int, if I try to mention as long still, I'm going to get an compilation error saying
[08:16] that some int, int is already defined.
[08:19] That's why always consider your method signatures, because Java compiler is not going to accept multiple
[08:26] methods with the same method signature inside a Java class.
[08:30] I hope you are clear.
[08:31] Now let me remove this code related to the extra sum() method that we have written.
[08:36] With that, my compiler is going to be happy.
[08:38] That's why we are not seeing any compilation errors.
[08:41] Let me save this file.
[08:43] I hope you are also doing these hands on exercises along with me.
[08:47] If not, please please pause the video and try to explore all the examples that we are discussing.
[08:52] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
