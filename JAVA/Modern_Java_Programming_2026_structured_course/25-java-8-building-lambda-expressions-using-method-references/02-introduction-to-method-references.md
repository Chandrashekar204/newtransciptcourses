# 25.2 — Introduction to Method References

> Section 25: [JAVA 8] Building Lambda expressions using Method References

[00:00] Welcome to the new section.
[00:02] Inside this section we are going to focus on a new concept called Method References.
[00:07] Method references are also introduced as part of Java 8 as a supporting component to build the lambda
[00:15] expressions.
[00:16] Before I try to explain you about method references, first let me explain you the problem that method
[00:22] reference is going to solve.
[00:23] Sometimes there might be already a method defined in a class which has some business logic, and you
[00:30] want to build the same kind of business logic with the help of lambda expression.
[00:35] So that's perfectly possible because lambda expressions are introduced only from Java 8.
[00:40] Before Java 8, everyone they used to define their business logic with the help of Java methods.
[00:46] So there is a good chance that there is a good possibility that a particular business logic might be
[00:52] already present in an existing Java method.
[00:55] So in this kind of scenario, you might be thinking that there is no option to leverage the existing
[01:00] Java method.
[01:01] We just have to rewrite the entire business logic with the help of lambda expression by duplicating
[01:08] all the code again.
[01:09] So this can be your initial assumption or initial thought.
[01:13] But my friend Java team, when they released functional programming and its associated new features
[01:19] inside Java 8, they know that these problem may come into picture.
[01:23] That's why they came up with a new feature called Method Reference from Java 8.
[01:29] So what are these
[01:30] Method References ?
[01:31] Method References are a special type of lambda expression, which we can build by referring to the existing
[01:39] methods.
[01:40] I know you may have too many questions right now.
[01:42] Don't worry
[01:43] when we start discussing in detail about these method references in the coming lectures, it is going
[01:48] to be super clear for you.
[01:49] For now, let's try to understand what are the different types of method references available and what
[01:54] is the syntax that we need to follow.
[01:56] Like you can see here, there are four types of method references
[02:00] introduce as part of Java 8.
[02:03] The very first one is static method reference.
[02:06] So whenever you want to use a static method and its business logic to build a lambda expression, in
[02:11] such scenarios, you can use the staticMethod reference.
[02:14] The syntax is
[02:15] first you need to mention the class name, followed by two colons.
[02:19] So you can see you need to mention two colons, not a single one.
[02:22] After these two colons, you need to mention what is your static method.
[02:26] One more thing that you need to observe here is, you should only mention your method name.
[02:31] There is no need of mentioning the parentheses after the method name, and there is also no need of
[02:37] mentioning the details about your input parameters.
[02:40] The Java compiler is going to take care of inferring the details about the lambda expression input parameters
[02:46] by looking at your Java method.
[02:48] Apart from static methods, our classes may also have instance methods.
[02:53] So if you are into a scenario where you want to refer the business logic from an instance method to
[02:58] build a lambda expression, then in such scenarios, first you need to create the object of your class
[03:03] using the same object reference and mentioning these two colons
[03:07] you can mention the instanceMethod name.
[03:10] So with that, you're going to get a new lambda expression with the business logic that you have defined
[03:15] inside the instanceMethod.
[03:17] And the next type of method reference is, reference to the instance method from the class type.
[03:23] So here you can see I'm trying to refer to the instance method with the help of class name itself.
[03:29] So this third type of method reference it is going to handle some special scenarios.
[03:34] We're going to discuss about the special scenario in the coming lectures in detail.
[03:38] So whenever you are trying to use these third type of method reference, you need to mention what is
[03:42] your class name followed by two colons.
[03:45] And after the two colons, you need to mention your instanceMethod and at last we have constructor
[03:51] reference.
[03:51] The syntax for these constructor reference is,
[03:54] you need to mention what is your class name followed by two colons.
[03:57] And after these two colons you need to mention new operator name, which is new itself.
[04:02] So after new also you can see there is no need of mentioning any parentheses.
[04:06] I hope you are clear with this syntax.
[04:08] As you might have observed, Java has introduced a new operator which is double colon.
[04:13] So this new operator, in other words we can call it as Method Reference Delimiter.
[04:19] So in future whenever you see a Java code with two colons, you can safely assume that particular code
[04:25] is built with the concept of Method References.
[04:28] I hope you're clear with this discussion.
[04:30] Please note that you can use the method references concept only in the scenarios when you are trying
[04:35] to build a lambda expression, by using the business logic present inside another Java method.
[04:40] I hope you are clear with the agenda of this section.
[04:43] In the next lecture, let's try to discuss in detail about these staticMethod reference.
[04:47] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
