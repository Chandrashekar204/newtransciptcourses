# 24.9 — Anonymous inner class in the place of lambda expressions

> Section 24: [JAVA 8] Functional Programming using lambda expressions

[00:00] With the help of lambda expressions were able to pass the behaviour as an input to other methods.
[00:08] Inside Java interviews, you may encounter a question saying that is, the lambda expression is the
[00:14] only possibility inside Java to pass the behaviour as an input to other methods.
[00:20] So this can be your question.
[00:21] Though lambda is the most recommended approach.
[00:24] There are other approaches as well to pass the behaviour around the methods.
[00:29] Before lambda expressions, everyone used to follow the anonymous classes approach. With the help of
[00:35] anonymous classes
[00:36] we should be able to pass the behaviour as an input to the other methods.
[00:41] Inside this lecture, let's see the demo of anonymous class and how to pass the behaviour with the help
[00:46] of anonymous classes.
[00:48] So this approach is very complex and outdated.
[00:51] You may still receive some questions around this inside your interviews.
[00:54] That's why I'm trying to cover this scenario.
[00:57] But in real projects always prefer using the lambda expressions.
[01:01] Off course, once you saw the demo of anonymous classes, you will hate anonymous classes and load the
[01:07] lambda expressions.
[01:08] I'm very confident about that.
[01:10] So to show you the demo of anonymous classes, what I can do is I can copy these LambdaExpressionDemo
[01:16] and paste inside the same package post that I'm going to rename this class name to AnonymousClassDemo.
[01:24] So inside this class, first let me delete all these code except the process() method.
[01:31] So you can see we have a process() static method which which is going to accept the parameter h of type.
[01:36] Hello.
[01:37] So this time what I'm going to do is I'm going to create a variable of type
[01:41] Hello.
[01:42] Inside my main() method. To this hello variable,
[01:45] I'm not going to assign the behaviour or the business logic with the help of lambda expression.
[01:50] Instead I'm going to use the anonymous class.
[01:53] So what is an anonymous class?
[01:54] A class that you can create without a name.
[01:57] What you can do here is you can try to type new Hello
[02:02] And as soon as you try to type hello and press enter inside your IntelliJ you can see after the hello
[02:09] constructor you have a curly brace, and inside this curly brace you need to override the abstract method
[02:15] available inside this Hello interface.
[02:18] Here, let me put a semicolon to resolve this compilation error.
[02:21] Post that I'm going to write a business logic which is System.out.println()
[02:25] anonymous is a word that I want to print.
[02:28] So if you see here this complete piece of code we can call it as AnonymousClass.
[02:34] It does not have any name, but it has the concrete methods by overriding the abstract methods available
[02:39] inside the Hello interface.
[02:41] Here it may look like you're creating the object of Hello interface, but that is not correct.
[02:46] We are indirectly creating an object of a class which is Anonymous.
[02:51] So now I can pass this hello variable to the process() method, just like how we did with the lambda expression.
[03:00] So if I execute this program you will be able to see the output anonymous inside the console.
[03:05] So if you see this code this looks very clumsy and hard to understand, especially for the junior developers.
[03:12] On top of that, if your Hello interface has like five abstract methods, all those five abstract methods
[03:18] you need to override inside your Anonymous inner class.
[03:23] So since as of now it has only one abstract method, the same I need to override.
[03:27] But like I said before, if it has multiple abstract method, we need to override all of them in order
[03:32] to create an object of AnonymousClass.
[03:35] So as and when you have more abstract methods, this code is going to look more complex and clumsy.
[03:41] With that reason though, these anonymous classes are present before Java 8 or before lambda expressions
[03:47] introduce, not many people use them because they are very complex to implement.
[03:52] I hope this makes sense to you here
[03:54] instead of passing these hello variable, we can also directly pass the behavior to these process() method.
[04:01] So what we need to do here inside these parentheses we need to try to create the Hello object.
[04:06] So here if I press enter I'm going to get a option to override all the abstract methods.
[04:12] This time I'm going to print out Anonymous 1.
[04:16] So this is a String that I want to print out.
[04:18] So if I execute this you will be able to see Anonymous and Anonymous1 as an output inside the console.
[04:24] I hope this makes sense to you.
[04:26] Everything that we discuss around the anonymous inner classes I have mentioned in this slide, anonymous
[04:31] classes
[04:31] we can also call them as Anonymous Inner classes.
[04:34] Before I try to close this lecture, let's see the differences between Anonymous inner classes and lambda
[04:40] expressions.
[04:41] We know with both of these two approaches, we should be able to pass the behavior as an input to the
[04:46] other methods, but they have their own differences.
[04:49] Let's try to understand the same.
[04:50] The very first one is Anonymous
[04:52] Inner class is a class without a name, whereas lambda expression it is an anonymous method without
[04:59] a name.
[05:00] Technically we're not giving any name to the lambda expression, but behind the scenes it is going to leverage the
[05:05] single abstract method defined inside a Functional interface.
[05:08] Moving on to the second difference anonymous inner classes.
[05:12] They can implement the interfaces with any number of abstract methods inside them.
[05:16] Whereas in order to write a lambda expression, you should only have a Functional interface which has
[05:22] one and only one abstract method.
[05:25] In the similar lines, we also have other difference, which is we can instantiate the anonymous inner
[05:30] classes and these anonymous inner classes
[05:32] they can extend other abstract and concrete classes, whereas lambda expressions we can't instantiate
[05:39] them and they cannot extend other abstract and concrete classes.
[05:43] You should only have a Functional interface with the one and only one abstract method. Coming to the
[05:48] next difference
[05:49] whenever you are trying to create the anonymous inner classes inside these anonymous inner classes code,
[05:54] you can define the instance variables and you can happily use that this keyword.
[05:59] So whenever you are using the this keyword inside an anonymous inner class, it is always going to refer
[06:04] to the current inner class.
[06:06] Whereas on the lambda expression side we can only create the local variables, but not the instance
[06:11] variables, because we can't create the objects out of lambda expressions.
[06:15] That's why we can't create the instance variables, only local variables we can declare
[06:20] and coming to that this keyword, whenever we are trying to use a this keyword inside the lambda expression,
[06:26] it is always referred to the outer enclosing class where we are trying to create the lambda expression.
[06:32] So if there is a confusion around the usage of this keyword inside the lambda expression and the anonymous
[06:38] inner class, don't worry.
[06:39] I have a separate lecture explaining about these in the coming lectures.
[06:43] At last, coming to the memory.
[06:44] Whenever we are trying to create an anonymous inner class behind the scenes, a object is going to be
[06:49] created inside the heap, whereas lambda expression,
[06:52] since it is a method implementation, the memory allocation to the lambda expression is going to happen
[06:58] inside the permanent memory, which is methodArea().
[07:01] I hope you are clear with these differences.
[07:03] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
