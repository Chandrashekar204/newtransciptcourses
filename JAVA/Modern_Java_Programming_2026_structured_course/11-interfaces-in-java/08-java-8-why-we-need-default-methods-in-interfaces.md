# 11.8 — [JAVA 8] Why we need default methods in interfaces

> Section 11: Interfaces in Java

[00:00] What are default methods in interface?
[00:03] Let's try to understand the same.
[00:04] Before I try to explain you about what are these default methods, please note that that these default
[00:10] methods are allowed only from Java 8, because inside Java 8 or JDK 8 version only the default
[00:18] methods are introduced, and from this version only we should be able to create default methods in interface.
[00:25] Any version that we have before Java 8 like Java 7,
[00:29] if you try to create default method in these old versions, then definitely you're going to get a compilation
[00:36] error.
[00:36] So in summary the default methods inside interface, they are not available from day one of Java.
[00:43] They are introduced only from Java 8.
[00:47] And with that you may have a question here like why Java people
[00:51] they introduced this default method from Java 8.
[00:55] What made them to introduce these methods?
[00:58] To explain the same, let me try to create a same superhero scenario that we have.
[01:03] Think like all of a sudden the Marvel company decided to introduce a new specification or a new abstract
[01:11] method in SuperHero interface.
[01:13] Maybe after 2 or 3 years of introducing this interface, the Marvel team, they decided to add one more
[01:20] specification by introducing a just new abstract method.
[01:24] And this may look very simple or straightforward from interface perspective, but when you introduce
[01:31] a new abstract method inside an interface, it is going to have ripple effect on all the implementation
[01:39] classes.
[01:39] Think like your interface has hundreds of implementation class.
[01:44] In all these hundreds of implementation classes, you're going to get a compilation error immediately
[01:50] saying that a new abstract method is introduced inside the super interface.
[01:56] Please overwrite the same by providing some business logic.
[01:59] So this kind of errors you may get if you try to evolve your interface with the new requirements.
[02:06] I can also show you an example
[02:08] here you can see we have a SuperHero interface.
[02:10] Initially, when we started implementing the SuperHero interface, we used to have only two abstract
[02:16] methods like usePower() and stopVillain().
[02:18] But later on, after 2 or 3 years down the line, if the super hero is going to have a new abstract
[02:25] method which is trackLiveLocation(), immediately it is going to have compilation error in all the implementation
[02:34] classes. Like you can see for IronMan, SpiderMan, CaptainAmerica
[02:38] we are having a compilation error.
[02:41] Though this new abstract method is going to help to evolve the SuperHero interface, but it is creating
[02:47] problems on the implementation class.
[02:49] The same kind of problem even Java team faced when they tried to update the thousands of interface available
[02:58] inside the Java library before Java 8, there are thousands of interfaces inside the Java library.
[03:03] Java team
[03:04] when they decided to introduce new features into these interfaces, they immediately faced the problem
[03:11] in all the subclasses with the compilation error.
[03:14] And all these Java interfaces might be being used by many of the organizations in their own business
[03:21] logic.
[03:22] So if there is a change in one of the library interface, it may have ripple effect in all the organizations
[03:30] where they are trying to use these interface.
[03:32] So it will force them to update their code.
[03:35] And updating a code for many organizations may not be a simple task.
[03:40] They may have to do a lot of research testing.
[03:42] That's why Java team, they did a lot of research and brainstorming and analysis on how to handle these
[03:49] kind of scenario.
[03:50] And at the end they choose the solution which is default method.
[03:55] So with the help of default methods, what is going to happen is, whenever a new feature want to be introduced
[04:01] inside an existing interface, instead of creating the method as an abstract method, they are going
[04:07] to create a default method with some default business logic inside it, and with that, the implementation
[04:14] subclasses
[04:15] they'll have various options.
[04:17] The very first option is they can completely ignore this new feature introduced inside the interface,
[04:22] and they can continue to work the same way like they used to work before.
[04:26] And the second option is the implementation classes
[04:29] they can accept the default behavior provided by the interface and continue to work with the help of
[04:37] default business logic.
[04:38] And the third option is the implementation classes
[04:41] if needed, they can override these default methods with their own business logic.
[04:46] So with these three kind of options the implementation classes, they can take some time to choose one
[04:53] of these option and make the changes inside the implementation classes.
[04:58] I hope you are clear with the discussion
[05:00] around why we need default methods in interface, why they are introduced in Java 8.
[05:06] In the next lecture, let's try to see the demo of default methods.
[05:10] Thank you,
[05:11] bye.

----------------------------------------
