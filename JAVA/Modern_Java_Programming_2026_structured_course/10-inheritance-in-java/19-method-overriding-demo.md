# 10.19 — Method Overriding - Demo

> Section 10: Inheritance in Java

[00:00] Let's see that demo of method overriding inside this lecture.
[00:04] As of now, we already did a lot of method overriding in the previous lecture.
[00:10] For example, if you go to the Dog class, we are already doing a overriding of the eat() method, which
[00:17] is inherited from the Animal class.
[00:19] But now let's try to discuss more formally, because right now we are aware about the concept of method
[00:26] overriding for the same,
[00:28] let me go to the Person superclass.
[00:30] Inside my Person superclass I have a method with the name public void walk().
[00:37] So inside this method I have a logic which is Person is walking and this logic is not going to make
[00:43] any sense to the IronMan.
[00:44] That's why I'll go to the IronMan subclass which is present inside the heroes package.
[00:51] Here I'm going to override the method of walk(), which is inherited from the Person superclass for the
[00:58] same,
[00:59] first I need to mention @Override annotation.
[01:03] So this annotation is present inside the java.lang package, followed by
[01:09] I'm going to type the same method definition like public void walk() post that I'm going to mention curly
[01:19] braces.
[01:19] Inside the curly braces, I'm going to have a System.out.println() statement and to the println()
[01:27] method.
[01:27] I'm going to pass a String data, which is IronMan walking with his suit.
[01:34] So this is what I want to build inside the walk() method of IronMan.
[01:39] So if you see here I have to follow the same method, signature and method details like the return type
[01:45] has to be the same and the method name has to be same
[01:48] and the method parameters also has to be same.
[01:51] So here I don't have any method parameters.
[01:53] If I try to be oversmart and try to use a input parameter which is like String input, then obviously
[02:01] I'm going to get a compilation error saying that you are trying to override a method from its superclass,
[02:07] but it is not exactly the same.
[02:09] So that is what my override compilation error is trying to highlight here.
[02:13] So if I try to remove this @Override annotation, you can see I'm not getting any compilation
[02:19] errors because my compiler is thinking I'm not overriding the method of walk().
[02:25] Instead I'm trying to perform some other operation.
[02:28] So that's why always if you have an intention to override a method from a superclass, please, please
[02:34] make sure you are mentioning these @Override annotation.
[02:38] So as soon as I remove these method input parameter, the error is going to be resolved.
[02:44] Similarly, if I try to change the method name to something else, I'm going to get the compilation
[02:50] error the same.
[02:51] You can also confirm with the return type as well.
[02:54] So here instead of void, if I try to mention String as an return type, I'm going to get a compilation
[02:59] error.
[03:00] So that's why let me roll back to the void coming to the access modifier access modifier
[03:05] always we need to make sure either it is same, or it should not be more restrictive than super method
[03:12] that we are trying to inherit.
[03:14] For example, here we have the restriction or the access modifier as public.
[03:19] But if I try to be more restrictive instead of public, if I try to mention protected, then I'm going
[03:26] to get a compilation error because my super method is public.
[03:31] But inside my subclass overridden method I'm trying to be more strict compared to superclass method.
[03:37] So that's why I'm getting a compilation error.
[03:40] Whereas if you try to keep the access modifier as protected inside your super method, and here if you
[03:47] maintain the public, it is not going to give any compilation error because you're not violating the
[03:53] rule of access modifier.
[03:55] What is the rule of access modifier?
[03:57] When we're dealing with a method overriding, we can change the access modifier as long as we are not
[04:03] more restrictive.
[04:04] In this scenario, I'm not trying to be more restrictive.
[04:06] Instead, I'm trying to be less restrictive because right now my overridden method is of type public.
[04:14] I hope you're clear, but most of the times you will end up maintaining the same access modifiers in
[04:21] both the parent method and the subclass method.
[04:24] So that's what I'm trying to follow here as well.
[04:27] I hope you are clear
[04:28] with the process of method overriding, there are certain rules that you need to be aware whenever you
[04:34] are trying to deal with the method overriding.
[04:36] So let me share those rules and regulations very quickly in a slide.
[04:41] So these are the six rules that you need to follow.
[04:43] The rule number one says the method must be an instance
[04:47] method, overriding does not apply to the static methods.
[04:50] Like we discussed
[04:51] the overriding method in the child class must have the same name and the arguments as a method in the
[04:57] parent class.
[04:58] But please note that the
[05:00] name of the parameter does not matter, which means if your superclass has a method which has a input
[05:06] parameter with the name age() inside your subclass, you can change the parameter name to something else.
[05:13] So the parameter names are not mandatory to maintain with the same names as superclass, but we need
[05:19] to make sure the data types of the parameters and the order of the parameters is always same as a superclass
[05:26] method coming to the rule number two.
[05:28] The return type of the child method can be same, or a subclass of the return type of the parent method.
[05:35] Think like the method present inside the superclass or parent class is returning an object of type Animal.
[05:42] Now inside your subclass overridden method
[05:45] you can either follow the Animal or the subclasses of Animal as return type.
[05:50] For example, you can mention Dog or Cat as well, so that is completely allowed as per the rule number
[05:56] two.
[05:57] Coming to the rule number three only inherited methods can be overridden.
[06:01] This is obvious because the method overriding concept comes in the scenario of inheritance only.
[06:07] The rule number four says constructors, private and final methods cannot be overridden, as they
[06:14] are never going to be participate in the inheritance process.
[06:18] Moving on to the rule number five, we already discussed the access modifier of the child method can't
[06:24] be more restrictive than the access modifier of the parent method.
[06:28] For example, if the parent method is protected, then using the private in the child's overridden method
[06:35] is not allowed.
[06:36] We also saw the demo of this rule number five just a few seconds back.
[06:40] Now moving on to the rule number six.
[06:42] It is not going to make sense to you right now because this is related to the exceptions.
[06:47] But still I will try to explain this.
[06:49] So once we discuss about the exceptions in the Java, you can come back and look at this rule number
[06:55] six.
[06:56] Then it is going to make more sense to you.
[06:58] This rule number six is the overriding method is not allowed to introduce any new checked exceptions
[07:06] to the set of checked exceptions specified in the parent method.
[07:09] So your parent method may throw multiple checked exceptions so you are overridden
[07:15] method can accept the same checked exceptions, but it is not allowed to introduce any new checked exceptions
[07:22] as part of the method definition.
[07:24] And at the same time, your subclass also has the flexibility to eliminate one or all checked
[07:30] exceptions are substituted and checked exception with another checked exception that is a descendant
[07:38] of the checked exception listed in the parent method.
[07:41] This means if your parent method is having two checked exceptions, then your subclass has an option
[07:47] of following the same two checked exceptions, or it can remove completely two of them, or it can maintaining
[07:53] only one of them, or it can remove all of them
[07:56] or it can also change to some other checked exceptions.
[07:59] But whenever it is changed to the some other checked exceptions, it needs to make sure that the new
[08:05] checked exception that it is trying to add it is a descendant of the checked exceptions defined in the
[08:11] parent method.
[08:12] I hope it is making sense to you.
[08:14] If it is not, don't worry
[08:15] like I said, once we discuss everything about the exceptions and checked exceptions inside Java, then
[08:21] it is going to make more sense to you.
[08:23] With this, I'm assuming you are super clear about how to perform the method overriding inside Java,
[08:29] and what are the rules and guidelines that you need to follow.
[08:32] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
