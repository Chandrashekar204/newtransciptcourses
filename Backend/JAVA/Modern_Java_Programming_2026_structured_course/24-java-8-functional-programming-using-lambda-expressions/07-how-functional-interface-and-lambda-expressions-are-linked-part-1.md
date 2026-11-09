# 24.7 — How Functional Interface & Lambda expressions are linked - Part 1

> Section 24: [JAVA 8] Functional Programming using lambda expressions

[00:00] All right
[00:01] now is the time to discuss about the relationship between the Functional interface and the lambda expression.
[00:07] As of now, we know how to create a lambda expression by following the lambda syntax.
[00:11] And we also know how to create a Functional interface.
[00:14] The knowledge that right now we are missing is how to integrate both of them, and create a valid and
[00:21] compiled lambda expression.
[00:23] Let's try to explore the same inside this lecture.
[00:25] Since we are into the new section, I have created a new Java project with the name
[00:31] section_24 the same
[00:32] I'm going to check in into the GitHub repo for your reference as well.
[00:35] Inside this project you can see I have created a package with the name com.eazybytes.lambda.
[00:40] And inside this package I'm going to first create a Functional interface by selecting the option as
[00:46] interface here.
[00:47] And the interface name I'm going to mention as hello.
[00:50] So inside these interface I'm going to create a single abstract method.
[00:55] I hope you remember the thumb rule of Functional interface.
[00:58] It should have only one abstract method.
[01:00] So the abstract method that I want to create here is public followed by void
[01:05] and after the void I'm going to mention the abstract method name, which is sayHello() and it is not
[01:11] going to accept any input parameter.
[01:13] So this is a simple abstract method that I want to create.
[01:15] We know by default all the abstract methods are public.
[01:19] That's why mentioning this public also is not needed.
[01:23] My IntelliJ also telling me saying that modifier public is redundant for interface members.
[01:28] So let me remove this public as well.
[01:30] And this is a single abstract method that I have created inside my interface.
[01:35] So this is a normal interface.
[01:37] And we can call this interface also as a Functional interface because it has one and only one abstract
[01:44] method. If needed
[01:45] we can also mention Functional interface annotation on top of this interface.
[01:50] The advantage that we get when we mention these annotation on top of the interface is it is going to
[01:55] stop the other developers or the same developer from adding another abstract method.
[02:01] For example, here, if I try to create one more abstract method with the name, sayHello1().
[02:06] You can see I'm getting a compilation error saying that multiple non overriding abstract methods found
[02:12] in interface.
[02:14] This way the compiler is going to stop the developers from adding multiple abstract methods.
[02:20] I hope this makes sense to you.
[02:21] Let me remove these second abstract method that I have added.
[02:25] With that the compilation error is going to be resolved.
[02:27] So now we have a valid Functional interface available. Using these Functional interface I'm going to
[02:33] build a valid compiled lambda expression.
[02:36] So to create a lambda expression I'm going to create a new Java class with the name LambdaExpressionDemo.
[02:43] .
[02:44] Inside this class
[02:45] first I'm going to create the main() method followed by I'm going to create one more static method with
[02:51] the name public static void, and the method name I'm going to mention as process().
[02:57] To this method, I'm going to send the hello data type as an input parameter.
[03:02] That's why I'm trying to mention Hello h.
[03:05] And inside this static method I'm going to simply invoke the sayHello() method.
[03:10] I hope you're clear.
[03:11] I'm not doing anything new here.
[03:13] I'm just trying to invoke the say hello abstract method using the data type of Help.
[03:18] So whenever I want to invoke this method, I need to pass the object of subtype of this Hello interface.
[03:23] As of now, we don't have any subtypes.
[03:26] If you have intentions to invoke these process method by following the imperative approach, then obviously
[03:32] the option that we have is to create a subtype of this hello class and the object of that specific subtype
[03:38] we need to create.
[03:39] And the same we need to pass.
[03:40] And using the object of the hello subtype, the sayHello() method is going to be invoked.
[03:45] But right now we're trying to explore about the Functional style.
[03:49] And in the same process we also want to leverage the lambda expression.
[03:52] So first let me show you how to build a lambda expression by using these
[03:56] Hello Functional interface. For the same,
[03:59] inside the main() method I'm going to create a variable of type
[04:03] Hello, to this I'm going to assign a lambda expression, which is going to have the implementation logic
[04:09] of this method which is sayHello().
[04:12] So what is this method is accepting it is not accepting any input parameter.
[04:16] That's why I'm going to straight away mention empty parentheses followed by lambda expression symbol.
[04:22] And inside the lambda expression body I'm going to have a System.out.println() which is going
[04:27] to print the String
[04:28] Hello.
[04:29] So this is a simple lambda expression that I'm trying to build based upon the single abstract method
[04:34] inside my Hello interface.
[04:37] Behind the scenes
[04:37] based upon this lambda expression, my compiler is going to have all kinds of information like what
[04:43] is the method name,
[04:44] what is the return type of it, what is the input parameter types ?
[04:47] Because inside this Hello interface, there is only a single abstract method.
[04:51] And that single abstract method implementation we are trying to achieve with these lambda expression
[04:56] Here
[04:57] if I try to be oversmart and try to mention
[05:00] an input parameter like a
[05:01] you can see my compiler is going to throw an error saying that incompatible parameter types in lambda
[05:07] expression wrong number of parameters.
[05:10] So it is expecting zero parameters.
[05:11] But we are trying to pass one parameter.
[05:14] So whenever we type these parameter, my compiler will go and check whether my abstract method inside
[05:19] these Hello interface is having any input parameter.
[05:22] Since it is not accepting any input parameter, we are going to get a compilation error.
[05:26] I hope you are getting how the link between Functional interface and lambda expression is going to work.
[05:31] So whenever you want to write a lambda expression, you need to have a supporting Functional interface
[05:36] which has a single abstract method.
[05:39] So based upon that single abstract method, the compiler is not going to expect you to provide the method
[05:45] name.
[05:45] What are the return type,
[05:46] what are the input parameter data type ?
[05:48] You can simply write a minimal Java code by following these kind of lambda expression syntax.
[05:55] So now what I can do is inside this variable I have a behavior which can be used by other methods.
[06:01] So here I'm going to invoke the process() method.
[06:04] And to this process() method I'm going to pass
[06:06] hello.
[06:07] So what I'm trying to do here is to the process() method
[06:09] I'm trying to send the my business logic as an input parameter.
[06:14] So previously in the imperative approach we can only send that data as an input parameter.
[06:19] But with the lambda expression we can pass the behavior as an input to the methods.
[06:25] And that's why if I execute this class I'm going to get the output
[06:29] Hello inside my console.
[06:31] So here you can see I have the output as hello.
[06:34] Similarly if I want I can create one more lambda expression with the variable name as hello1.
[06:39] This time I can just mention hello world and the same
[06:44] I can also pass to the process().
[06:46] This time
[06:47] if I try to invoke these class, I'm going to get the output as Hello and Hello world.
[06:52] I hope you are seeing the beauty of lambda expression on the fly
[06:56] we are able to create the behavior for a particular method and the same behavior we are throwing at
[07:02] other methods to use them.
[07:04] Whereas if you go with the imperative approach, you will create a subclass of Hello interface.
[07:09] And inside the subclass of Hello interface, you're going to override the abstract method with a business
[07:15] logic.
[07:15] And with that, you're going to get tired with the same business logic.
[07:19] Every time someone is going to invoke your sayHello() method, but with the help of lambda expression,
[07:25] we can write any kind of business logic, and the same can be sent as an input to other methods.
[07:31] So this is one of the great advantage that we have with the lambda expressions.
[07:35] I hope this lecture provided some basic understanding about the relationship between the Functional
[07:40] interface and lambda expression.
[07:42] Let's try to continue this discussion in the next lecture as well.
[07:45] Thank you,
[07:46] bye.

----------------------------------------
