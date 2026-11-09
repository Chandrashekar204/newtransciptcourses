# 11.11 — Multiple Inheritance using interfaces - Part 1

> Section 11: Interfaces in Java

[00:00] In the previous section,
[00:01] when we are talking about types of inheritance, we briefly talked about why Multiple inheritance is
[00:09] not allowed with the help of superclass and subclass.
[00:12] So we are going to have a diamond problem
[00:15] that's why Java is not going to allow you to inherit more than one class in the same class, but the
[00:23] same Multiple inheritance is not going to be a problem
[00:27] when we are trying to inherit multiple interfaces, we are going to get this diamond problem.
[00:32] But there are some approaches to solve this diamond problem whenever we are dealing with the multiple
[00:38] inheritance with the interfaces.
[00:40] So first let's try to understand how to build a multiple inheritance with the help of interfaces like
[00:47] you can see here, we have implementation classes like IronMan, SpiderMan and CaptainAmerica.
[00:53] Inside these classes, we are trying to implement our inherit more than one interface at the same time.
[01:00] For example, I have a interface name, SuperHero and Person.
[01:05] So this is one of the classical example of multiple inheritance using interface.
[01:11] So just like how a class can inherit multiple interfaces with the help of implements keyword, very
[01:17] similarly a interface can extend multiple other interfaces.
[01:23] Here I also gave an example.
[01:25] I have an interface with the name SuperHero and it is trying to extend multiple other interface
[01:31] the interface names are Person and Hero.
[01:34] I hope you are clear how to achieve multiple inheritance using interface.
[01:39] It's very simple.
[01:40] You can mention your list of interfaces by using comma as a separator, but when you try to achieve
[01:47] multiple inheritance with the help of interfaces, sometimes you may get a diamond problem or a ambiguity
[01:54] to your compiler.
[01:55] So let's try to understand what kind of ambiguities your compiler may face and how to solve them.
[02:02] Inside the scenario one
[02:03] I'm going to give some tricky questions around the multiple inheritance.
[02:07] Here you can see I have an Interface A and B, and inside both of these interfaces I have the same abstract
[02:16] method with the name m1().
[02:18] If another interface, which is C, is trying to extend both A, B.
[02:24] In this kind of scenarios, which m1() method is going to be inherited by my Interface C.
[02:30] So this kind of ambiguity your compiler may get.
[02:34] So this is one typical scenario that may arrive during multiple inheritance using interfaces.
[02:41] Let's see other combinations as well.
[02:43] If you take the same combination of interfaces A, B and C, this time you can see one of my interface
[02:50] which is A
[02:51] it has m1() method defined as a default method.
[02:54] Inside this m1() default method, it has some business logic, whereas interface B it is going to define
[03:01] the same m1() method as an abstract method.
[03:04] In this kind of scenario, also, your compiler is going to have an ambiguity.
[03:10] For example, inside interface C where it is trying to inherit multiple interfaces like A, B,
[03:17] it is going to have some ambiguity whether to inherit that default m1() method present inside the interface
[03:24] A, or whether to inherit the abstract m1() method available inside interface B on the very similar
[03:30] lines
[03:31] this time both of you are interfaces A and B, they are going to have the same default m1() method
[03:38] with their own respective business logic.
[03:40] In this scenario
[03:41] also, your compiler obviously will have the same ambiguity which default m1() method to inherit inside
[03:49] the interface C.
[03:50] Here
[03:50] in this scenario, we are completely talking about interfaces.
[03:54] Nowhere we are talking about implementation class.
[03:56] Regarding implementation class scenario, we're going to discuss in the coming lectures.
[04:01] But now let's try to focus on this scenario where we have multiple inheritance achieved with all interfaces
[04:07] alone.
[04:07] So to resolve this problem there are multiple options going to be used by your compiler.
[04:14] So let's try to understand what are those.
[04:16] There are three different approaches for the three different scenarios that we have discussed.
[04:20] In the very first scenario where both A and B, they are having the m1() method as an abstract method
[04:27] in this scenario, since both of them are abstract methods, your interface C can completely ignore
[04:34] about them, and your compiler also does not going to complain anything because anyway, both of them
[04:40] are abstract methods.
[04:41] Regardless of which one is going to be inherited, there is no harm is going to happen.
[04:46] But if you want to be too specific, or if you want to handle this in a more graceful manner, then
[04:51] the most recommended approach is, to define the same abstract method inside your interface C as well,
[04:58] but on top of your
[04:59] abstract method m1()
[05:01] you can mention @Override annotation.
[05:05] I hope you are clear with these
[05:06] first solution.
[05:07] Coming to the second problem, where one of the interface has a m1() method as a default method, and
[05:14] the other interface is having the m1() method as an abstract method.
[05:18] So in this kind of scenarios, the interface C,
[05:21] it has to override the conflicting method with a default method by providing its own custom logic
[05:29] or if needed, it can also call the same default methods, which is available inside the super interface
[05:36] from its own override default method inside the interface C.
[05:40] .
[05:40] And
[05:41] the last problem that we have is,
[05:42] in this scenario, both both the A and B interfaces, they are having the same m1() method defined as
[05:49] default methods.
[05:51] In this scenario as well, we need to guide the compiler to clear the ambiguity by overriding the same
[05:59] default m1() method inside the interface C and inside the override default method
[06:04] we can write our own custom logic, or we can invoke one of the default method available in the super
[06:11] interfaces.
[06:12] I know it may not be clear to you based upon our discussion.
[06:15] Let me replicate this scenario, and in the same process I can show you how to solve the problems.
[06:21] As of now, you can see my SuperHero interface
[06:23] it is extending the interface Person.
[06:26] As a next step
[06:27] I want to create one more interface with the name Hero.
[06:31] Inside this Hero interface,
[06:34] first I'm going to create an abstract method with the name walk().
[06:38] So the same abstract method I'm also going to define inside the Person as well.
[06:44] Now inside my SuperHero interface I'm going to extend one more interface, which is Hero with this
[06:51] now my SuperHero interface, it is going to inherit the walk() method from the first interface that you
[06:57] have defined inside the interface declaration.
[07:00] So the first interface that we have defined is Person.
[07:03] That's why it is inheriting from the Person interface.
[07:06] If I try to change these interface names by swapping Hero first and Person as a second, in this scenario,
[07:14] if you try to look for the list of methods, you can see this time the walk() abstract method is being
[07:19] inherited from the Hero interface.
[07:22] As long as you are interfaces has having the abstract methods with the same name, your compiler is
[07:28] not going to complain anything inside your interface SuperHero, because regardless of which one it
[07:34] is going to inherit, there is no damage is going to happen.
[07:38] But the ideal or graceful approach is you should define the same abstract method inside the SuperHero.
[07:46] For example, I can mention the same abstract method which is void walk(), but it is always advisable
[07:53] to mention @Override to convey to others who are trying to understand your interface, saying
[07:59] that that these abstract method is being inherited from other interfaces like Hero and Person.
[08:05] If you try to hover on this method, you will be able to see that these method is being override from the
[08:11] interfaces Hero and Person.
[08:13] I hope you are clear about these first scenario.
[08:16] Now as a next step, I am going to change one of the walk() method available inside the super interfaces
[08:23] as default.
[08:24] For example, inside Hero, I can change this walk() method as an default method, and inside this default
[08:32] method I'm going to have System.out.println() with a statement walking post this
[08:38] if I go to my SuperHero interface and remove this code which we have written previously, this time
[08:44] I'm going to get a compilation error saying that there is an ambiguity to your compiler.
[08:49] It is not sure whether to inherit the default method from the Hero, or the abstract method from the
[08:56] Person.
[08:57] To resolve this ambiguity, like we discussed, we can follow the previous approach, which is defining
[09:03] the same abstract method with the @Override annotation.
[09:07] So this is one of the basic approach, whereas the second approach is to override the default method
[09:14] with your own business logic.
[09:16] Maybe I can try to have a print statement saying that SuperHero is walking.
[09:23] So this is the second approach.
[09:24] Instead of having the custom logic, the other approach you can follow is you can try to invoke the
[09:31] super default method itself with the help of the statement like what is your interface name, super
[09:37] keyword followed by your default method which is walk().
[09:41] So this is the third approach that we can use to resolve this ambiguity.
[09:44] This time I'm going to define the same walk() method as a default method inside my Person interface as
[09:52] well, even in this scenario
[09:53] also, if I don't have these logic inside my SuperHero, my compiler is going to
[09:59] throw an error saying that I have an ambiguity and I'm not sure which default method to inherit.
[10:05] So to resolve this error, we can follow any of the three approaches that we discuss.
[10:10] The very first approach is we can directly override the method in an abstract way, like I can simply
[10:18] mention void walk().
[10:20] So this is one of the most basic way.
[10:22] The other approach is, you can override the default method itself.
[10:27] And inside the default method you can try to invoke the walk() method present inside the Hero or inside
[10:33] the Person
[10:34] or instead of invoking the walk() method inside the super interfaces, you can write your own business
[10:40] logic as well.
[10:41] So anything is going to be perfect for your compiler.
[10:44] I hope you are clear with the three solutions that we have discussed.
[10:47] These three solutions you can use whenever you are having abstract methods
[10:53] conflict from your super interface inside an interface, or a combination of abstract default methods
[11:00] or two default methods.
[11:02] In all these three scenarios, you can follow any of these solution that you are seeing on the screen.
[11:08] I hope you are clear.
[11:09] Let's try to discuss about more scenarios in the next lecture as well.
[11:14] Thank you,
[11:14] bye.

----------------------------------------
