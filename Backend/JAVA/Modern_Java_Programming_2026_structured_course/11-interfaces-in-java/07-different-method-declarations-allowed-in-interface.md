# 11.7 — Different method declarations allowed in interface

> Section 11: Interfaces in Java

[00:00] Let's try to understand what type of methods we can declare or define
[00:05] inside interface.
[00:06] Inside interface
[00:07] in total, we can try to create four different kinds of methods.
[00:12] The very first one like we saw previously, abstract method followed by default method, static method
[00:19] and private methods.
[00:20] But please note that the default methods and static methods we can only create inside an interface from
[00:26] Java 8, and similarly the private methods we can only create from Java 9 version.
[00:32] So before Java 8 inside an interface, we can only create abstract methods, but from Java 8
[00:39] it is allowed to create static default methods.
[00:43] And from Java 9, like I said, we can also create private methods.
[00:46] So there is a strong reason why these default static and private methods are allowed
[00:52] from Java 8 and later onwards, I'm going to explain you what is the strong reason in the coming
[00:57] lectures.
[00:57] For now, I just wanted to highlight you that before Java 8 we can implement 100% of abstraction
[01:05] using interface, because before Java 8 only abstract methods are allowed inside an interface,
[01:12] whereas from Java 8, since default and static methods are also allowed inside an interface.
[01:19] That's why from Java 8, the difference between abstract class and interface is almost negligible.
[01:25] Using both of these options, we can achieve 0 to 100% abstraction.
[01:31] I hope you are clear with this quick introduction about what kind of methods that we can create inside
[01:36] an interface.
[01:37] Since we already discussed about the abstract methods previously, let's try to quickly revise about
[01:42] these methods.
[01:43] Whenever you are trying to declare an interface.
[01:45] The primary goal of an interface is always to outline an abstract blueprint or concept or a guidelines.
[01:52] So that's why most of the times in real projects developers, they will create interfaces to define
[01:59] multiple abstract methods.
[02:01] So we can have an interface with the zero abstract methods or more abstract methods as well.
[02:06] And whenever we are trying to declare a method inside an interface, by default it is going to be considered
[02:12] as abstract and public unless specified otherwise with the static or default keywords.
[02:18] So you can see here I also gave two examples on the left hand side for the abstract method walk() and
[02:24] sleep().
[02:25] I have mentioned the public abstract void and this is completely redundant and not required.
[02:31] So regardless whether you are using left hand side example or right hand side example to create a abstract
[02:37] method, it is going to have the same effect.
[02:40] And how to declare an abstract method,
[02:42] it is very simple.
[02:43] You can have a method name along with its return type, followed by method input parameter and any Throws
[02:50] class to throws to mention any Exception
[02:52] handling.
[02:53] After mentioning all these details inside your method signature, you can simply mention the semicolon
[02:59] without any method body and curly braces.
[03:02] So these kind of methods are going to act as a abstract method.
[03:07] And the last point that I want to highlight here is, whenever you are trying to create an abstract method
[03:11] inside an interface or an abstract class, we can't make the method as final, since it is against to
[03:17] the concept of interface and abstract classes.
[03:20] It is not allowed to define an abstract method as final inside Java. Because if final is allowed on
[03:27] top of abstract methods, then no other class or no other subclass can override the abstract method.
[03:33] And with that, the final abstract method declaration is going to become useless.
[03:38] I can also show you a quick demo around this.
[03:41] For example, here we have a SuperHero interface.
[03:44] If I try to mention final, you can see I'm getting a compilation error saying that modifier final not
[03:51] followed here.
[03:52] Why it is not allowed because this method usePower() is an abstract method.
[03:57] I hope you are clear with all the discussion that we have done inside this lecture.
[04:01] Thank you,
[04:01] bye.

----------------------------------------
