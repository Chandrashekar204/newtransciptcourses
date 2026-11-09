# 10.28 — The story of constructors & Inheritance together - Part 2

> Section 10: Inheritance in Java

[00:00] Like I said in the previous lecture, your Java are the compiler is going to take care of always invoking
[00:08] the default constructor of your superclass from your subclass constructor by mentioning this super keyword
[00:15] as a very first statement.
[00:16] So that's why even if I remove this, my code still is going to work, and it is still going to initialize
[00:23] the variables that I have initialized inside the Vehicle constructor.
[00:28] That's why this statement were able to see as an output inside the console.
[00:32] When you are trying to create the object of Car, but this behavior is going to applicable only for
[00:38] that default constructor.
[00:39] In the scenarios where your superclass have constructors that is going to accept the parameters.
[00:45] Then in such scenarios as a developer, we need to manually invoke that superclass constructor from
[00:52] the subclass constructor.
[00:53] So let me show you a demo around this.
[00:55] Think like I don't want to maintain a default constructor inside my Vehicle
[01:00] superclass.
[01:00] So what I'm going to do here is, I'm going to accept an parameter which is made for using the same value
[01:08] that I received
[01:08] as part of this input parameter, I want to initialize a made for field available inside my superclass.
[01:15] So how to do that?
[01:16] We just need to type
[01:17] this.madeFor = madeFor parameter value that we are receiving as an input.
[01:25] So this we should always use whenever you are trying to refer to a variable or a method which is specific
[01:32] to the current object, whereas super is a keyword which you need to use whenever you want to access
[01:39] a field or a method, or a constructor, which is belongs to a super class.
[01:43] With this now I no more have an default constructor inside my Vehicle
[01:48] super class.
[01:48] If I go to the Car subclass, you can see I'm getting a compilation error saying that there is no default
[01:56] constructor available inside the Vehicle
[01:58] superclass. Behind the scenes
[02:00] my compiler it is trying to add the super keyword to invoke the default constructor by mentioning these
[02:07] empty parentheses after the super keyword.
[02:09] But the problem here is right now my superclass does not have any default constructor.
[02:14] So how to resolve this issue?
[02:16] We can either have a default constructor inside the Vehicle superclass, or we need to manually invoke
[02:22] the parametric constructor using the super keyword.
[02:25] So using the super keyword, I'm going to pass an input value for my String parameter.
[02:32] So I'll just mention this time water.
[02:34] So the Vehicle is going to made for water.
[02:37] So when I pass a parameter to the super it is going to check whether my constructor is also accepting
[02:43] a single parameter of type String.
[02:45] If it is, yes, the same is going to be assigned to these madeFor, and eventually the same is going
[02:51] to be assigned to these madeFor variable available inside the object of Vehicle.
[02:56] So that's why you can see right now our compilation error is also resolved.
[03:00] So this confirms whenever your superclass does not have a default constructor.
[03:05] As a developer we need to make sure that inside our subclass constructor to invoke the superclass constructors
[03:13] with the help of super keyword like you can see here.
[03:16] Otherwise you are going to get the compilation error.
[03:19] So this is the story of the constructor with the inheritance.
[03:22] Now if I go to the constructor demo and try to invoke this code, this time we are going to get the
[03:28] output as water, because from the Car constructor we are passing the value as water, which is eventually
[03:35] going to be assigned to the madeFor variable.
[03:38] All the data points that we have discussed around the constructors and inheritance together
[03:43] I have updated them inside these three slides, so please refer them whenever you want to quickly brush
[03:49] up all the concepts that we are discussing throughout this course.
[03:52] I hope you are liking the progress that you are making.
[03:55] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
