# 10.33 — final keyword in Java

> Section 10: Inheritance in Java

[00:00] Sometimes when we are creating a Java class, we don't want that class to be inherited by any other
[00:07] class.
[00:08] To achieve these kind of requirements, we can simply mention the final keyword inside the class definition,
[00:15] and with that, no other subclass are no other Java class.
[00:19] They can inherit a specific superclass.
[00:22] For example
[00:23] as of now you can see I have a superclass with the name Vehicle, and this is being extended by another
[00:30] subclass which is Car.
[00:31] Once I define final keyword just before my class, the Car subclass will not be able to inherit the
[00:40] Vehicle superclass.
[00:42] That's why we are able to see a compilation error saying that cannot inherit from the final superclass,
[00:48] which is of type Vehicle.
[00:50] So this way inside your real projects, whenever you have some requirements where you want to stop the
[00:56] inheritance behavior from a specific class, you can simply mention the final keyword.
[01:03] I hope you are clear.
[01:04] Let me remove these final keywords so that the compilation error inside Car is going to be resolved.
[01:10] We can also use the final keyword just before a variable name just before a method name.
[01:16] So let's try to understand the behavior of the final keyword when we use the same at different places.
[01:22] For example, this time I'm going to use the final keyword just before the instance variable.
[01:29] Here I have an horsePower instance variable.
[01:32] After the final, I'm going to make it as final, and I'll try to initialize with a value which is 100.
[01:39] With this, if someone is trying to reassign a new value to this horsePower variable, I'm going to
[01:46] get a compilation error.
[01:47] You can see here inside the constructor
[01:50] since I'm trying to assign a new value to the final variable horsePower, it is not going to be allowed
[01:57] with this compilation error.
[01:58] So what is the error that we are getting here?
[02:00] Cannot assign a value to the final variable horsePower.
[02:04] I hope this makes sense.
[02:06] So whenever you are trying to use a final keyword on top of a variable, please make sure you are assigning
[02:12] a initial value during the declaration itself so that the same cannot be changed anywhere inside the
[02:18] class.
[02:19] Very similarly, if needed, we can also use this final keyword on top of the methods that we have inside
[02:26] the Java class.
[02:27] For example, here I have a static method.
[02:31] If I mark the static method as final, then I'm going to get a compilation error inside the subclass,
[02:37] saying that the subclass is not allowed to change our override or hide these method.
[02:44] That's why I am getting a compilation here.
[02:47] The same applies for the instance or non static methods as well.
[02:51] Let me go to another superclass.
[02:53] Maybe I'll go to the person superclass.
[02:56] And here we have many methods.
[02:59] What I can do is, I can try to put the final keyword inside the eat() method definition.
[03:05] As soon as I mentioned these final keyword, I'll be getting compilation error inside the subclasses
[03:11] like IronMan.
[03:12] You can see I'm getting a compilation error saying that I am not allowed to override these eat() method
[03:19] because this eat() method inside the superclass is marked as final.
[03:24] That's why my subclass is not allowed either to inherit or to override the same. If needed
[03:31] we can also mention this final keyword inside the method parameters
[03:35] also like I can try to change this to final String food.
[03:38] So when you use this final keyword as part of the method parameters, no piece of code inside your method
[03:45] body can change the parameter value.
[03:48] Even when you are trying to create a local variable within a scope, like inside if block or inside
[03:54] for block or inside a method body.
[03:56] So in all such scenarios, if you make a local variable as final, then no other code within that scope
[04:03] will not be able to change the local variable value.
[04:06] I hope you are completely clear about the final keyword.
[04:10] Let me revert all these final keyword changes so that all these compilation errors, they are going
[04:16] to be resolved.
[04:17] So inside my Person class I'm going to revert these final just to before these eat() method.
[04:22] So let me delete this.
[04:24] So now I don't have any compilation errors.
[04:27] Before I try to close this lecture, let me show you the slides that I have built for your revision.
[04:32] In future,
[04:33] whenever you have a question around the final keyword usage, please refer to these slides that I have
[04:39] built around the final keyword.
[04:42] I hope you are clear with the purpose of the final keyword.
[04:44] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
