# 11.6 — Constant Field Declarations in interface

> Section 11: Interfaces in Java

[00:00] As of now, inside our interfaces, we just declared the abstract methods.
[00:05] Apart from abstract methods, we can also declare constant fields inside interfaces.
[00:11] So whenever you are trying to declare a constant value inside an interface, it is going to be by default
[00:19] public static and final.
[00:21] That means you don't have to mention public static final.
[00:25] For example, like you can see here, I have two different examples where I'm trying to create the same
[00:31] constant, which is UNIVERSE_NAME.
[00:34] On the left hand side example, I'm trying to mention public static final before my constant declaration,
[00:41] whereas on the right hand side I simply mentioned String UNIVERSE_NAME as MARVEL
[00:46] So both of these examples, they are going to be work very similarly because like I said, inside interfaces,
[00:54] all your constants, they are going to be implicitly public, static and final.
[00:59] So whenever we define a constant inside an interface, we can access these interfaces with the help
[01:05] of interface name.
[01:07] So please note that we can only define a static fields inside interfaces.
[01:12] We will not be able to define instance variables inside interfaces because the interfaces are mean to
[01:20] be defined a contract a specification, but they are never meant to be to create an object from them.
[01:26] That's why the instance variable declarations inside interfaces is not allowed.
[01:31] And since by implicitly, every static field that you're going to create inside interface is final,
[01:38] you will not be able to change the value of these constant values at later point of time.
[01:44] So whenever you are trying to declare during the same time, you should also assign an initialize value.
[01:50] And this initialize value is going to be final forever.
[01:54] If you try to change this initialized value at later point of time, it is not going to work because
[01:59] all the constants that we define inside an interface, they are going to be final.
[02:04] On top of that, if you are trying to simply declare an constant without initialization, it will also
[02:10] not allowed and it may result into compilation error.
[02:13] For example, here I have a variable name which is UNIVERSE_NAME.
[02:18] I'm trying to do only the declaration, but not the initialization.
[02:21] That's why I'm going to get a compilation error.
[02:24] The next important point that you need to be aware here is, whenever you are trying to define constant
[02:30] fields inside an interface, please make sure you are mentioning the variable name in all uppercase
[02:36] letters, and each of the word inside your variable can be separated by an underscore value.
[02:42] Following this naming convention is only optional.
[02:45] Java is not going to enforce this specific naming convention rules, but I would always recommend you
[02:50] to follow this naming convention.
[02:52] So what is this naming convention called?
[02:54] It is called as snake case Naming convention, where we can mention all the letters or characters inside
[03:01] a word in completely capital letters, and each word can be separated with the help of underscore.
[03:07] The next rule that you need to be aware is, interface
[03:10] fields are always public, but their accessibility from outside the declaration package depends on the
[03:17] interface scope.
[03:18] For instance, if an interface has a package level or default scope, then in such scenarios the interface
[03:25] fields won't be accessible outside the package, even though the fields themselves are public.
[03:31] So if you want to make your interface constant to fields to be accessible by everyone across all the
[03:37] packages, then you need to make sure you are declaring your interface with a public access modifier.
[03:43] I hope you are clear with this theory discussion.
[03:45] As a next step, let's try to create an constant field inside an interface with the help of IntelliJ.
[03:52] So here inside my IntelliJ, I'm going to create an constant by mentioning public static final String,
[04:00] followed by constant name, which is UNIVERSE_NAME.
[04:05] And to this I'm going to assign the value which is Marvel.
[04:09] You can see there is a warning saying that this public static final, they are not needed or they are
[04:16] redundant, since by default every constant inside interface is going to be considered as public static
[04:23] final.
[04:23] That's why I would always recommend you to remove these public static final to avoid the warnings inside
[04:29] your class.
[04:30] So now let's try to understand how these constant value is going to be inherited by the implementation
[04:37] classes.
[04:37] So if I can go to one of the implementation class which is IronMan, here I can see the list of methods
[04:44] and constants available.
[04:45] You can see my implementation class
[04:48] it is able to inherit the UNIVERSE_NAME
[04:51] static constant field available are declared inside the SuperHero interface.
[04:56] The same I can see here as well.
[04:58] Now let's try to access
[05:00] same from the IronMan class.
[05:02] Think like I have a requirement to access the interface static field from this use power method of IronMan.
[05:08] .
[05:09] Let's try to understand how to access the same.
[05:11] So I want to access the same and and print the same
[05:14] whenever this usePower() method is invoked, I can directly invoke the universe name by simply mentioning
[05:20] the constant name.
[05:22] So this is perfectly allowed because my implementation class inherited this variable from the SuperHero
[05:29] interface.
[05:30] Whereas if I try to access from a class where there is no inheritance involved in such scenarios, if
[05:36] you want to access the static final variable available inside an interface, then you should definitely
[05:42] use the interface name followed by what is your constant name?
[05:47] So this is how you need to invoke.
[05:48] So let me try to execute this program and see whether we are able to see in the output.
[05:53] You can see we're able to see the Marvel output two times one from this statement,
[05:58] and the second one is from this statement.
[06:00] When we are invoking this usePower() method using the IronMan object.
[06:05] I hope this provides a better clarity for you around the constant fields or the static fields that we
[06:12] can create inside an interface.
[06:14] Like I said, we can only create an static fields inside an interface.
[06:19] Even if I try to declare a normal variable like int num = 6, this is going to be considered
[06:25] as a final and a constant variable because like I said, in interface all the Java fields, they are
[06:31] going to be public static final by default.
[06:35] That's why if I try to simply mention int name, I'm going to get a compilation error saying that it
[06:42] is not initialized because the reason is num is being treated as a final variable inside your interface.
[06:48] I hope this makes sense.
[06:49] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
