# 24.21 — Deep dive on Lexical Scoping of Lambda expressions

> Section 24: [JAVA 8] Functional Programming using lambda expressions

[00:00] As of now
[00:01] we started writing lot of lambda expressions inside the existing Java methods like main() method.
[00:07] So whenever you are trying to define a lot of lambda expressions inside the Java methods, sometimes
[00:13] you may end up using the same variable names inside your lambda expression and inside your Java method.
[00:21] And with that, you may receive a lot of compilation errors.
[00:24] To resolve these kind of compilation issues.
[00:26] First, you need to understand how the variable scope is going to work inside the lambda expression.
[00:32] So let's try to understand more details about scoping concept inside the lambda expressions.
[00:38] Like
[00:38] we know there is a similarity between the lambda expression and the method declarations like they both
[00:43] accept the input parameter and they both are going to have body which can be written inside the curly
[00:48] braces.
[00:49] They are going to have return type.
[00:50] So there are a lot of similarities between lambda expression and the method declaration that we need
[00:55] to accept first.
[00:56] But with these understanding, don't be under the assumption that the scoping is going to work very
[01:01] similarly inside the normal methods and the lambda expressions.
[01:05] The very first thumb rule that you need to be aware is, whenever you are defining a lambda expression,
[01:11] it is not going to create its own scope.
[01:14] Instead, it is going to work within the scope of the enclosing context.
[01:19] When I say the enclosing context, it is the enclosing Java method where you are trying to define your
[01:25] lambda expression.
[01:26] So this characteristics is referred as lexical scoping inside lambda expressions concept.
[01:33] Let me show you the demo on how the scoping is going to work with the lambda expressions.
[01:38] For the same, I'll go to intelliJ. Inside my IntelliJ,
[01:41] first, I'm going to create my own functional interface with the name Printer.
[01:46] So this is an interface.
[01:48] That's why I need to select the interface option followed by I'm going to mention the annotation which
[01:52] is @FunctionalInterface, followed by I'm going to define a single abstract method inside these interface.
[01:59] So the method is going to be void print
[02:01] and it is going to accept an input parameter of type String with the variable name as input.
[02:07] So this is my function interface.
[02:09] Now using this function interface I want to show you the lexical scoping of lambda expressions for the
[02:15] same
[02:15] let me create a new Java class with the name LexicalScopeTest.
[02:21] So these are class.
[02:22] Let me create it and post that I'm going to create the main() method inside the main() method
[02:28] first I'm going to create a variable with the name input and to this variable I'm going to assign a
[02:34] String object which is hello world.
[02:38] Now I'm going to create the lambda expression with the help of Printer functional interface.
[02:44] So let me type input followed by lambda symbol followed by System.out.println().
[02:51] Followed by to this println() method I'm going to pass the same variable which is input.
[02:57] So if you see here I'm getting a compilation error because variable input is already defined in the
[03:04] scope.
[03:04] So right now we have created these lambda expression inside these main() method.
[03:09] So the scope of this method is going to be shared by these lambda expression.
[03:14] It is not going to have its own scope, since the same scope is going to be accepted by this lambda
[03:20] expression.
[03:20] And getting this compilation error, because there is already a variable defined with the same name
[03:25] input.
[03:26] So if I update these two, input1 to a different parameter name, and if I use the same, I'm not
[03:32] going to get any compilation error.
[03:34] So now using this Printer.print() method I'm going to pass String object as an input.
[03:40] So here I have a String object with the name input.
[03:43] So if I execute this program you can see I'm going to get the hello world as an output.
[03:47] So this is one rule that you need to be aware.
[03:49] Don't ever try to use the same variable names that you have declared inside the method as the input
[03:56] parameter names for your lambda expression.
[03:59] But if the String input is present after my lambda expression, I'm not going to get any problem.
[04:05] So these whatever parameter name that you have defined here like input, this is going to be specific
[04:11] to my lambda expression.
[04:12] And it is not going to be affect other method scope.
[04:15] So that's why I'm able to happily create a variable with the same name input.
[04:20] And still I'm not getting any compilation error.
[04:23] So if I execute this program you can see I'm getting the proper output this time.
[04:28] Let me show you another interesting scenario to show you this scenario.
[04:32] First, let me move back the String input to the first line.
[04:36] With that we are going to get a compilation error.
[04:38] Let me change this variable name to input one in both the places inside my lambda expression.
[04:44] Now think like I have a requirement to write some good amount of business logic inside my lambda expression.
[04:50] That's why I'm trying to use curly braces to write a body inside my lambda expression.
[04:56] So as of now I have a single statement but think like
[04:59] for these System.out.println().
[05:01] I want to change the content of input variable which we have declared inside the method.
[05:07] So to this input variable I'm trying to assign a new value which is high.
[05:13] So if you see here I'm getting a compilation error saying that variable used inside lambda expression
[05:18] should be final or effective final.
[05:21] That means whenever my lambda expression is trying to use the variables that I have declared outside
[05:28] my lambda expression this variable, it is going to act as a implicitly final.
[05:34] Regardless, I am trying to mention final or not inside the variable declaration.
[05:39] Still, this variable whose scope is being shared with the lambda expression, it is going to act as
[05:44] a implicitly final.
[05:46] Do you know why we have this restriction inside Java?
[05:49] It's pretty clear.
[05:49] Think like once you have created this lambda expression, you're trying to pass this behavior to multiple
[05:55] other methods and each of the other methods, if they are trying to assign different, different values
[06:00] to these input at some point of time, especially inside the multithreading environment, you're going
[06:06] to get unexpected results, because each execution of your lambda expression is trying to have different,
[06:11] different values.
[06:12] And with that, you are going to corrupt the original value which you have defined here.
[06:17] That's why this limitation is enforced
[06:19] whenever we are dealing with the lambda expressions. We will not be able to change the content of the
[06:25] variables that we have declared outside of the lambda expression, but I should be able to use them
[06:32] without any issues.
[06:33] So here, instead of input one, I can mention input1 + input
[06:39] So the input is defined outside.
[06:42] So if I execute this program you'll be able to see that I'm getting Hello World Hello world two times
[06:47] I hope this makes sense to you.
[06:48] Now as a next step let me show you another interesting scenario.
[06:52] Think like I have declared this input with this content later on in the next line itself, I'm trying
[06:58] to assign a different value which is high.
[07:01] So these kind of variables where you are trying to assign multiple values inside your method scope.
[07:07] So such variables, you can't use them inside your lambda expressions.
[07:12] The reason is this variable is never going to act as a implicitly final, because first you assign this
[07:18] value later on, you're trying to change with a different value.
[07:21] So since this variable is never going to act as a implicitly final, we are not allowed to use these
[07:27] input variable inside my lambda expression.
[07:30] That's why I'm getting a compilation error here.
[07:32] So the compilation error says variable used in lambda expression should be final or effective final.
[07:38] I hope this makes sense.
[07:39] So to resolve this compilation error, we need to make sure we are initializing the variables only once,
[07:46] otherwise we can't use them inside your lambda expression.
[07:50] With this discussion you may have a question which is can I create my own local variables inside the
[07:57] lambda() method?
[07:58] So this can be your question.
[07:59] You can create them without any issues.
[08:02] There is no restriction.
[08:03] You can create any number of local variables inside your lambda expression.
[08:07] For example, inside my lambda expression, I'm going to create a local variable with the name msg.
[08:13] And to this I'm going to assign a content which is high.
[08:17] So the same msg I can try to append to the inpu1, input like you can see here.
[08:24] So if I execute this program this time you can see I'm going to get the output
[08:27] Hello world,
[08:29] Hi.
[08:29] So this way always feel free to create any number of local variables inside your lambda expression.
[08:36] But these local variables you will not be able to access them outside your lambda() method.
[08:41] So here if I try to access MSG, you can see I'm getting a compilation error saying that cannot resolve
[08:49] symbol msg.
[08:51] I hope you are clear around the lexical scoping the examples that we have discussed inside this lecture.
[08:56] I have mentioned them in this slide
[08:58] for your reference, please refer them for any questions.
[09:01] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
