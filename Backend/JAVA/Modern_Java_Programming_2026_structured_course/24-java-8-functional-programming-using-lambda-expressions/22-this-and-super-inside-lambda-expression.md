# 24.22 — this and super inside lambda expression

> Section 24: [JAVA 8] Functional Programming using lambda expressions

[00:00] One of the complex questions that you may receive around the lambda expressions and the anonymous inner
[00:05] class is how the this and the super keyword is going to work in these two scenarios.
[00:11] So let's try to understand the same inside this lecture with a small demo.
[00:15] To show you the demo, I'm going to create a new Java class with the name This Demo.
[00:20] I'm going to show you the demo of this keyword.
[00:24] Whatever we discussed for this
[00:26] the same applies for super keyword as well.
[00:28] So inside these class, first let me create the main() method post that I'm going to create
[00:34] a couple of instance are non-static methods.
[00:37] So the very first method that I'm going to create here is, public.
[00:42] After the public I'm going to mention printer as a return data type, followed by the method name I'm
[00:47] going to mention as getLambdaPrinter().
[00:51] So basically this method is going to return the lambda expression of type Printer.
[00:56] So Printer is a function interface that we have created in the previous lecture.
[01:00] So if we can open this you can see this is the Function interface with a single abstract method with
[01:05] the name print.
[01:05] Now let me go to the ThisDemo class.
[01:08] Inside this method first I'm going to create a lambda expression with the help of Printer functional interface.
[01:15] So my lambda expression it is going to accept an input parameter.
[01:19] So the parameter name I'm going to give as msg.
[01:22] After that lambda expression I'm going to write System.out.println(), to this System.out.println()
[01:27] method I'm going to first pass the message, which is the input parameter that I have received,
[01:34] followed by.
[01:35] I'll mention the append symbol after the append symbol inside the String
[01:39] I'm going to mention the colon with this
[01:41] space before and after and after this colon, I'm going to append that text which is
[01:49] this.getClass().
[01:50] So whenever we are using this code which is this.getClass() , it is going to print the current class
[01:56] name where the current code is being executed.
[01:59] So these are lambda expression inside lambda expressions always.
[02:03] This refers to the class where this lambda expression is created.
[02:07] So this lambda expression is created inside a method which belongs to the class name which is ThisDemo.
[02:13] That's why we are going to get a complete qualified name of this class as an output here.
[02:18] At last, I'm going to return this lambda expression as an output from this method.
[02:24] Similarly, let me create one more instance method, but this time I'll mention the method name as
[02:30] getAnonymousPrinter().
[02:33] Inside this method, I'm going to use the Anonymous class to pass the behavior with the help of this
[02:39] printer variable.
[02:40] So whenever we want to create a Anonymous inner class, we just have to type new Printer and after typing
[02:47] Printer, if you press enter, your interface is going to ask you to overwrite the logic inside the
[02:53] print() method.
[02:54] So what I'm going to do is I'll take the same code that we have written as part of the lambda expression
[03:00] and mention here.
[03:01] So let me resolve this compilation error by replacing this MSC with input
[03:06] and at last I can mention a semicolon here.
[03:08] So this time this keyword which we are trying to refer to print the class name, it is not going to
[03:15] refer to the outer class, because with this code we have created an AnonymousInner class.
[03:22] So whenever you are referring this keyword inside an AnonymousInner class code, it is going to refer
[03:28] to the same AnonymousInner class.
[03:30] Whereas for the lambda expression, it is always going to refer to the class where this lambda expression
[03:37] is created.
[03:37] That's why we are going to get a different output when you try to invoke both of these methods.
[03:42] So in order to invoke both these methods, first I need to create the object of ThisDemo class.
[03:47] Because these are not static methods, I can't invoke them directly.
[03:51] The reason why I have created instance methods is this keyword is only applicable for the instance methods.
[03:57] Inside static methods, this and super keywords.
[04:00] They are not going to make any sense.
[04:02] I hope it makes sense.
[04:03] So first let me create the ThisDemo class with the variable name as thisDemo itself post that I'm
[04:10] going to invoke the method which is getLambdaPrinter(), which is going to give me a lambda expression,
[04:18] which I can store with the variable name as lambdaPrinter.
[04:23] So using these lambdaPrinter, I can try to invoke the print() method.
[04:28] To this print() method I can pass the output which is lambda expression.
[04:33] So this value is going to be used here.
[04:36] And to this value This.getClass() output is going to be appended along with the colon.
[04:41] In the similar lines
[04:42] let me try to invoke the getAnonymousPrinter() method.
[04:48] On the right hand side
[04:49] I'm going to mention the variable name as an AnonymousPrinter.
[04:53] So using this AnonymousPrinter I'm trying to invoke the print() method and to the print() method I'm going
[04:59] to
[05:00] the input, which is AnonymousInner class.
[05:05] So now I'm going to execute this code.
[05:07] Let me execute this code.
[05:08] You can see whenever we are trying to refer to the this keyword inside the lambda expression, it is
[05:13] referring to the current class where the lambda expression is returned.
[05:18] So what is the class where we have returned?
[05:19] It is ThisDemo, but coming to the code that we have written with the help of AnonymousInner class,
[05:24] this always referred to the AnonymousInner class itself.
[05:29] So that's why the class name here you can see ThisDemo$1.
[05:33] Since my AnonymousInner class, it is not going to have any name behind the scenes.
[05:37] The compiler, it is going to give a name to it, which is one.
[05:41] So inside a normal class we can create any number of AnonymousInner classes
[05:46] that's why it is trying to give numbers like one, two, three.
[05:49] In our scenario, since we have created only one AnonymousInner class, the same is represented here
[05:55] with these dollar one.
[05:57] So with this, I'm assuming you are clear about the point, which is always
[06:02] this refers to the current class where the lambda expression is created, whereas in the AnonymousInner
[06:08] class scenario, this always refers to the AnonymousInner class itself.
[06:12] Long back when we were discussing about the differences between AnonymousInner class and lambda expression,
[06:17] I have highlighted this point saying that this inside it always referred to the current inner class.
[06:23] So whereas under the lambda expression, this inside it always referred to the outer enclosing class.
[06:30] I hope now this point makes sense to you.
[06:32] Whatever example that we have discussed inside this lecture, I have mentioned inside this slide for
[06:37] your reference along with its output.
[06:40] I just try to show you the demo with the help of this keyword.
[06:43] The same kind of concept applicable for super keyword as well.
[06:47] I hope this makes sense to you.
[06:49] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
