# 22.7 — Associating Data to Enum Constants

> Section 22: Enums in Java

[00:00] As of now, when we create the constants with the help of enum datatype, we are only giving a name
[00:06] to the constants like low, medium, high and urgent.
[00:10] But if needed, we can also associate a data or a value for a given constant.
[00:16] For example, I can associate a data to the low constant, saying that a low priority task can be closed
[00:22] within seven days.
[00:24] For medium, we can associate a data like five days for high
[00:27] we can associate a data like two days for urgent
[00:31] we can associate that data like one day.
[00:33] The advantage that we are going to get if you try to associate a data to a enum constant is other developer
[00:40] they don't have to rely on the utility logic to calculate the number of days to handle a task with a
[00:47] given priority.
[00:47] As of now, if you check our class, which is TaskUtil, we have a static method which is accepting
[00:54] the PriorityEnum as an input.
[00:57] And here inside this method we have written a switch expression inside the switch expression
[01:02] using the enum constant, we are trying to return the number of days as an output, like for low task
[01:08] seven, followed by five, three, and one.
[01:11] But we can avoid invoking this method by directly associating the data to a given enum constant.
[01:18] Let me show you how to do that inside this lecture.
[01:21] For the same, I'm going to copy the PriorityEnum class inside the same package.
[01:26] The new name that I'm going to give here is Advanced PriorityEnum, because this is more advanced compared
[01:32] to the basic PriorityEnum that we have created previously.
[01:36] Now inside this enum data type I'm going to associate some data like for low I'm going to associate
[01:43] the value as seven seven indicates seven days.
[01:47] For medium I'm going to associate five days, and for high I'm going to associate data which is two.
[01:54] And at last I'm going to associate one as a data to the urgent constant.
[01:59] If you simply try to associate data to your enum constants, you're going to get a compilation error
[02:04] saying that behind the scenes JVM created only the default constructor.
[02:08] But we are trying to invoke a constructor by passing a parameter as an input.
[02:14] So to resolve this compilation error, we need to create our own custom constructor inside the same
[02:21] Enum class.
[02:21] Before that, let me try to create an instance variable with the name private int and the name to this
[02:28] variable.
[02:28] I'm going to give as estimated completion days.
[02:33] Post that I'm going to create a constructor.
[02:36] Whenever we are trying to create a constructor inside enum, please make sure you are creating a private
[02:41] constructor only.
[02:42] After mentioning private, I need to mention the Enum data type name which is AdvancedPriorityEnum
[02:48] and to this I'm going to accept an input which is int with the variable name as estimated completion
[02:55] days.
[02:56] And inside this constructor I'm going to perform the assignment.
[02:59] this.estimationCompletionDays = estimationCompletionDays.
[03:04] So if you see here I'm getting a warning saying that mentioning modifier private is redundant for enum
[03:09] constructors.
[03:10] Anyway
[03:10] by default all the constructors inside enum they are considered as private.
[03:15] That's why let me remove these private access modifier with these
[03:18] what we are trying to do is, we have created a constructor which which accepts int as an input parameter
[03:25] and the same parameter.
[03:26] We are trying to assign a instance variable inside this enum data type.
[03:30] With the help of this code that we have written here.
[03:33] So now you can see my compilation errors are resolved.
[03:36] Since we have written more code after our constants, it is mandatory to mention semicolon instead of
[03:42] one data.
[03:43] If I try to send multiple data, maybe if I want to send one more string as an input data type like
[03:49] this is urgent.
[03:51] So if I want to send this kind of multiple input data, it's always simple
[03:56] you just have to make sure you have a constructor representing the number of input parameters that you
[04:02] are trying to send.
[04:03] For now, for our use case one input is enough.
[04:06] That's why I'm rolling back the code.
[04:08] As a next step, I need to build a method inside my enum, which someone can invoke by using my enum
[04:16] object.
[04:16] This method should give them how many days it is going to take to complete a given task.
[04:22] Since this method is going to be invoked from other classes, this method access modifier should be
[04:28] public and after the public access modifier, I need to mention int as the return data type post that
[04:34] I can mention the name as get estimated completion days.
[04:39] So you can see this is simply a getter method for my variable estimatedCompletionDays.
[04:44] So inside this method I can simply return estimatedCompletionDays.
[04:49] So now we have an enum data type ready that is capable of holding both a constant name and data against
[04:56] it.
[04:57] As a next step we can see the power of this
[04:59] Enum class by testing it.
[05:01] To test the same, I'm going to create a new Java class with the name AdvancedPriorityEnumTest.
[05:08] Inside this class
[05:09] first I'm going to create the main() method.
[05:11] Inside this main() method, I'm going to build a for each block and inside that for each block.
[05:17] Using the AdvancedPriorityEnum, I'm going to invoke the values() method, which is going to give me
[05:25] the array of AdvancedPriorityEnum constants.
[05:28] That's why on the left hand side, let me create a temporary variable name with the name PriorityEnum.
[05:35] After this, I'm going to mention colon followed by
[05:38] Inside this
[05:38] for each block, I can fetch details based upon an Enum object.
[05:43] During each iteration, the Enum object is going to be represented with these PriorityEnum variable
[05:49] name.
[05:49] Using the same object variable, I'm going to invoke the name() method, and with that we should be able
[05:55] to get the name value.
[05:57] After that, we can also get the oridinal value by invoking the original method.
[06:03] Now the fun part comes here.
[06:05] If someone want to understand how many days it is going to take to resolve a task based upon the priority,
[06:11] they don't have to worry much.
[06:13] They can simply invoke the method that we have written, which is getEstimatedCompletionDays.
[06:19] On the left hand side, I can try to catch the output with the variable name as int days.
[06:24] Now I can try to print out all these content with the help of System.out.println().
[06:30] I'll just mention inside the string saying that name is equal to plus name.
[06:36] After that I'm going to mention a String with the value comma followed by ordinal is equal to and and
[06:44] after this is equal to.
[06:45] I'm going to append the variable ordinal.
[06:48] Post that I'm going to press enter and append the String which is comma days is equal to
[06:56] to this String I'm going to append the variable which is days.
[06:59] If I execute this program, you'll be able to see the complete information.
[07:03] What is the name of the constant like low?
[07:05] What is the oridinal and how many days it is going to solve to handle a task with the given priority?
[07:11] The same applies for remaining priorities as well.
[07:14] This way
[07:15] now the other developers, they don't have to rely on the utility logic that we have written.
[07:19] They can simply get an instance of an enum constant and using the same instance object, they should
[07:25] be able to invoke these methods like getEstimatedCompletionDays, ordinal and name.
[07:30] This approach
[07:31] is also going to give you a flexibility which is in future if you are trying to add more constants
[07:37] with the more data associated, you don't have to change any logic inside your TaskUtil, because we
[07:44] are no more going to depend on this logic.
[07:46] I hope this makes sense to you, and you are clear on how to associate data to an enum constant.
[07:52] The example that we have discussed, along with the explanation I have mentioned inside this slide for
[07:57] your reference.
[07:58] Thank you and I'll catch you in the next lecture,
[08:00] bye.

----------------------------------------
