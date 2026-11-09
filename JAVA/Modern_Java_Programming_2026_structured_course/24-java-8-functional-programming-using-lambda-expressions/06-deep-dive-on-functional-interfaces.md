# 24.6 — Deep dive on Functional Interfaces

> Section 24: [JAVA 8] Functional Programming using lambda expressions

[00:00] We can't define lambda expression wherever we want, because in order to build a lambda expression to
[00:07] my compiler, it has to know what is the method name.
[00:11] This lambda expression is associated to it.
[00:14] What are the input parameter types?
[00:16] What are the return type of the method?
[00:18] So whenever we want to define a lambda expression we need an separate supporting component as well.
[00:24] Such a supporting component is Functional interface.
[00:28] We're going to deep dive into what is a Functional interface in few minutes.
[00:31] But before that let me try to write a lambda expression directly inside a class.
[00:36] So here you can see I have a random class with the name Test.
[00:39] Here I'll try to write a lambda expression, which is,
[00:43] it is going to accept two parameters a comma b and post that
[00:47] I'm going to mention lambda expression symbol, followed by
[00:50] I'll just mention a+b, which means I want to return the output of a + b as an return type from
[00:57] this lambda expression.
[00:59] With that, you can see I'm getting a compilation error.
[01:01] My compiler is clueless
[01:04] what is this a,
[01:05] what is the name associated to this lambda expression?
[01:08] What is the return type from this lambda expression
[01:10] business logic ?
[01:11] So all these details right now are not available regarding my lambda expression.
[01:16] That's why my compiler out of confusion it is throwing a compilation error.
[01:21] I can also try to build one more lambda expression.
[01:24] This time I will not accept any input parameter.
[01:27] I will straight away write System.out.println() with a hello String, and I'll terminate this Java statement
[01:34] with a semicolon.
[01:35] If you try to hold on to this lambda expression, you can see I'm getting a statement, which is it
[01:41] is not a statement.
[01:43] My compiler is not able to recognize
[01:45] what is the statement about. With this
[01:48] it should be clear for you that we can't write lambda expression wherever we want.
[01:52] Whenever we want to write a lambda expression, we need a supporting component.
[01:56] Such a supporting component is Functional interface.
[02:00] We can only build a lambda expression in the context of a Functional interface.
[02:06] In the next lecture, I'm going to explain you what is the relationship between Functional interface
[02:12] and lambda expression, and how to integrate them together to make them work.
[02:17] But for now, let's focus on trying to understand the concept of Functional interface.
[02:22] When we are discussing about the interfaces
[02:24] long back inside this course, I talked about the Functional interface on a high level.
[02:28] I hope you remember that.
[02:30] If not, don't worry, I'm going to quickly explain one more time about what is a Functional interface
[02:35] inside Java, a Functional interface is an interface that specifies exactly a single abstract method.
[02:42] So this single abstract method in short form we can call it as SAM.
[02:47] You can see here I have an interface with the name MyAdditionInterface.
[02:51] And inside this interface I have a single abstract method with the name int add( int a, int b).
[02:58] So this can be considered as an Functional interface inside Java because it has a single abstract method.
[03:05] Similarly, here you can see I have another interface with the name MySubtractionInterface.
[03:10] And this interface also has a single abstract method with the name subtraction().
[03:15] But if you closely observe, there is a difference between this interface and this interface.
[03:19] Inside the second interface, I have mentioned an annotation which is @FunctionalInterface.
[03:25] So whenever we mention this annotation on top of an interface, this annotation will make sure that
[03:31] my interface always have only a single abstract method.
[03:35] So since I have mentioned this annotation, no one should be able to add one more abstract method or
[03:41] they will not be able to delete these existing abstract method.
[03:45] The compiler will always complain saying that hey buddy, you need to have single abstract method inside
[03:51] and Function interface.
[03:52] So don't try to add one more abstract method, or don't try to delete the existing single abstract method.
[03:59] Whereas with the very first interface, though technically we can call this as a Functional interface,
[04:04] many other developers, they can come and add many others abstract methods, and with that it is going
[04:10] to lose the definition of Functional interface.
[04:12] That's why whenever you are trying to define a Functional interface, please make sure you are mentioning
[04:17] this annotation so that no other developers will be able to add more abstract methods.
[04:23] Apart from having a single abstract method, your Functional interface can have any number of default
[04:29] methods, static methods, and private methods.
[04:32] Just like any other interface, we can define any number of default static private methods with their
[04:38] own business logic, but we need to make sure there is only a single abstract method without any business
[04:45] logic.
[04:45] I hope you are clear.
[04:46] I'm going to test your knowledge around the Functional interface by giving some examples.
[04:51] So here I have three different interfaces.
[04:54] So please tell me whether it is a valid Functional interface or not.
[04:58] Coming to the
[04:59] first interface,
[05:00] so this is an interface
[05:01] and it has how many abstract method ?
[05:03] It has only a single abstract method.
[05:05] Do you think it is a valid Functional interface?
[05:07] Off course
[05:08] yes it is a valid Functional interface.
[05:11] Now I have a second interface with the name Print and it is extends the Hello interface.
[05:17] And inside this interface I have abstract method which is print().
[05:21] Do you think this interface is a valid Functional interface.
[05:24] Think about it.
[05:24] There is a inheritance logic here.
[05:27] So my interface which is print it is going to inherit one abstract method which is say hello.
[05:32] On top of that you are trying to add one more abstract method.
[05:36] And with that, this print interface cannot be called as a functional interface because it has two abstract
[05:43] methods.
[05:44] One is derived from the parent interface and the other one present inside itself.
[05:48] And the last interface you can see it does not have any abstract method.
[05:52] Do you think it is a valid Functional interface?
[05:54] Off course not, because it don't have a single abstract method.
[05:59] Let me give a few more examples.
[06:01] This time you can see I have a interface with the name ArithmeticOperation, and on top of this I have
[06:07] mentioned the Functional interface annotation.
[06:09] After mentioning this Functional interface annotation, I have defined two abstract methods with the same
[06:15] method name, but they are overloaded abstract methods because they are accepting two different input
[06:21] type of parameters.
[06:22] Do you think this is a valid Functional interface?
[06:24] Off course not, because there are two different abstract methods.
[06:29] Regardless, they are overloaded or not always
[06:31] only a single abstract method is allowed.
[06:34] Since we have mentioned this annotation, the compiler will throw compilation error saying that we cannot
[06:40] have two abstract methods in this interface.
[06:43] Let's see the next interface.
[06:44] Here you can see I have an interface with the name A which is of type Functional interface.
[06:50] So these are valid Functional interface because it has a single abstract method with the name m1().
[06:55] Now I have another interface which is extending the A interface.
[07:00] Inside this B interface I have the same abstract method with the same name.
[07:05] So this is like overriding.
[07:07] So with the same method signature I have an abstract method inside interface B.
[07:11] So this is somewhat tricky, but I think you should be able to answer yes, it is a valid Functional
[07:18] interface because though it is extending the abstract method m1() from A interface, since it is trying
[07:25] to override the same abstract method with the same name, with the same input parameter with the same
[07:30] method signature.
[07:31] We can treat this as a valid Functional interface.
[07:35] And at last, like you can see here, I have an interface with the name C and it has a abstract method
[07:40] with the name m2().
[07:41] So this is going to be simple.
[07:43] Yes it is a valid Functional interface.
[07:46] So regardless of I'm trying to use a Functional interface annotation or not till this is going to be
[07:51] considered as a valid Functional interface.
[07:54] And we can use this to write the lambda expression because it has a single abstract method.
[07:59] With this I'm assuming you are clear about what is a Functional interface.
[08:03] As a next step, we need to understand what is the link between lambda expression and Functional interface,
[08:09] how we can leverage this Functional interface to define the lambda expressions.
[08:14] I'm getting excited here to explain you about these beautiful concepts from the next lecture.
[08:20] I hope you are also excited.
[08:21] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
