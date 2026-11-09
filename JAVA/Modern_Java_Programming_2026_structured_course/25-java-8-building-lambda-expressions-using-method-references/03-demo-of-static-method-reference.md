# 25.3 — Demo of Static Method Reference

> Section 25: [JAVA 8] Building Lambda expressions using Method References

[00:00] Inside this lecture,
[00:01] let's see the demo of one of the flavor of method reference, which is staticMethod reference.
[00:07] Since we are into the new section as per the protocol that we are following, I have created a new project
[00:13] with the name section_25.
[00:15] Inside this project, I am going to create all the examples that we are going to discuss inside this
[00:20] section.
[00:21] And at the end I am going to upload the same into the GitHub repo for your reference.
[00:25] Now inside this project, first let me create the package with the name com.eazybytes.method.reference
[00:35] .
[00:37] Inside this package, I'm going to create a new Java class with the name StaticMethodReference.
[00:43] Since we are planning to build a lambda expression, we need to have a supporting functional interface
[00:48] either we can use Java provided function interfaces like Predicate, Supplier, Consumer, or we can
[00:54] also define our own functional interface.
[00:57] Here I'm going to choose the second approach where I'm going to create my own functional interface.
[01:03] So here after selecting the Java class option I'm going to select the interface post that I'm going
[01:09] to give the name as ArithmeticOperation.
[01:12] So this is the function interface name post that I'm going to mention
[01:16] @FunctionInterface annotation followed by I'm going to create one abstract method inside this function
[01:22] interface with the name intPerformOperation
[01:27] and it is going to accept two input parameters of type int with the variable names as a and b.
[01:35] Since there is a spelling mistake inside perform.
[01:37] So let me correct it and mentioning the public is completely optional here, because this is an abstract
[01:44] method inside the interface.
[01:45] So now I have a function interface available inside my project using the same
[01:50] first, I'll show you how to create a lambda expression based upon the concepts that we have discussed
[01:55] so far in the previous lecture post, that we can build another lambda expression with the help of static
[02:01] method reference.
[02:02] So here inside the StaticMethodReference class, I'm going to create the main() method followed by
[02:09] I'm going to define the lambda expression with the help of ArithmeticOperation functional interface.
[02:15] So let me give the variable name as operation followed by
[02:19] inside the parentheses
[02:20] I'm going to mention the variable names as a, b, followed by lambda symbol followed by curly braces
[02:27] inside this curly braces
[02:29] first I'm going to perform the addition operation.
[02:32] So I'm going to write into sum is equal to a plus b the same sum I'm going to print out onto the console
[02:40] with the help of System.out.println().
[02:42] Post that I'm going to return the
[02:43] sum whoever is trying to invoke my lambda expression.
[02:47] So now you can see I have a lambda expression ready.
[02:49] Using this lambda expression, I'm going to invoke the only abstract method available which is
[02:55] performOperation().
[02:56] And to this I'm going to provide the input as two 2, 3 if needed
[03:01] I can also catch the output on the left hand side, but I don't want to catch the output here
[03:05] I simply want to invoke these performOperation() method.
[03:08] So if I execute this class, you can see I'll be getting an output file onto the console.
[03:15] So these are regular style of writing the lambda expression.
[03:19] Now think like you have a static method already with the similar kind of logic.
[03:25] For example, think like there is a static method inside this class with the same business logic.
[03:30] In such scenarios, duplicating the business logic at two different places is not going to make any
[03:36] sense.
[03:36] That's why to overcome these kind of challenges, we can happily use the staticMethod reference.
[03:41] So let me create a static method inside this class, which is public static int and the method name
[03:48] I'm going to mention as performAddition(). This method
[03:52] it is going to accept two input parameters like int a, b.
[03:58] Was that this method?
[03:59] It is going to have the same business logic that we have defined here.
[04:02] So let me copy this code and paste it here.
[04:06] Now you can see we have the same business logic at two different places.
[04:10] So this method might have developed before Java 8.
[04:13] In this kind of scenarios like we discussed we don't have to write these in detail
[04:17] lambda expression.
[04:18] Instead what we can do is we can use a staticMethod reference.
[04:22] So let me show you how to do that.
[04:24] First I'm going to mention the functional interface name which is ArithmeticOperation followed by I'm
[04:30] going to give the variable name as methodReference.
[04:34] Now on the right hand side you're going to see the interesting part.
[04:38] So first I need to mention the class name which is StaticMethodReference and post that I need to mention
[04:44] that two colons without any space.
[04:46] And with that you can see I am getting an option to invoke the performAddition() method.
[04:52] So while you're trying to invoke this performAddition(), you should not mention any parentheses.
[04:57] On top of that, you don't have to
[04:59] mention a, b like you can see here.
[05:02] So this kind of syntax is not needed because my compiler is smart enough to understand that this method,
[05:08] it is going to accept two input parameters.
[05:10] Accordingly it is going to build the lambda expression behind the scenes, just like how we did in the
[05:16] above code.
[05:16] So now we have a lambda expression ready.
[05:18] Using this lambda expression variable I'm going to invoke the method performOperation() and pass the
[05:25] same input which is 2, 3.
[05:27] So if I execute this program you can see I'm going to get the five and five two times.
[05:31] Because we have the logic with the help of lambda expression.
[05:34] And we also have another logic with the help of StaticMethodReference.
[05:39] According to me, this method reference can be used in another kind of scenarios as well.
[05:44] Think like your lambda expression is going to have 100 lines of business code.
[05:48] In such scenarios, instead of writing all your business logic inside your lambda expression like you
[05:54] can see here, what you can do is you can put all your business logic in a separate method.
[05:59] It can be a static method, or it can be an instance method.
[06:03] Once you have built all your business logic in a separate method, you can happily use the method reference
[06:09] concept.
[06:09] This way, the readability of your code also is going to be improved whenever you are trying to build
[06:15] your logic with the help of functional programming style.
[06:18] I hope this makes sense to you.
[06:20] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
