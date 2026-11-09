# 22.5 — More details about enum - Part 1

> Section 22: Enums in Java

[00:00] Inside this lecture, let's try to understand more details about the enum.
[00:04] The very first important point that you need to be aware whenever you are trying to use enum inside
[00:10] your Java project is, the constants that you're going to define inside your enum data type.
[00:17] They should be related with each other.
[00:19] For example, all these constants that I'm trying to define here, they are related to a priority of
[00:25] the task.
[00:26] Here if I try to randomly define a constant like male female, these new constants that I'm trying to add,
[00:34] they are nowhere related to the priority.
[00:36] That's why defining unrelated constants in a same enum file is not recommended, and it's considered
[00:43] as a bad approach.
[00:45] The purpose of enum is always to define the constants related to a particular scenario or a concept.
[00:52] Whereas when you're trying to define constants with the help of normal Java class approach, you can
[00:58] define any number of constants.
[01:00] Even you can define 1000 or 10,000 constants belongs to your whole Java application.
[01:06] So that's perfectly possible and acceptable inside Java.
[01:10] But coming to the enum, please define the constants which are related to the a particular scenario.
[01:17] That's why I'm trying to delete these male and female
[01:19] here.
[01:20] Let me show you few more example scenarios in which we can create enums. Like you can see here,
[01:26] if I want to define constants related to a day, then we know day has only a specified set of names
[01:34] like there are total seven days, the same seven days
[01:37] we can try to define them inside the enum data type like you can see here.
[01:42] Similarly, if we're trying to build a business logic related to the size of a t shirt or size of a
[01:47] product, in all those scenarios, you can create one more enum with the name size, and inside that
[01:53] you can have constants like small, medium, large, extra large.
[01:57] Let's try to create these enums very quickly inside IntelliJ.
[02:01] Here I'm going to create a new enum with the name Day.
[02:05] So whenever we're trying to create enough we need to make sure we are selecting the enum option for
[02:10] all the enum data types your intellej
[02:11] it is going to show you the icon as E, whereas for a normal class it is going to show you the icon
[02:18] with the C inside a circle.
[02:20] Now inside this enum data type, let me try to create various constants representing the day.
[02:25] The very first one is MONDAY, followed by THUESDAY, followed by WEDNESDAY.
[02:31] And after Wednesday
[02:32] I'm going to mention THURSDAY, and after Thursday I'm going to mention FRIDAY, which is our favorite
[02:39] day because from Friday evening, the fun of weekend is going to start after Friday
[02:44] I'm going to define SATURDAY, and at last I'm going to mention SUNDAY.
[02:48] So if you see how defined constants related to only that day, I'm not trying to define other constants
[02:56] like MARCH.
[02:57] So the matches belong to the month, but not the day.
[03:00] So this is a unrelated constants.
[03:02] So these kind of constants we should not define.
[03:05] On top of that, whenever you're trying to define the constants inside the enum make sure you are following
[03:11] the order.
[03:11] Like after Monday we get Tuesday, followed by Wednesday, Thursday, Friday, Saturday, Sunday.
[03:16] If you try to put this Sunday in the middle, it's not going to make sense and it is going to be considered
[03:22] as a very, very bad practice.
[03:24] There is a very good reason as well on why we should maintain the order properly behind the scenes
[03:30] each of your constant it is going to have a positional value, which we are going to discuss in the
[03:35] coming lectures.
[03:36] Now let me create one more enum file.
[03:39] This time I want you to pass the video and try to create the enum with the name size, and define all
[03:45] the constants that we have discussed.
[03:46] I hope you are successful, otherwise you can simply follow my discussion.
[03:50] The name I want to give here is Size.
[03:53] Inside the Size enum type I'm going to define constants like SMALL, MEDIUM, LARGE, followed by
[04:02] EXTRA_LARGE.
[04:03] So if you have multiple words inside your constants, please make sure you are separating them with
[04:08] the help of underscore.
[04:09] The next important point that I want to highlight about enums is we can declare the variables of enum
[04:15] type the same way how we declare the variables of a class, data type, or interface data type.
[04:21] On top of that, we can also assign null values as well to the enum variables.
[04:26] For example, here I'm trying to create a enum variable with the name priority, and you can see the
[04:32] data type I have mentioned as PriorityEnum.
[04:35] Similarly, during the declaration, you can also assign the value null to the PriorityEnum variables.
[04:43] So let's try to see the demo of this.
[04:45] What I'm going to do is I'll open my TaskPriorityConstantDemo.
[04:49] And here inside this class maybe I can try to create some class level variables like private PriorityEnum
[04:57] and to these PriorityEnum data type.
[05:00] I'm going to assign the variable name I want to these priorities.
[05:04] So this way is I can define a type for of variable which belongs to the label in PriorityEnum.
[05:10] So this is going to work very similar to the common data type and interface data type.
[05:15] And if need measure I can also assign a get value.
[05:17] What I from there is I'll go to class method and inside any method I'll just create a variable from
[05:23] the with the name PriorityEnum and to
[05:25] the same is to assign the null value.
[05:28] That means null also is a valid value that you can store inside a Enum data type.
[05:34] With that you may have naughty thought here, which is can
[05:37] we send this null as an input to the method that have return. I liked your naughty thought let's
[05:43] try do the same. Here instead of low
[05:45] am going to send the preorityEnum variable as input and I'm not going get
[05:51] any compilation error even inside the TaskUtil as well am
[05:54] not going to get any compailation error.
[05:57] But let's see what is going to happen when we run these class, when I run this we are going
[06:02] to see keyword and surprise output.
[06:05] Let me show you that surprise.
[06:06] you have a NullPointerException.
[06:09] And this is very obvious
[06:11] you are sending a null as input to the
[06:14] TaskUtil method.
[06:15] And since you're trying to send the null object, using Null object switch expression
[06:20] it will try to perform these operations. Like it will look for the low, medium, high and urgent
[06:26] constants.
[06:27] Since it is trying to perform operations on top of a null object, we are going to get a
[06:33] NullPointerException.
[06:33] That's why whenever you are using the enum data type, please make sure you're not passing the null
[06:38] as an input.
[06:39] Even your intelliJ also is trying to warn you.
[06:42] I hope this makes sense.
[06:44] Let me revert back to the previous value which is PriorityEnum.Low.
[06:48] The next important point that you need to aware whenever you are using enum data type is you will not
[06:54] be able to create an object of enum data type.
[06:57] This is very similar to the abstract class and interface.
[07:01] Just like how we can't create an object of interface and abstract class.
[07:05] Very similarly, we cannot create object of enum data type.
[07:10] Let's validate the same inside IntelliJ as well.
[07:13] So here what I'm going to do is, I'll try to type new, and I'll try to invoke the default constructor
[07:19] of the PriorityEnum.
[07:21] And with that you can see I'm getting a compilation error saying that enum types cannot be instantiated.
[07:27] Always your compiler is to stop from creating the objects.
[07:31] So let me revert back to the null.
[07:33] Coming to the next important point.
[07:35] Whenever we are trying to define constants with the help of Java enum, they are going to be static
[07:42] and final implicitly, and each and every enum data type that you are going to create inside your Java
[07:49] project, it is going to internally inherit or extends the Enum class.
[07:55] There is a class with the name Enum inside the java.lang package.
[07:59] The same is going to be extended by all the enum data types that you are going to create inside your
[08:06] Java project.
[08:06] Since your enum data type already extending another class internally, you cannot extend any more class
[08:14] inside your enum data type. But you will be able to implement any number of interfaces apart from defining
[08:22] constants
[08:23] inside enum.
[08:24] We can define normal instance inputs constructors to birds and even in this can write a main() method
[08:31] as well.
[08:31] But majority of the times dev tools they are going to use, which is enums only to define the control
[08:37] bus.
[08:38] They will not trying to create main() method.
[08:40] Now the methods or instance fields, though technically
[08:43] we can use anything just like any other class.
[08:45] It is not recommanded to define other than constants is always go your enum data type.
[08:51] Here you may have question which is, previously
[08:53] we discussed that we cannot create the object of a enum data type.
[08:57] Then what is the purpose of defining the constructors, instance feilds, instance methods.
[09:03] So that might be your question.
[09:04] So let me clarify your question by providing more details.
[09:08] Whenever we define a Enum data type inside a Java project.
[09:13] ineternally during compilation time it is going to be converted into a normal java class with
[09:20] lot of other code. So when a compailer compiles your Enum calss into a normal java class
[09:26] behind the scenes it is going to treat each of your enum constants as an object of the
[09:32] same enum data type.
[09:34] Since it is internally going to create the object of your enum data type based upon your constants, the compiler
[09:40] need constructor.
[09:42] That's why events go to cannot directly create an object of enum data type.
[09:47] Since compiler is going to create the objects behind scenes.
[09:51] We can write the constructors inside the enum data type.
[09:55] I hope this make sense, let's see few of these details inside IntelliJ
[09:59] by looking at the JDK
[10:00] library files.
[10:02] The very first demo I show you here is, here my Day is a enum data type
[10:07] if try to look for the list of methods available
[10:09] inside my Day.java file, you can see there are good amount of inherited methods and majority
[10:17] of them are getting inherited from the Enum class.
[10:20] So let me open any of these method which is inherited from the Enum.
[10:25] You can see Enum.java is present inside the java.lang package and it is an abstract
[10:31] class.
[10:31] It is also implementing other interfcaes like Constable, Comparable and Serializable.
[10:38] Inside this we have so many methods
[10:39] like name(),
[10:40] oridinal(), toString(),
[10:41] hashCode(), equals(), clone().
[10:44] So there are good amount of
[10:45] methods available that's why
[10:47] the same is going to be extend by each and
[10:49] every enum data type that you are going to create inside your java project.
[10:53] Since my Enum data type it is already inherited the Enum abstract class I will not
[10:59] be able to inherit any other class for example here with help of extends keyword
[11:04] I'm trying to inherit a class which is may be think like TaskUtil.
[11:09] You can see am not able extend this because no extends class allowed for Enum.
[11:15] I hope this make sense but coming to the implements we will be able to implement any of interface.
[11:22] Maybe if I try to implement Comparator interface they should not be any problem.
[11:28] It is asking me to implement the methods inside these Comparator interface.
[11:32] That means we can always try to implement inheritance with the help of interfaces inside enum, but
[11:38] not with the normal Java class or a abstract class.
[11:42] I hope you are clear with whatever details discussed inside this lecture.
[11:46] There are more details that we need to discuss about enum, so let's continue the same in the next lecture
[11:52] as well.
[11:53] Thank you,
[11:54] bye.

----------------------------------------
