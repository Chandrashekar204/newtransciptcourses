# 10.29 — this and super keywords in Java

> Section 10: Inheritance in Java

[00:00] As of now
[00:01] we discussed enough details and examples around the this and the super keyword in Java. But still,
[00:07] I want to spend more time around these keywords inside this lecture explaining you about the differences
[00:14] between them and when you should use them.
[00:16] Because this is the most common topic where students may feel some complexity and they may get confused
[00:23] very easily inside the interviews.
[00:25] So let's try to understand difference between them and when to use them.
[00:29] The very first basic point that you should be knowing is, both of them are two reserved keywords
[00:35] inside Java, we are going to use the this keyword whenever we want to access a member of a current
[00:41] object, whereas super keyword we need to use if we want to access a member of a super class object.
[00:48] For example
[00:49] here you can see I have given two different examples.
[00:52] On the left hand side, I have a class of Person inside this Person class I have a constructor that
[00:58] accepts two input parameters.
[01:00] Since the parameter names to the constructor and the variable names inside the class since they both
[01:05] are same, I need to use this keyword to point to the variable present inside the current object.
[01:12] Like you can see with the help of this this.name, I'm trying to refer to the instance variable
[01:17] that I have created at the top of the class, whereas with the other name variable, we are trying to
[01:23] refer to the parameter that we have received as an input to this constructor.
[01:27] So with this, it should be clear for you.
[01:29] Whenever we want to access a member of a current object, we should be using the this keyword.
[01:35] Whereas super keyword will always come into picture in the scenarios of inheritance.
[01:41] Without inheritance, you will not be able to use the super keyword.
[01:45] Here I have an example where I have a Animal superclass and a subclass with the name Dog.
[01:51] Both these superclass and subclass, they have a same method which is makeSound().
[01:56] That means my Dog subclass overridden the method makeSound() with its own logic.
[02:02] But if my subclass has a requirement to access the method present inside the superclass, then in such
[02:09] scenarios, my subclass should use the super keyword to access the makeSound() method available inside
[02:15] the superclass.
[02:16] We can also use these, this and super keywords while we are trying to invoke the constructors.
[02:22] For example, I can use the this keyword along with the parentheses to invoke the other constructors
[02:29] from a constructor inside the same class.
[02:32] And whenever we are using the this keyword to invoke the other constructor, it should be the very first
[02:38] statement inside a constructor. On the similar lines
[02:41] we can also use the super keyword to invoke the constructors of the super class.
[02:48] Just in the previous lecture, we have discussed this scenario.
[02:51] Even in the scenario of using super keyword to construct an invocation
[02:55] in this kind of scenario
[02:56] also, we need to make sure that super constructor invocation is a very first statement inside your
[03:02] subclass constructor.
[03:03] At last, I want to highlight you that both these this and super keywords.
[03:07] They are reserved keywords inside Java.
[03:10] We can't use them as an variable identifiers or method name identifiers.
[03:15] And there is also a restriction or limitation on where we can use these these and the super keyword.
[03:22] We can only use this and super keywords in an non-static area like inside the non-static methods or
[03:30] inside the constructors.
[03:31] We will not be able to use these keywords inside the static methods or inside the static initializers.
[03:37] The reason is these keywords are specific to the objects of a super class or objects of a current class.
[03:43] Since the static method and the static initializer they belongs to the class, we will not be able to
[03:49] use these and super keyword in the static areas.
[03:53] And like I said, we can use that this keyword without the involvement of inheritance concept.
[03:59] Whereas in order to use a super keyword, you need to make sure there is a inheritance involved and
[04:05] there is a superclass and there is a subclass.
[04:07] So the most common use case of super keyword is to eliminate the confusion between the superclass and
[04:14] subclass methods that have a same name.
[04:17] I hope you are clear with this discussion.
[04:19] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
