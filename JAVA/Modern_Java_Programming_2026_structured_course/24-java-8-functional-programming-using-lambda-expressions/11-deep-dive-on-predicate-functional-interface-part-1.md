# 24.11 — Deep dive on Predicate functional interface - Part 1

> Section 24: [JAVA 8] Functional Programming using lambda expressions

[00:00] Inside this lecture, let's try to understand about the Predicate Functional interface.
[00:05] This is the most commonly used Functional interface by developers in real projects as well.
[00:11] So Predicate is a functional interface.
[00:13] And you can happily create the lambda expression by leveraging the single abstract method available
[00:19] inside these Functional interface.
[00:21] But you need to be aware about when to use these functional interface to create a lambda expression.
[00:27] This Predicate functional interface you can use in the scenarios where you want to accept a single input
[00:34] parameter.
[00:35] And this input parameter can belong to any data type.
[00:39] That's why you can see after the interface name we have generics with the type as T.
[00:43] This T indicates that this Predicate interface is going to handle any kind of input data type.
[00:49] So based upon these input parameter you're going to write some business logic.
[00:54] And from the business logic, if you want to return a boolean value, then in all such scenarios you
[00:59] can use Predicate function interface to create the lambda expression.
[01:04] I have mentioned other details about these interface in this slide, but slides are boring to discuss.
[01:10] That's why let's go to intellect and try to open these Function interface so that it is going to be
[01:15] more clear for you.
[01:16] So this is the Predicate function interface available inside the package java.util.function.
[01:22] You can see after that interface name there is a generic with the type as T.
[01:27] So this T indicates the type of the input to the Predicate.
[01:31] So inside this Functional interface there is only a single abstract method with the name test().
[01:36] So this test() method it is always going to accept an input parameter of type t, and it is always going
[01:43] to return the boolean as output.
[01:45] So whenever you are into the scenario where your lambda expression should accept an input data and return
[01:51] the boolean value as an output.
[01:53] In all such scenarios, you can happily use this Functional interface Predicate to build the lambda expression.
[01:59] So if you try to export the list of methods available inside this Predicate interface.
[02:03] Apart from these single abstract method, these interface also has default methods like and(), negate(), or().
[02:11] So using these three default methods, we can chain multiple predicate lambda expressions.
[02:18] So here if you try to read the and() method documentation, it has a good documentation saying that
[02:24] it is going to return a composed predicate that represents a short circuiting logical and operation.
[02:30] Similarly, using negate(), we should be able to apply the logical not condition by using the Predicate,
[02:37] and after that we also have or(), which is going to help us to build the logical or condition.
[02:42] When I show you the demo of this method, it is going to make more sense to you.
[02:46] Basically, these methods are going to help you to chain multiple predicate conditions.
[02:50] And similarly we have static methods like isEqual() and not() method.
[02:55] So these not() static method
[02:57] it is going to help you to return a Predicate.
[02:59] That is the negation of the supplied predicate.
[03:02] Above not we have ease equal method, which is going to return a predicate that test if two arguments are
[03:08] equal according to the Objects.equals() method.
[03:12] I know this may not make any sense to you, because you don't know how to use these methods and how
[03:17] to build a lambda expression using these Functional interface.
[03:20] That's why let's see a demo so that it is going to be super clear for you.
[03:24] What I'm going to do is I'm going to create a new Java class with the name PredicateDemo inside this
[03:33] class
[03:33] first let me create the main() method, followed by I'm going to build a lambda expression, which is
[03:39] going to help me to identify if a given input number is a even number or not.
[03:45] So if you see this requirement matches with the Predicate.
[03:49] So Predicate also accepts an input parameter and it is going to result a boolean value.
[03:55] So that's why here I'll try to create a lambda expression with the help of Predicate.
[04:00] After mentioning the Predicate, we need to mention the integer as a data type inside the angle brackets.
[04:06] Because we are trying to accept a input parameter of type int using the same input value, I want to
[04:12] identify whether it is a even number or not.
[04:15] That's why I'm going to give the variable name as isEven.
[04:19] Now, on the right hand side, I need to build the lambda expression by leveraging that test() method
[04:26] available inside the Predicate.
[04:27] So this test() method, it is going to accept an input parameter of type t, since we have defined that
[04:34] type as integer.
[04:35] So the test() method, it is going to accept the input parameter of type integer.
[04:40] And at last it is also going to return the boolean as a return type.
[04:44] So first I need to mention the parentheses to this input parentheses.
[04:48] I'm going to pass a variable num which indicates my input parameter data, followed by
[04:54] I'm going to mention the lambda expression.
[04:56] After the lambda symbol I'm going to write a simple logic which
[05:00] if num exactly divisible by two, then I want to return the output from this expression.
[05:06] So the output from this expression is going to be a Boolean value, which is going to match with the
[05:11] test() method signature.
[05:13] How easily I have created a lambda expression.
[05:15] Now, if I want to use this lambda expression to evaluate if a given number is a even number or not,
[05:20] it is going to be super easy.
[05:22] I just have to invoke that test method by using the isEven lambda expression.
[05:28] To this test() method, I need to pass the number.
[05:32] Like if I try to pass the number as 16, I'm going to get a boolean value which I can try to print out
[05:38] onto the console.
[05:39] So let me copy this entire code and paste it inside these parentheses.
[05:44] Similarly, I can try to repeat this code one more time, but this time I'm going to pass the number
[05:50] as 13.
[05:51] So basically we can expect that true as output here followed by false.
[05:56] So if I try to execute this program you'll be able to see true and false as output inside the console.
[06:02] Here instead of int number
[06:04] if I try to send a string object by surrounding this 13 inside the double quotes, I'm going to get
[06:11] a compilation error because this num is of type integer, but we are trying to pass the string as an
[06:18] input.
[06:18] That's why we are getting a compilation error saying that required type is integer, but we're trying
[06:23] to provide String.
[06:24] So let me roll back so that this compilation error will get resolved.
[06:28] Now think like I want to write another lambda expression, which is going to help me to identify whether
[06:35] a given number is greater than 50 or not.
[06:37] It is also going to be super easy.
[06:39] We just have to copy this similar lambda expression.
[06:42] But this time I'm going to mention that lambda expression variable name as isGreaterThan50.
[06:49] So here I'm going to mention the business logic as num > 50.
[06:56] If this condition satisfies I'm going to get the output as true.
[07:00] Otherwise I'm going to get the output as false.
[07:03] We can further simplify this lambda expression whenever your lambda expression is accepting a single
[07:08] input parameter.
[07:09] Then mentioning these parentheses is also optional.
[07:13] Like I can remove them, and with that, your lambda expression is going to become even more simple.
[07:19] So you can see in both of these lambda expressions I have removed the parentheses because my lambda
[07:24] expression is accepting a single input parameter.
[07:27] Now I can try to copy these two lines of code and with the help of these isGreaterThan50.
[07:33] I'm going to invoke that test() method.
[07:35] We should always use the test() method whenever we are dealing with the Predicate, because inside the
[07:40] Predicate, the abstract method name is test().
[07:42] I hope this makes sense.
[07:43] Now let me go to the PredicateDemo.
[07:45] And here what I'm going to do is I'll try to send the number 61 as an first input followed by 31.
[07:52] So this time also we should get the output as true and false.
[07:56] So if I execute this program you can see I'm getting true and false.
[08:00] I hope this makes sense to you.
[08:01] As a next step, I'll show you the demo on how to chain your multiple predicate conditions.
[08:06] Here you can see I have a predicate with the name isEven and I have another Predicate
[08:11] also with the name isGreaterThan50.
[08:13] So there are two predicate conditions.
[08:15] Think like
[08:16] I have a scenario where by using both these two conditions I want to calculate the output.
[08:22] Maybe I have a scenario to check if the number is even and greater than 50.
[08:31] For this kind of scenarios, we can use the under default method available inside the Predicate functional
[08:37] interface.
[08:38] So first I need to mention the first Predicate condition, which isEven followed by I need to
[08:44] invoke the and() method.
[08:47] To this and() method, you can see it is accepting one more Predicate condition.
[08:50] So to this and() method I'm going to pass the isGreaterThan50 as an input.
[08:56] At last we need to invoke that test() method, and to this test() method I'm going to pass the input as
[09:03] 62.
[09:04] With that we are going to get the output as true.
[09:06] We can also confirm the same by having a System.out.println() and pasting this entire code inside
[09:13] this println() method.
[09:15] So the outcome we are going to get is true here, because my number is going to be greater than 50,
[09:20] and it is also going to be even.
[09:22] So if I execute this program, you can see at the end we are getting the output as true.
[09:26] Whereas if I try to change this to 63, I am going to get the output as false because one of the condition
[09:34] is failed, which is is even.
[09:37] So, here we are trying to perform the logical and operation by using the various predicate conditions.
[09:45] Here I'm trying to chain only two predicate conditions, but if needed you can keep invoking and(), or() methods
[09:51] based upon your business requirements to chain multiple predicate conditions.
[09:55] So now let me show you how to use the or() method.
[09:58] So using the
[09:59] or() method, we are going to apply the logical or condition, which means even if one of the predicate
[10:05] is going to be true, the overall output we are going to get is true.
[10:09] So let me copy these two lines of code.
[10:12] But before that let me update this comment to false.
[10:15] So here I'll update the comment saying that to check if the number is even or greater than 50.
[10:21] So here instead of and() we need to invoke the or() static method.
[10:26] And apart from that everything else is going to be same since I'm trying to pass the same input, which
[10:31] is 63 this time I'm going to get the output as true because 63 is greater than 50, so it is not a even
[10:37] number.
[10:37] So let's validate this
[10:38] by running this program you'll be able to see two at the end.
[10:41] I hope this makes sense.
[10:43] Let's continue this discussion around the predicate in the next lecture as well.
[10:47] Thank you,
[10:48] bye.

----------------------------------------
