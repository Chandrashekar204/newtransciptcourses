# 11.12 — Multiple Inheritance using interfaces - Part 2

> Section 11: Interfaces in Java

[00:00] This time, let's talk about a few scenarios where a class is involved as part of the multiple inheritance.
[00:07] Like you can see here,
[00:08] I have a class with the name C and it is extending another super class which is a, and also it is trying
[00:16] to implement an interface with the name B.
[00:18] If you see this is a multiple inheritance where it is trying to inherit the properties and methods from
[00:24] two different components, like a class and the interface.
[00:28] But the complex part here is both my super class and super interface
[00:33] they have the same method, m1().
[00:35] So inside class A it is defined as an instance method, whereas inside the interface B it is defined
[00:42] as an default method.
[00:44] Both the super class and super interface
[00:46] they have their own business logic inside the m1() method.
[00:50] Since my class C, it is trying to inherit from both these components here, there might be some ambiguity
[00:57] to my compiler whether to inherit from the superclass or from the super interface.
[01:02] So for these kind of scenarios, there is clear direction provided to the compiler by the Java team.
[01:09] The direction is always give the priority to the super class.
[01:13] That means always super class is going to win in these kind of scenarios.
[01:17] So you are a compiler
[01:19] it is going to consider the m1() method available from the super class instead of from the super interface.
[01:26] The reason is very obvious interfaces are mean to build the contract or the specifications, whereas
[01:33] the super class or a class
[01:34] they are more mean to build the actual business logic with that perspective.
[01:40] In this kind of scenarios, always the super class is going to win.
[01:44] Let me show you a quick demo around this.
[01:46] As of now you can see inside my Person interface I have a default method with the name walk().
[01:52] I am going to create very similar method in one of my super class.
[01:57] So I'm going to create a class inside my impl package.
[02:02] The class name I'm going to mention as Employee.
[02:05] Inside this method, I'm going to define the same method with the name walk().
[02:10] But since default is not allowed inside the classes, I need to mention public.
[02:16] So public void walk().
[02:17] And inside this method I'm going to update this statement as Employee walking.
[02:23] As a next step, I'm going to create a class with the name developer.
[02:28] And inside this class first I'm going to extend the super class, which is Employee,
[02:34] after that I'm also going to implement the interface which is Person.
[02:39] So here you can see I'm not getting any compilation error.
[02:42] Though my developer class is inheriting the same walk() method from the Employee and Person.
[02:48] The reason is it is very obvious in these kind of scenarios, the compiler is always going to give preference
[02:54] to the superclass.
[02:56] That's why we are able to see Employee here.
[02:58] I hope you are clear.
[02:59] I can also test this behavior.
[03:01] Let me go to Marvel Hero demo.
[03:04] Here I'm going to create the object of developer using new operator and the default constructor of developer
[03:12] post that I will invoke the walk() method.
[03:16] So let's try to see which statement we are going to have inside the console.
[03:20] Inside the console you can see Employee walking is a statement that we are seeing here.
[03:24] So this statement is coming from the superclass.
[03:27] I hope this makes sense to you.
[03:29] Now this time let me take a more complex scenario.
[03:32] Like you can see here I have two super interfaces A and B.
[03:37] The same is being extended by another interface AB.
[03:41] So here both m one methods inside the super interface.
[03:45] They are abstract methods.
[03:46] That's why inside my interface AB we are going with one of the solution where we can try to override
[03:53] the same abstract method with the same name by using this Override annotation.
[03:58] So this is the solution that we have chosen here.
[04:01] Now coming to the other methods like where m2() is defined as an abstract method in interface A and
[04:07] as a default method inside interface B.
[04:09] So in the scenario of m2(), the interface AB is going with a option or a solution where it is trying
[04:16] to override the default method, and inside this default override method, either it can write its own
[04:23] custom logic, or it can invoke default method inside the Super interface.
[04:28] So there are multiple options we have.
[04:29] But for now, let's not worry about what logic is present inside these override default method.
[04:35] Now the fun part comes when a class C it is trying to implement both the interfaces A and AB.
[04:43] In this scenario, if you see the a, B interface is having the m1() method as an abstract method
[04:50] by using these override annotation and at the same time interface A is also having the same m one abstract
[04:56] method.
[04:57] So in this kind of scenario, the solution
[05:00] is going to be
[05:01] the implementation class is always going to consider most specific Super interface.
[05:07] In this scenario, the most specific interface is going to be AB because AB is overriding the methods
[05:14] from the A and B.
[05:16] So with the use of override annotation, my AB is trying to tell I'm trying to be more specific in this
[05:22] scenario
[05:22] that's why the class C it is going to inherit the abstract method which is AB.m1().
[05:29] So since it is an abstract method, obviously the class C, it has to provide the implementation logic.
[05:35] Now coming to the m2() method here also the same rule is going to apply.
[05:40] The same m2() method is present inside A and AB but inside A we have it as an abstract method, whereas
[05:46] inside AB we have it as an default method.
[05:49] So in this scenario also AB interface is going to be most specific super interface.
[05:54] The reason is inside AB we are trying to override the m2() method with the help of this override annotation.
[06:01] That's why my class C is going to inherit that default m2() method.
[06:06] And when inherit this default m2() method, it has an option of simply accepting the default behavior
[06:13] or it can also override this default method with its own custom logic, or by invoking the Super interface
[06:20] default method.
[06:21] I hope you are clear with these explanation.
[06:23] I think it's pretty easy to understand
[06:25] that's why I'm not going to show you any demo here to save some time, but if you are interested, try
[06:30] to simulate the same class structure and interface structure and see what is going to happen inside
[06:36] your Java classes.
[06:37] Before I try to close this lecture, I want you to highlight that whenever a class which is involved
[06:44] in multiple inheritance and if it is not able to solve the problem or ambiguity by using the two solutions
[06:51] that we discussed inside this lecture, then in such scenarios, the only solution that is going to
[06:56] be accepted here is your implementation class
[07:00] it has to override the method and implement its own logic, either by defining its own custom logic
[07:07] or by invoking one of the Super interface methods.
[07:11] So in real projects, you may have these kind of scenarios whenever your Java class or Java interface
[07:17] is involved in multiple inheritance.
[07:20] So don't worry too much about it.
[07:22] Please follow the rules that we discussed.
[07:24] In the worst case, you can clear the ambiguity by simply overriding the abstract method or default
[07:30] method with your own custom logic.
[07:32] Thank you,
[07:33] bye.

----------------------------------------
