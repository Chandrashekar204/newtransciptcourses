# 25.5 — Demo of Instance method Reference using Class type

> Section 25: [JAVA 8] Building Lambda expressions using Method References

[00:00] We discussed about the instanceMethod reference in the previous lecture, and this is the example that
[00:06] we have discussed.
[00:07] Now inside this lecture, let's try to discuss one more flavor of instanceMethod reference available
[00:14] inside Java.
[00:15] This flavor we can call it as instanceMethod reference using class type.
[00:20] As of now in the previous lecture when we were trying to invoke a instanceMethod, we first created
[00:27] the object of the class, and using the same object reference, we implemented instanceMethod reference,
[00:34] but this may not be possible in some scenarios.
[00:38] Let me explain,
[00:39] what are those special scenarios ?
[00:41] Like you can see here there is a class with the name ClassMethodReference.
[00:44] Inside this I have a list with the elements like Supply, HR, Sales and Marketing.
[00:50] Using these lists I invoke the for each method and to this
[00:55] for each method I pass the lambda expression implementation of a Consumer functional interface.
[01:02] So what I'm trying to do here, I'm just trying to consume the input parameter, which is department,
[01:08] and the same I'm trying to print out inside the lambda expression.
[01:12] So each of the elements that we have inside the list, they are going to be sent as an input to this
[01:18] lambda expression.
[01:19] And by the end of this program, all these elements are going to be printed with the help of lambda
[01:24] expression logic that we have here.
[01:26] But if you closely observe here, we are trying to invoke System.out.println() land to display
[01:32] a particular element.
[01:33] That means we are trying to leverage an instance method available inside the System.out
[01:39] We know how these System.out.println() is going to work internally.
[01:43] So this out is a static variable inside the System class.
[01:46] So when we try to invoke the static variable behind the scenes, we are going to get an object of
[01:52] PrintStream.
[01:52] And using the object of PrintStream we are going to invoke a instance method which is println().
[01:59] So here I can't mention the PrintStream object because the PrintStream object it is going to be created
[02:05] behind the scenes, and at the same time we can't simply mention the System class name.
[02:10] So the syntax that we need to follow to implement method reference in these kind of special scenarios
[02:16] is, you can type as usually whatever you have like System.out post that you need to mention two colons
[02:23] followed by your instance method.
[02:25] So this System.out behind the scenes
[02:27] it is going to create an object of PrintStream.
[02:30] And using the same object of PrintStream, we are trying to invoke these println() instance method.
[02:37] With that, you're going to get the same output which you got from the above lambda expression.
[02:42] So let's try to see the demo of this very quickly.
[02:44] I'm going to create a new class with the name class method reference post that as usual, we need to
[02:53] create the main() method inside the main() method
[02:56] first I'm going to create a list with the help of List.of() method.
[03:01] To this of() method I'm going to pass some String elements.
[03:05] For example, I'm going to mention supply followed by HR followed by sales followed by marketing.
[03:14] Post this using these list
[03:16] first, I'm going to invoke the
[03:18] forEach() method you can see this
[03:20] forEach() it is accepting the lambda expression which built based upon the Consumer Functional interface.
[03:26] So what is the purpose of Consumer functional interface?
[03:29] It is always going to accept an input of any data type, but it is not going to return anything.
[03:35] So let me invoke this method and write a lambda expression here.
[03:38] So the lambda expression it has to accept an input parameter.
[03:42] Since it is going to accept a single input parameter.
[03:44] We don't have to mention parentheses.
[03:46] We can directly mention the variable name.
[03:48] So the temporary variable name that I'm going to give here is, department post that I'll just mention
[03:54] lambda symbol followed by I'll try to mention System.out.println() and to the same
[03:59] I'm going to pass department which we have received as an input.
[04:03] So if I execute this program like you know we are going to get these elements supply, HR, sales
[04:08] marketing on the console.
[04:10] But we know this logic is already available as part of the println().
[04:15] We don't have to manually write these lambda expression.
[04:18] So that's why this time what I'm going to do is I'll just invoke List.forEach() method.
[04:24] But this time I'll try to mention System.out followed by two colons followed by and
[04:32] after this you can see I have various options to invoke the instance methods which are available inside
[04:38] the PrintStream.
[04:39] So one such method is println().
[04:41] So if I execute this program this time also you should get the similar kind of output like we are getting
[04:48] with the lambda expression that we have written with our own hands.
[04:52] So my recommendation is always, wherever possible, try to leverage the method reference so that your
[04:58] code is going to become
[04:59] even more Short-Term.
[05:01] I'm assuming you're seeing the difference between these two lines.
[05:04] So the very first line has so many characters, whereas the second line, it looks very simple and short.
[05:10] But the challenge with the last line is for someone to understand this code.
[05:15] They should know the concept of method references.
[05:18] Otherwise they will be scratching their head by looking at these operator, which is two colons.
[05:24] But I'm assuming right now you should be able to easily understand these kind of code anywhere.
[05:29] On top of that, I'm also assuming you are going to leverage these method references a lot during your
[05:35] real projects as well.
[05:37] I hope this is clear.
[05:38] In the next lecture, let's discuss the last flavor of method reference, which is constructor reference.
[05:44] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
