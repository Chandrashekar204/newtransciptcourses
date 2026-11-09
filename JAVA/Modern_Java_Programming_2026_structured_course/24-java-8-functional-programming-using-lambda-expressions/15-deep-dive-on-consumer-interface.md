# 24.15 — Deep dive on Consumer interface

> Section 24: [JAVA 8] Functional Programming using lambda expressions

[00:00] The next Functional interface that we are going to discuss is Consumer.
[00:04] This Consumer interface and the next interface that we are going to discuss in the next lecture with
[00:09] the name Supplier.
[00:10] They both are very important.
[00:12] I want you to be very attentive while we are discussing about Consumer and Supplier interfaces.
[00:17] So what is the scenario where we need to use the Consumer function interface to define the lambda expression?
[00:23] This can be your question.
[00:25] The scenario is very simple, like the name itself is conveying whenever your lambda expression only
[00:31] consumes the input data, but not return anything as an output.
[00:37] In such scenarios you can use the Consumer functional interface. Like you can see here, this Consumer
[00:43] function interface
[00:44] It has a abstract method with the name accept().
[00:46] It is always going to accept a input parameter of any data type, but it is not going to return anything.
[00:52] That's why the return type of this method is void.
[00:55] So in this kind of scenarios where your lambda expression only consumes or accepts the data but not
[01:01] return any output, you can happily use the Consumer functional interface, the image
[01:07] also, it should be pretty clear for you it has only the input but not the output.
[01:12] And apart from these abstract method, the Consumer function interface, it has a default method with
[01:18] the name
[01:18] andThen(), which is going to help us to perform the chaining of multiple consumer lambda expressions.
[01:25] And these Consumer function interface
[01:27] It is not going to have any static methods.
[01:30] So let's explore these Consumer function interface inside IntelliJ
[01:33] post that we can also see a demo of this functional interface.
[01:37] Here I'm going to search for Consumer.
[01:40] And you can see it is a function interface which is going to accept an input of type T.
[01:46] And it is not going to return anything. Apart from this accept() method
[01:50] it also has andThen() default method which is going to help us to chain multiple consumer lambda expressions.
[01:57] So let me create a Java class to show you that demo of Consumer.
[02:01] So the class name I'll just mention as ConsumerDemo followed by I'm going to create the main() method.
[02:08] First I'm going to define a lambda expression which is going to accept a String input data and convert
[02:15] the input data into the uppercase and post that it is going to simply print the uppercase String data
[02:22] onto the console.
[02:22] It is not going to return anything to the caller or invoking method. Since in this scenario we're not
[02:29] going to return anything as an output, but accepting an input data type of type T, we can happily
[02:35] use Consumer functional interface.
[02:37] So inside the angle brackets I'm going to mention string, followed by
[02:42] I'll just mention the variable name as convertAndDisplay on the right hand side.
[02:47] Let me write the lambda expression with the input parameter name as input, followed by lambda symbol
[02:54] post that I'm going to type System.out.println() and to this println() method
[02:59] I'm going to pass the output from the toUppercase() method.
[03:04] With that, I have a lambda expression ready, which is aligned to the abstract method defined inside
[03:10] this Consumer functional interface.
[03:12] So as a next step, what I'm going to do is using these variable name which is convert and display.
[03:17] I'm going to invoke the accept() method.
[03:20] And to this I'm going to pass a value which is Eazy Bytes.
[03:24] So whatever I'm trying to pass as an input, the same is going to be converted into uppercase.
[03:29] And eventually it will be printed onto the console.
[03:31] So let me execute this program.
[03:33] And you can see I'm getting the output like we expect.
[03:37] Similarly let me create one more lambda expression which is going to accept an int number.
[03:44] And it's going to calculate the square of the given int number and print it onto the console.
[03:48] So what I'm going to do is I'm going to type Consumer,
[03:51] and to this Consumer I'll provide the data type as integer followed by the variable name I'm going to
[03:57] mention as square off and on the right hand side
[04:01] let me first mention the input parameter name as num followed by lambda expression, followed by I'm
[04:07] going to have a System.out.println().
[04:10] And to this System.out.println() I'm going to pass the code which is num * num.
[04:16] So the number it is going to be multiplied by itself.
[04:19] Now I'm going to build a list with the help of Arrays.asList().
[04:24] And to this I'm going to pass numbers like 1, 2, 3, 4, 5, 6, 7, 8, 9, 10.
[04:33] So let me catch the List object on the left hand side by mentioning list integer with the variable name
[04:40] as numberList.
[04:43] Now using this numberList, I'm going to invoke the forEach() method.
[04:48] So you can see there is a for each method available inside the List interface, which is going to accept
[04:54] an lambda expression that built with the help of Consumer functional interface.
[05:00] So to this far h I can pass the square off, which is the lambda expression that I built with the help
[05:05] of Consumer.
[05:06] So if I execute this program, all the elements, they'll be processed based upon the logic that I have
[05:11] written.
[05:12] And eventually they will be displayed onto the console.
[05:15] But this lambda expression, it is not going to return anything.
[05:17] That's why you'll be able to see the square of these numbers onto the console.
[05:22] So let me execute this program.
[05:23] You can see we have the square values of all the numbers that we have inside the List.
[05:29] I hope this makes sense to you.
[05:30] Now let me show you the demo of the default method available inside the Consumer interface.
[05:35] For the same, I'm going to create a new lambda expression with the help of Consumer interface this
[05:42] lambda expression
[05:43] also, it is going to accept the String input data type.
[05:46] That's why I have mentioned the String inside the angle brackets of Consumer. Post that I'll mention
[05:51] the variable name as append input.
[05:54] So on the right hand side, let me accept the input with the variable name as input, followed by lambda
[06:01] symbol and post that I'm going to write a System.out.println().
[06:04] Inside this System.out.println(), I'm going to write a statement which is new value after appending is
[06:15] colon hello in completely capital letters followed by space.
[06:20] And after that I'm going to append whatever input that I have received.
[06:25] So basically what this lambda expression it is going to do is whatever input that I'm trying to send
[06:30] the same it is going to be append to this line.
[06:33] Now what I'm going to do is I'll try to change these append input and this convert and display using
[06:39] the andThen()method.
[06:41] So first let me invoke appendInput and invoke the andThen() default method.
[06:46] And to this
[06:46] andThen() I'm going to pass the lambda variable name which is convert and display post that I'm going
[06:53] to invoke the accept() method.
[06:55] To this accept() method, I'm going to pass the input as lambda expression.
[07:00] If I execute this program, you'll be able to see that this lambda expression is going to be appended
[07:07] to this statement.
[07:08] So let me execute this program.
[07:10] You can see there is a statement which is new value after appending is hello lambda expression.
[07:16] And we also have a sentence with the name lambda expression which printed based upon the code that we
[07:21] have written here.
[07:22] So basically what it has done is first it has executed this lambda expression followed by it has executed
[07:28] this lambda expression.
[07:29] So that's why we are getting this System.out.println()
[07:33] as an output followed by this one which we have defined as part of this lambda expression.
[07:39] I hope you are clear.
[07:40] In the next lecture let's discuss about the sibling of consumer which is Supplier.
[07:45] I'll explain you why I am calling this as a sibling in the next lecture.
[07:49] Thank you,
[07:49] bye.

----------------------------------------
