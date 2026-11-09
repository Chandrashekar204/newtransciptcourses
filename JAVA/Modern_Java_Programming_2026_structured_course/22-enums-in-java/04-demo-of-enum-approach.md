# 22.4 — Demo of Enum approach

> Section 22: Enums in Java

[00:00] Before we try to implement our business logic with the help of Enums.
[00:05] First, let me give you a short introduction about Enums and how to create them.
[00:10] As per the dictionary definition, the term enumerate means to specify one after another.
[00:17] The enum type that we have inside Java precisely does the same.
[00:21] It is going to allow the developers to specify constants in a particular order.
[00:26] Whatever constants that we are going to define within the enum type is going to act as instances of
[00:33] that specific enum type.
[00:35] Whenever we want to define an enum type inside Java, it's very easy.
[00:39] You need to use the keyword enum like you can see here.
[00:42] This is the syntax.
[00:44] First you need to mention what is your access modifier followed by enum.
[00:48] Usually for a Java class or an interface, we mention the keyword as class or interface, whereas for
[00:54] the enum we need to use the keyword enum followed by what is that name of your enum type and post that
[01:01] inside the body of the enum type, we can define any number of constants which are separated by comma.
[01:08] The access modifier that we have inside the syntax.
[01:11] It is going to work similar to a Java class
[01:13] or an interface, we can use public, private, protected or default based upon our business requirements
[01:21] and coming to the enum type name, it should be a valid Java identifier.
[01:25] You should follow the same naming conventions that you're going to follow for a Java class and Java
[01:31] interface, and coming to the body of the enum type within the braces, you can define constants, methods,
[01:38] constructors, instance fields, static methods, and instance methods.
[01:43] Your enum type
[01:44] also, it is going to work very similar to a normal Java class.
[01:48] You can define all kinds of members inside it, but majority of the time developers they will define
[01:54] enums to declare only the constants.
[01:56] Here is an example of an enum.
[01:59] The enum type name is PriorityEnum.
[02:01] Inside this enum type, we are trying to store four different constants like low, medium, high and
[02:08] urgent.
[02:09] Do you see how simple and compact it is?
[02:11] We don't have to define public static final because by default all the constants inside the enum, they
[02:18] are implicitly final, and we don't have to assign a value as well for our constants by default, whatever
[02:24] name we are giving to our constant, the same is going to be considered as a value.
[02:29] As a standard, we should define enum constants in completely uppercase letters.
[02:36] We follow the same standard even for normal Java constants as well.
[02:39] Coming to the semicolon that you see at the end, it is going to be optional if you don't have any other
[02:45] code inside your enum file other than constants.
[02:49] Now using this knowledge, let's try to create the enum and using the same enum, we can update the
[02:55] business logic inside that task util file.
[02:58] Inside my IntelliJ, I'm going to create a new Java enum type for the same
[03:04] inside this pop up window, you need to select the enum as an option.
[03:08] Post that I'm going to give the name to my enum type as PriorityEnum.
[03:14] Since we already have a Java class with the name Priority,
[03:16] just to avoid some confusion, I'm trying to give the name as PriorityEnum.
[03:21] As soon as I press enter, you can see we have the keyword enum here with a public access modifier.
[03:27] Inside these enum type, I'm going to create four different constants, which is low followed by comma
[03:35] medium.
[03:36] After medium I'm going to mention comma followed by high comma followed by urgent.
[03:42] And at last mentioning the semicolon is completely optional.
[03:46] That's why you can see I'm getting a warning saying that unnecessary semicolon.
[03:50] So let me remove this.
[03:51] Did you see how simple it is to create the constants, or to define the constants with the enum compared
[03:56] to the traditional approach where you need to type all this code and we need to assign some values as
[04:01] well to those constants.
[04:03] All these kind of lengthy code we can avoid with the help of enums.
[04:07] Your fingers is going to love you because you are saving them from typing a lot of code.
[04:12] As a next step using these PriorityEnum, I'm going to update that TaskUtil class.
[04:18] So here instead of into priority, I need to accept the PriorityEnum as an input. Post that you can
[04:26] see I'm getting a compilation error to resolve this compilation error.
[04:30] What I can do is, I can mention the enum class name which is PriorityEnum.Low.
[04:37] Similarly, let me replace them in the other places as well.
[04:40] And at last, whenever we are using the enums, we can avoid the default branch.
[04:46] You can see I'm also getting a warning saying that default branch is unnecessary.
[04:50] The reason why default branch is unnecessary in the case of enums, is no one who is trying to invoke
[04:56] these method.
[04:57] They will not be able to send the input
[05:00] to this method other than these values that you have defined inside the enum.
[05:05] For example, inside this class here I can send the low priority by using the PriorityEnum.Low.
[05:14] Similarly, whenever I want to send high, I need to do the same.
[05:18] I need to type PriorityEnum.High and at last and after high I can mention PriorityEnum.High.
[05:27] Here I have mentioned High.
[05:29] It's a mistake.
[05:30] So let me mention medium and at last I can mention urgent as well.
[05:34] If you see the beauty of enums, if someone is trying to send other than your valid enum values, they
[05:40] are going to get a compilation error like this.
[05:42] With this, we are stopping the invalid data at the compilation time itself.
[05:48] There is no need to write dirty code inside your business logic to handle invalid data, and there is
[05:54] no need to throw the runtime exceptions.
[05:56] Everything is going to be simple and clean.
[05:58] So if I execute this program, you're going to get the same kind of output.
[06:03] And at the end, instead of Priority.Urgent, I'll try to print out PriorityEnum.Urgent.
[06:12] So let's see what value we are going to get.
[06:14] You can see the same is being printed as a value.
[06:17] So that's a beauty of enum.
[06:19] So these values like 7, 5, 3, 1 those are getting returned based upon the logic that we have returned inside
[06:25] the switch expression.
[06:26] Let me show you one more beauty of enum here.
[06:29] Since you already mentioned the input for these method as PriorityEnum, you don't have to use the
[06:35] complete qualified name of your constant.
[06:37] Instead, you can simply mention unqualified name like Low.
[06:42] So let me remove PriorityEnum in the other places as well.
[06:46] With this, your code is going to look even more compact.
[06:50] I'm trying to show you a demo with the help of switch expression, but please note that it is not mandatory
[06:54] that you need to use enums only with the switch expressions.
[06:57] You can use these enums anywhere inside your business logic, like inside normal if loops or inside
[07:04] normal business logic that you are going to write with the help of Java statements.
[07:09] I hope you are clear on how to create enums and how to use them.
[07:13] And in the same process, I'm assuming you are appreciating the enums feature compared to the traditional
[07:19] Java constants approach.
[07:21] The examples that we have discussed I also highlighted in this slide.
[07:25] So I'm trying to give two different examples.
[07:27] One is with the help of traditional switch statement and the second example using the switch expression.
[07:34] Regardless whether you are using the traditional switch statement or switch expression, the usage of
[07:40] enums is going to be same, and the advantages provided by your enum are also going to remain same.
[07:46] We need to discuss more about enums, so let's try to continue that discussion around enums in the next
[07:52] lecture as well.
[07:53] Thank you,
[07:53] bye.

----------------------------------------
