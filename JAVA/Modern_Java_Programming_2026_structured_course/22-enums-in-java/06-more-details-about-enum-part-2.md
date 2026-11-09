# 22.6 — More details about enum - Part 2

> Section 22: Enums in Java

[00:00] Whenever we are using enums, it is going to serve to specify two crucial aspects.
[00:06] The very first one is constants.
[00:08] With the help of enum constants, we can represent exclusive and permissible values for a given enum
[00:15] data type.
[00:16] Apart from these constants values.
[00:18] Internally, the enum is going to maintain the sequence or order assigned to each of the constant.
[00:25] I'm going to show you a demo about these order and how to check these order in few minutes.
[00:30] Let's try to understand these two important points by taking an example.
[00:34] In the previous lectures, we have created a enum with the name PriorityEnum.
[00:38] Inside these enum we have defined four different constants low, medium, high and urgent.
[00:45] So whenever someone is trying to create a variable of a given data type, they can store these four
[00:50] valid constants or a null value.
[00:52] For example, if I want to store these low constant into a variable of PriorityEnum first with the
[00:59] help of PriorityEnum, I need to invoke the constant with the help of dot operator.
[01:04] With that, behind the scenes my JVM or Java, it is going to give me an object of PriorityEnum, which
[01:12] is going to hold the details of these low constant.
[01:15] Here you can see on the left hand side I'm trying to catch the output with the help of PriorityEnum
[01:20] data type by using a variable name as low.
[01:23] The same applies for medium, high and urgent.
[01:26] Whatever constants that we are trying to create inside an enum data type like low, medium, high and
[01:32] urgent.
[01:33] Each of these constants, they are going to have a name.
[01:36] So what is this name?
[01:37] This name is equal to the same value that you have mentioned as a constant name.
[01:42] For example, for this low constant, its name is going to be low itself, which means behind the scenes
[01:48] this low constant is going to hold a value with the name low.
[01:53] The same applies for medium, high and urgent.
[01:56] When I show you an demo, it is going to make more sense to you.
[01:59] Apart from these constants and names
[02:01] like I said, behind the scenes enums, they are also going to maintain an order for your constants.
[02:07] So this order
[02:08] in other words, we can call it as ordinal based upon the sequence that you have followed while defining
[02:14] the constants inside your enum datatype.
[02:16] Behind the scenes, a ordinal value is going to be assigned to each of your constant right from zero.
[02:23] With that assumption, if you try to calculate the oridinal values for your constants, the very first
[02:28] constant that we have defined low, it is going to get the ordinal
[02:32] or position as zero followed by medium is going to get the value one.
[02:36] For high, we are going to get the original value as two, and for urgent we are going to get the
[02:41] ordinal value as three.
[02:42] Anytime you're trying to add a new constant or remove an existing constant accordingly, the original
[02:49] value is going to be changed behind the scenes.
[02:52] With this discussion, you may have $1 million question, which is how can I validate
[02:57] what is the name for my enum constant,
[02:59] what is the original value assigned to my enum constant?
[03:02] To clear your question, I have a example here.
[03:06] There are good amount of static methods available inside the Enum abstract class, since the same is
[03:12] being inherited internally by each of the enum data type, we should be able to invoke all the static
[03:18] methods once such static method that we can use is values with the help of value() static method,
[03:24] we are going to get an array containing enum constants in the order they are declared within the enum
[03:31] data type.
[03:32] So if someone asks you what are the values or the constants that your enum is going to support, you
[03:38] don't have to provide them by using hard coded values.
[03:42] Instead, you can ask them to programmatically invoke these values() method, which is going to provide
[03:48] an array to them, and the same array can be iterated using for or for each loop, and during the iteration
[03:56] they can invoke methods like name() and ordinal() to understand what is the name assigned to a specific
[04:02] constant, and what is the ordinal array position assigned to a constant.
[04:07] So here I'm trying to invoke these methods and the same I'm trying to store inside the variables name
[04:12] and ordinal.
[04:13] If I try to print out these values with the help of System.out.println().
[04:17] By following these format, I'm going to get the output like you can see here.
[04:21] So for the low constant the name is going to be low followed by ordinal as zero.
[04:26] For medium it is going to be one,
[04:28] for height is going to be two followed by urgent
[04:30] it is going to be three.
[04:31] We can also perform reverse lookup.
[04:33] What do I mean by reverse lookup?
[04:35] If you know a constant name or its oridinal value or its position value, you should be able to get
[04:41] the object of a enum constant or its details.
[04:44] With the help of these valueOf() static method, you can see to this valueOf() static method.
[04:50] I can pass a String name which is low and the left hand side
[04:54] I'm going to get an PropertyEnum object, which is going to hold the details of low
[04:59] constant.
[05:00] Whereas if you are trying to get the enum constant details based upon the original or based upon the
[05:05] position, first you need to invoke the values() method, which is going to give the array on top of that
[05:11] array
[05:12] you can specify the index which is two, and with that we are going to get the third element inside
[05:18] the array which represents high priority.
[05:20] So this concept we call as reverse lookup because we are trying to get the enum constant objects by
[05:27] providing their values like name and position.
[05:29] Let's try to see the demo of these methods very quickly
[05:32] inside IntelliJ. Inside IntelliJ I'm going to create a new Java class with the name
[05:41] InternalEnumMethodsDemo.
[05:42] Inside this I'm going to write a main() method followed by
[05:46] I'm going to build a for each block inside this
[05:50] for each block
[05:51] first I'm going to invoke the PriorityEnum, and using this I'm going to invoke the value() static method.
[05:59] So the return type of this value static method is an array of PriorityEnum.
[06:04] On the left hand side
[06:05] I need to make sure I'm creating a temporary variable name with the name PriorityEnum.
[06:11] For that I'm going to mention semicolon.
[06:13] Now I'm going to mention the curly braces.
[06:15] Before I try to write the logic, let me open these values() method.
[06:19] You can see it is redirecting me to the PriorityEnum data type.
[06:24] I'm not allowed to see the code that is going to be generated internally by my Java or JVM, but we
[06:31] should be able to easily invoke these methods.
[06:34] That's what I'm trying to do here.
[06:35] Now using this PriorityEnum variable, first I'm going to get the name of the constant by invoking
[06:42] the name() method.
[06:44] So this is a instance method which we can invoke using the object of your enum data type.
[06:49] If I try to open this, I will be able to see a method which is present inside the Enum abstract class.
[06:56] In the similar lines, let me try to invoke one more method, which is ordinal.
[07:01] So this is going to give me the ordinal value as an int.
[07:05] That's why on the left hand side I'm trying to mention the code which is int ordinal.
[07:09] If I open this original method, you can see this also present inside the Enum abstract class.
[07:14] As a last step inside this, for each block, I'm going to write a System.out.println().
[07:20] First I'm going to print the name of the constant, followed by
[07:23] I'm going to mention a String.
[07:25] Inside this String, I'm going to mention the open bracket, followed by
[07:30] I'm going to print the oridinal value, and at last I can mention the String which is close bracket.
[07:36] Now, if I try to execute this program, you will be able to see the output like low, medium, high
[07:42] and agent along with their original values.
[07:45] So this should give a confirmation to you whatever value that you have mentioned for your constants
[07:50] inside enums, the same is going to be considered as a name and the logic for oridinal
[07:54] you already know whatever sequence that you have followed here.
[07:58] The same is going to be considered like first constant
[08:01] it is going to have zero followed by one, two, three.
[08:04] Now let's try to perform the reverse lookup.
[08:06] What I'm going to do is, with the help of PriorityEnum data type, I'm going to invoke the valueOf()
[08:12] method.
[08:13] To this valueOf() method, we need to pass the String representation of our constant.
[08:17] Here I'll try to pass the low as a String value.
[08:21] With that
[08:21] on the left hand side, we can catch an object of type enum.
[08:27] So the variable name
[08:28] I'll just give it as low post that
[08:30] I'm going to print out the low object and see what is going to present inside this low object.
[08:36] I can also keep a breakpoint here.
[08:38] Let me debug this program.
[08:40] Inside the console you can see I'm able to see the name of my constant which is low.
[08:46] But if I try to open this low object and try to understand what is there, the name is low and we can
[08:53] see the name has a value low, oridinal is zero and the hash is zero.
[08:57] As a next step, let me release this breakpoint and this time I'm going to invoke one more method which
[09:03] isValues().
[09:04] So when we are invoking the values we are going to get an array.
[09:07] If you are trying to get an Enum object that has ordinal as two, we are going to get a high constant
[09:15] Enum object as an output on the left hand side.
[09:18] So that's why on the left hand side, let me type PriorityEnum with the variable name as high and post that
[09:24] if I try to print out the high object this time, you should be able to see the high as a name inside
[09:30] the console.
[09:31] So this way you can always perform the reverse lookup as well whenever you are using the enum.
[09:37] So anytime, if someone has questions around your enums and their constants and their ordinal values,
[09:43] you don't have to worry much.
[09:44] You just tell them that there are methods inside enum API which they can use to know more details about
[09:51] your constants.
[09:52] For example, if your enum has 100 different constants, you don't have to provide them manually.
[09:57] You can simply ask them to invoke this
[09:59] values() method and iterate them with the help of the logic that we have written.
[10:03] So these kind of flexibility are not going to get if you define the constants with a normal Java class.
[10:09] Before I try to close this lecture, let me highlight you that we can create nested enum types as well.
[10:15] If needed, you can create an enum data type within a class or an interface, or another enum data type.
[10:23] Whenever you are trying to define a nested enum data type, they are going to be considered static implicitly.
[10:30] Regardless, you are trying to mention a static keyword or not inherently, all your inner enum data
[10:36] types are going to be considered static.
[10:38] Since these nested enum data types are static in nature, we cannot declare them as local enum types.
[10:46] Let me show you a demo around this.
[10:48] First, I'm going to create a class with the name Car.
[10:52] Think like
[10:53] inside this class we want to create an inner enum data type that holds the valid constants are valid
[10:59] values for the Car model.
[11:01] For the same, I'm going to type public enum followed by model and inside these enum body I can define
[11:09] the enum constants.
[11:11] For example, I can mention SEDAN, SUV, HATCHBACK.
[11:17] With this we have an inner enum data type within the class.
[11:21] Like I said before, regardless you're trying to mention static or not inherently.
[11:27] Each of the nested enum data type it is going to be considered as static only.
[11:32] That's why you can see I'm getting a warning saying that modify static is redundant for inner enums.
[11:37] So let me remove this
[11:38] So since your inner enums are static, you cannot create local enum data type.
[11:43] I hope you are clear with all the important points that we have discussed around enums.
[11:48] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
