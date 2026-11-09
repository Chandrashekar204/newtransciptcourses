# 10.16 — Static Binding and Dynamic Binding in Java

> Section 10: Inheritance in Java

[00:00] Inside this lecture we are going to talk about the concept of "Binding" and what are the types of binding
[00:06] available.
[00:07] Usually inside a Java class will be having fields and methods.
[00:11] and these methods and fields can be invoked with the help of class name or with the help of object.
[00:18] So there won't be any confusion if you have a single class which has its own static methods, instance
[00:25] methods and variables.
[00:26] But if you try to bring inheritance into your Java project, then there will be lot many scenarios like
[00:33] Upcasting, Downcasting.
[00:34] So in this kind of scenarios, your compiler sometimes it has to take a decision which method has to
[00:42] be invoked.
[00:42] For example, inside your superclass you may have a method which is method one and inside your subclasses
[00:49] also, you might have overrided that method with the same method name.
[00:54] In the case of Upcasting we saw we can upcast a subclass to a superclass.
[01:00] So when these kind of upcasting happens and if you try to invoke the method one with the help of object
[01:07] reference of superclass, then your compiler has to take a decision which method has to be invoked,
[01:13] whether it has to invoke the method present inside the superclass, or it has to invoke the method present
[01:19] inside the subclass.
[01:20] So the same kind of decision it has to take for the variables as well.
[01:24] So the effort that is going to be put by your Java to determine which method to invoke or to which variable
[01:32] to invoke is called as binding.
[01:35] In other words, we can say binding is the decision making process that establishes the connection between
[01:42] the code and the specific method or field it is trying to access.
[01:47] This binding process can happen at two stages during the compilation time and runtime.
[01:53] If the binding is happening at the compilation time, we can call that as Static Binding.
[01:58] In other words, we can also call the Static Binding as Early binding or compile time binding.
[02:04] So static binding or early binding indicates that decision that has been taken by the Java or Java
[02:12] compiler, to which method, or to which variable it has to invoke during the compilation time.
[02:18] Maybe this decision will get override during the runtime, but it has to take a decision at compile
[02:25] time about which method or which field it is going to invoke.
[02:29] Just like Static Binding, we also have Dynamic Binding.
[02:33] The other name for this Dynamic Binding is late binding or runtime binding, because as part of this
[02:40] dynamic binding, the decision is going to be taken at the runtime.
[02:45] At runtime, Java is going to check which object is being hold by an object reference.
[02:52] Using the same data, it is going to decide which method or which variable to invoke at the runtime.
[02:59] So if your Java class has private methods, or private variables, or static methods, or static variables,
[03:06] or final variables or final methods.
[03:09] So in all these kind of scenarios, the decision is going to be very simple.
[03:13] The Java always going to follow the Static Binding because private variables, private methods, static
[03:19] members and the final members, they're all going to be exclusive for a given class.
[03:24] There won't be any confusion in these kind of scenarios, only in the scenario of non private instance
[03:31] methods or instance variables.
[03:33] The compiler or Java is going to have a confusion due to inheritance.
[03:39] I know I'm talking a lot about the Static Binding and Dynamic Binding.
[03:43] You may have some questions here.
[03:44] Let me show you an example
[03:46] and with that you're going to be pretty clear here I have a Java program.
[03:51] Let's try to understand the same.
[03:53] First I have a class with the name A.
[03:55] And inside this class I have a method show().
[03:58] So this class A is going to act as a superclass for my class B.
[04:03] So B is a subclass and the A is a superclass.
[04:06] We can also confirm the same by looking at these extends
[04:09] keyword followed by A.
[04:11] So inside my subclass also the same method which is inherited from the superclass is Overrided with
[04:18] the logic specific to the subclass.
[04:21] So inside my superclass the logic is show() method.
[04:23] Inside class A is going to be printed, whereas the subclass change the message to show method in class B.
[04:30] .
[04:30] I hope you are clear.
[04:31] We have a superclass and a subclass, and both of them has the same method which is show().
[04:36] Now if you see there is a Main class and inside this Main class I have a main() method.
[04:41] First, I'm trying to create the object of A and B without any typecasting or Downcasting it's a simple
[04:49] object creation of the A class and a B class.
[04:53] So object reference we have is a and b.
[04:56] So if I try to invoke the a.show() there won't be
[05:00] any confusion to my Java compiler, because on the right hand side we have a and on the left hand side
[05:06] also we have a.
[05:07] So since there is no confusion to my compiler, the static binding is going to happen
[05:13] at this point of time, the compiler is going to take a decision that it is going to invoke the show()
[05:19] method available inside the a superclass.
[05:22] So that's why we are going to get the output as show() method in class A.
[05:26] Coming to the b.show(), even for the b.show()
[05:30] also, there won't be any confusion to my Java compiler because on the right hand side we have B constructor
[05:37] and on the left hand side also we have reference to the B class.
[05:40] So since this is going to be pretty straightforward in this scenario, also the compiler is going to
[05:46] take a static binding decision and the same it is going to follow even at the runtime.
[05:50] That's why we are getting the output, which is show() method in class B up to this point
[05:56] I'm assuming you are with me now
[05:58] the fun starts.
[05:59] So here you can see I'm trying to do the upcasting.
[06:02] I'm trying to assign the object of subclass to the object reference of superclass, which is a.
[06:09] So this obj object reference, it belongs to the class A which is a superclass.
[06:14] But inside this object reference I'm holding the object of B which is a subclass.
[06:21] So in this kind of scenarios, definitely my compiler is going to have a confusion because I'm trying
[06:27] to invoke the show method with the help of obj.
[06:30] So here my compiler does not know whether to invoke the show() method present inside the A or inside the
[06:36] B.
[06:37] So first, during the compilation time, the Java at the compiler is going to perform the static binding,
[06:43] and with the static binding, it will be under the assumption that it is going to invoke the show() method
[06:50] present inside the a superclass, because this obj belongs to the class A, but at runtime the Java
[06:58] is going to check this obj object reference points to the which object.
[07:03] So this obj object reference is pointing to the object of B subclass.
[07:09] So that's why at runtime, based upon the dynamic binding are based upon the dynamic decision taken,
[07:15] the show() method present inside the subclass is going to be invoked. The sme
[07:20] you can see I have confirmed here the output we are going to get is show() method in class B.
[07:25] I hope you are clear.
[07:26] What is a static binding and dynamic binding?
[07:29] My humble request is please create these scenario like you can create the super class subclass and you
[07:35] can also try to create this Main class.
[07:37] And you can write all these logic post that validate whether the output is coming based upon our discussion
[07:43] or not.
[07:44] In the same process, you can try to understand static binding and dynamic binding.
[07:49] So based upon these binding concept only inside Java we have another concept which is polymorphism.
[07:56] So what is a polymorphism?
[07:58] Polymorphism is one of the oops concept.
[08:01] We're going to talk about the same in the coming lectures.
[08:04] But for now I'm assuming you are clear with the binding concept.
[08:08] Thank you
[08:09] and I'll catch you in the next lecture bye.

----------------------------------------
