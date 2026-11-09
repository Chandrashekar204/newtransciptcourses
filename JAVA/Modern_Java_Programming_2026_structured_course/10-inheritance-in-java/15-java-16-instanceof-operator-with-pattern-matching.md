# 10.15 — [JAVA 16] instanceof Operator with pattern matching

> Section 10: Inheritance in Java

[00:00] In the previous lecture we talked about the instanceof
[00:03] operator.
[00:04] So what is a syntax that we need to follow?
[00:06] First we need to mention what is the object reference name our object variable followed by instanceof
[00:12] keyword.
[00:13] After that instanceof keyword, you can mention the class name with which you're trying to check whether
[00:19] these object reference belongs.
[00:21] So this is one form of using the instanceof operator.
[00:25] So there is also a better version or better syntax of instanceof available.
[00:30] So whatever new syntax of instanceof operator that we are going to discuss.
[00:35] This syntax is introduced only in the Java 16.
[00:39] So if you are working in a Java project which is using a Java version less than 16, then you can't
[00:45] use this new syntax that we are going to discuss.
[00:48] Otherwise, you can happily use this new syntax because new syntax is better than the old syntax, which
[00:55] we have discussed in the previous lecture.
[00:57] So let me show you that new syntax for the same, I'll open the AnimalUtility.
[01:01] So as of now here you can see I'm trying to use this instanceof operator at two different places.
[01:08] One is if block and the other one is inside the else if block.
[01:11] So I'll keep this if block with the old syntax only, whereas the else if block.
[01:17] I'm going to update with the new syntax so that you have a reference for both of them.
[01:22] So the new syntax is also very similar to the old syntax, except that after the class name you can
[01:29] give a object reference name like
[01:31] I can mention cat which is the object reference name.
[01:35] And with that I don't need to perform that downcasting manually.
[01:39] I can simply remove this and inside my elseif block I can happily use this object reference name which
[01:45] is cat and using the same
[01:47] you can see I'm trying to invoke the meow() method, so it is pretty clear with the new syntax which is
[01:54] introduced in Java 16.
[01:56] The Downcasting will happen automatically behind the scenes.
[02:00] Otherwise, if you are using the old syntax, you need to perform the downcasting manually like I highlighted.
[02:06] I hope you are clear and you like the new syntax.
[02:08] The only difference between the old syntax and the new syntax is just after the class name
[02:13] you can give an object reference name.
[02:16] So as soon as you give this object reference name behind the scenes, the Downcasting is going to be
[02:21] performed by the Java and the same object reference name you can use inside your business logic.
[02:27] I hope you are clear about the two syntaxes of instanceof operator.
[02:31] Before I try to close this lecture, let me share a guideline or rule that you need to follow whenever
[02:37] you are using the instance operator.
[02:39] The rule is whenever you want to use the instanceof operator, you can only use it with the classes
[02:46] which have inheritance relationship.
[02:48] That means I can't compare these Animal with the some random class like String or any other class available
[02:56] inside your Java project.
[02:57] In such cases, I'm going to get a compilation error because instanceof operator you can only use when
[03:03] there is a superclass and subclass relationship exist.
[03:07] For example,
[03:08] here I can also show you an example.
[03:10] First, let me try to create an object of String.
[03:13] The object name is going to be input.
[03:15] And inside this I'm going to store some random data which is hello.
[03:19] So input is a String object.
[03:21] So if I try to compare String object with an Animal object reference I'm going to get a compilation
[03:28] error.
[03:29] For example, here I can mention Animal instanceof
[03:33] and if I try to compare it with the String, I'm going to get a compilation error.
[03:39] So you can see the reason is there is no relationship between Animal and String.
[03:44] That's why I'm not able to use this instanceof operator, not only String
[03:48] any class
[03:49] you can take,
[03:49] for example, I have a class with the name engine, so if I try to mention engine here, I'm going to
[03:56] still get the compilation error because there is no relationship between the Animal and Engine class.
[04:03] I hope you are clear about this rule and limitation.
[04:06] Let me remove all this code, everything that we discussed around the instanceof operator I have mentioned
[04:12] in these three slides.
[04:13] I hope you're clear.
[04:14] Thank you,
[04:15] bye.

----------------------------------------
