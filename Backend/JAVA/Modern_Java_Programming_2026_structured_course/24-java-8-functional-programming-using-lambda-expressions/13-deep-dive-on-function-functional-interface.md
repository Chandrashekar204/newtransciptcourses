# 24.13 — Deep dive on Function functional interface

> Section 24: [JAVA 8] Functional Programming using lambda expressions

[00:00] After Predicate
[00:01] the next most commonly used function interface is function, so there is a function with the name function
[00:08] itself inside the package
[00:09] java.util.function package.
[00:12] So this sounds like a tongue twister coming to the point, which is when to use this Functional interface
[00:18] Function to define a lambda expression. You should use this Function interface in the scenarios where
[00:25] you want to send any data type as an input, and return any data type as an output.
[00:31] This is going to look very similar to predicate, except that Predicate is going to return the boolean
[00:37] as an output, but function it is going to return any data type as an output.
[00:43] Here you can see there are two generic types T and R.
[00:46] T indicates what is the input data type and R indicates the output are the result data type.
[00:53] I mentioned a picture also here like this is a input.
[00:56] Then this is an output.
[00:57] You can send any kind of data type as an input.
[01:00] And you can also get any kind of data type as an output. Inside these function interface
[01:06] the abstract method that we have is apply.
[01:09] After these abstract method we have identity static method followed by two default methods like compose()
[01:16] and andThen().
[01:17] So let's try to evaluate about these methods by exploring these Function interface inside the IntelliJ
[01:23] Idea.
[01:24] Here let me try to open a Function interface with the name Function.
[01:28] Inside this Function interface
[01:29] the very first important information that I want you to observe is these generics T and R.
[01:35] So the T indicates what is the input data type that you are abstract method is going to accept.
[01:40] And the R indicates the return type of your abstract method.
[01:43] So let's try to build some lambda expressions with the help of these Function interface.
[01:49] Here I'm going to create a new Java class with the name FunctionDemo.
[01:55] Inside this class, as usual we need to create the main() method followed by I'm going to build a lambda
[02:01] expression, which is going to help me to convert a input toString() object into completely capital R
[02:08] uppercase letters.
[02:09] So first I need to type Function
[02:11] and coming to the input data type I'm going to mention String.
[02:15] And even for the output data type
[02:17] also I'm going to mention String because I'm expecting a String as an output.
[02:22] After this I'm going to give a name to my lambda expression with the name convert str str indicates
[02:30] String, followed by
[02:31] I'm going to write a lambda expression, which is going to accept a string as an input parameter, followed
[02:38] by
[02:38] I'm going to mention a lambda symbol, and inside my lambda expression body, I'm going to simply invoke
[02:44] the toUppercase() method.
[02:46] So if you see the beauty here, I'm able to invoke the toUppercase() method available inside the String,
[02:52] because my lambda expression is able to interpret this input variable as String based upon the data
[02:58] type that we have defined here.
[03:00] Inside the angle brackets.
[03:02] So now using this lambda expression, if I try to invoke the apply() method to this apply() method I can
[03:08] pass any String.
[03:09] Maybe I'll try to pass Eazy Bytes and the output I'm going to print out with the help of System.out.println().
[03:17] So if I execute this program, I'm going to get the output in completely capital letters.
[03:22] This time let me write another lambda expression, which is going to help me to identify the total number
[03:28] of characters inside a String.
[03:30] For the same, I'm going to copy these two lines of code and post that.
[03:35] I'm going to change the second parameter type to integer, because I'm expecting the output in an integer
[03:42] format, and the variable name I'm going to mention as get str length.
[03:48] So it is going to help me to get the length of a String.
[03:51] So here you can see I'm getting a compilation error because the toUppercase() is going to return the
[03:56] String as an output.
[03:58] But my lambda expression it should return the integer as an output.
[04:03] So that's why we are getting these compilation error.
[04:05] Let me invoke the length() method.
[04:08] With that the compilation is going to be resolved.
[04:10] We can optimize this lambda expression further like by removing these parentheses.
[04:15] Like I said before, whenever you have a single input parameter, you can get rid of these optional
[04:21] parentheses around your parameter name.
[04:24] As a next step, I need to use these getStringLength variable to invoke the apply() method.
[04:29] If I try to execute this program this time, I should get the output as ten because the total length
[04:34] of the String is ten.
[04:36] I hope you are seeing the power of Function functional interface.
[04:39] So regardless of whatever is the input data type and whatever is the output data type, you can happily
[04:46] use these Function functional interface.
[04:49] Next, let's see the demo of the static method available inside the Function interface.
[04:54] To invoke the static method, first I need to type Function followed by
[04:58] identity() is a static.
[05:00] So this identity() static method, it is going to return me a lambda expression of type Function, which
[05:06] is going to capable of returning the same input value as an output every time.
[05:12] In real projects, you may have certain scenarios where you want to take an input and return the same
[05:18] input as an output
[05:19] after processing some logic. In all such scenarios, you can happily use these identity() method.
[05:25] So on the left hand side, I need to catch the lambda expression with the variable name as same value,
[05:33] and inside these angle brackets I'm going to mention String, String.
[05:38] So with this, whenever I try to invoke the apply() method on top of the same value lambda expression,
[05:44] I'm going to get the same input value as an output.
[05:48] For example, here, if I type I Madan as an input, the output I'm going to get from these lambda
[05:55] expression is going to be hi modern itself.
[05:57] So let me try to print out the output from these apply() method.
[06:01] If I execute this class you'll be able to see that I'm getting the same Hi Madan as an output.
[06:07] Next, let's try to explore that two default methods that we have inside the Function interface.
[06:13] These two default methods are compose() and andThen() methods to show you the demo of these two default
[06:20] methods.
[06:20] First, let me create some couple of lambda expressions with the help of Function interface.
[06:25] So here I'm trying to create a lambda expression which is going to accept integer and return the integer
[06:31] as an output.
[06:32] So I'll just mention the lambda expression variable name as double value.
[06:37] Because this lambda expression which I'm going to define, it is always going to double the input number.
[06:42] I'll mention the input parameter name as num followed by lambda symbol, followed by
[06:48] I'll just simply mention num asterisk two.
[06:51] In the similar lines, let me create one more lambda expression, which is going to add three to the
[06:57] input number.
[06:58] So that's why I'm trying to mention the variable name as addThree.
[07:02] So here instead of num asterisk two I'm going to mention num + 3.
[07:07] So you can see we have two different lambda expressions that we have implemented with the Function interface.
[07:12] Now I'll try to chain them with the help of the default methods available inside the Function interface.
[07:18] So first with the help of these double value I'm going to invoke the addThen() method and post that I'm
[07:25] going to provide these addThree as an input
[07:28] for this addThen() method with these these two lambda expressions that I have written, they are going
[07:33] to be chained together on the left hand side
[07:36] I can try to catch the new lambda expression, which is of type Function integer with the variable name
[07:45] as output1.
[07:47] In the similar lines, let me try to invoke the compose() method instead of andThen() method, and this
[07:53] time I'll mention the variable name as output2.
[07:56] Now using these output1, I'm going to invoke the apply() method and to this apply() method I'm going
[08:02] to pass the input as an five.
[08:05] So the total result value I can try to print out with the help of System.out.println().
[08:10] So let me do the same for the another variable which is output2.
[08:16] So first let's try to execute this program.
[08:18] And later on we can try to understand what is happening here.
[08:21] So you can see here first I'm getting the 13 as an output.
[08:24] Later on I'm getting the 16 as an output.
[08:27] So let me mark them here.
[08:29] So first we are getting 13 followed by we are getting 16.
[08:33] Let's try to understand the difference between these two methods.
[08:36] Basically these two methods are going to help you to chain multiple lambda expressions that you have
[08:43] defined with the help of Function interface.
[08:45] But there is a difference between these two default methods.
[08:48] Whenever you are using the addThen() method
[08:51] first the left side lambda expression is going to be executed, followed by the right hand side lambda
[08:58] expression.
[08:58] So first what is going to happen,
[09:00] my number five
[09:01] it is going to be doubled.
[09:03] That's why I'm going to get the output as ten later on to the ten, it is going to add three.
[09:08] That's why I'm getting the output as 13.
[09:09] But coming to the compose() first the right hand side lambda expression is going to be executed followed
[09:16] by the left hand side lambda expression.
[09:18] With that first this is going to be executed which is five plus three, which gives output as eight.
[09:24] And post that 8 * 2,
[09:26] we are going to get the output as 16.
[09:28] I hope this discussion makes sense to you.
[09:30] And now you're clear about all the methods available inside the Function interface, all the details
[09:36] that we have discussed so far, I have mentioned in this slide for your quick reference.
[09:40] On top of that, I also have a slide comparing the Predicate and Function.
[09:45] This should be very easy.
[09:46] You should be able to easily understand the differences between them.
[09:49] My humble request is once you complete this lecture, please read these differences because these are
[09:54] very important from interview perspective.
[09:57] Thank you and I'll catch you in the next lecture by,
[09:59] bye.

----------------------------------------
