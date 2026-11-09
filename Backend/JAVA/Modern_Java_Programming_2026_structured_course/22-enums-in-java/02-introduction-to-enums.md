# 22.2 — Introduction to Enums

> Section 22: Enums in Java

[00:00] Welcome to the new section.
[00:02] Inside this section we are going to talk about a new topic which is Enum. Inside Java
[00:08] whenever we are trying to create a data type, we have various options.
[00:12] We can create a class, interface and similarly we have other options as well.
[00:17] Let me show you all the options that we have here inside my project with the name
[00:22] section_22.
[00:23] I'm trying to create a new Java class.
[00:26] If I select these, you can see apart from Java class which is the default selected option, we should
[00:33] be able to create Interface, Record, Enum and Annotation.
[00:38] As of now we discussed everything about class, interface, record and annotation.
[00:44] We only left with the Enum.
[00:46] As of now we have not discussed anything around Enum.
[00:49] That's why we are going to talk in detail about Enum throughout this section.
[00:54] So what is an Enum?
[00:55] Let's try to understand the same inside this lecture.
[00:58] Inside Java Enum
[00:59] also referred to as Enumeration or Enumerated data type.
[01:04] Using these Enum, we can define a organized list of constants in a specified order.
[01:12] This Enum feature introduced inside Java 5.
[01:16] As of now, the minimum Java version that you can use is Java 8.
[01:20] With that, every Java developer and every Java project, they are going to have this feature inside
[01:25] their code base.
[01:26] I know it may not be super clear for you, based upon the definition that I have provided to understand
[01:32] enums better.
[01:33] First, let's try to take a scenario and try to build the same without enums and with enums in the same
[01:40] process, we can appreciate the benefits provided by the enum.
[01:45] The scenario that I'm trying to take here is we are going to build a business logic, which is going
[01:50] to accept a task priority as an input based upon the priority of the task.
[01:55] My method or my business logic has to return within how many days a particular task can be expected
[02:02] to close.
[02:03] For example, we are going to have priorities like low, medium, high and urgent.
[02:08] For low tasks, the business logic has to return seven days as an output, whereas for medium it is
[02:13] going to be five, and for high it is going to be two, and for urgent it is going to be within one
[02:18] day
[02:19] the task is going to be addressed.
[02:20] So these are logic that we are trying to build.
[02:23] First, let's forget about enums and try to solve this problem by using normal Java classes.
[02:30] Since we are into the new section, I have created a new Java project with the name section_22.
[02:35] .
[02:36] Inside this project, I'm going to create a new package with the name com.eazybytes.enum.
[02:45] Since I can't use the enum as part of the package definition, maybe I can mention enumeration as a
[02:52] package name.
[02:53] Inside this new package, I'm going to create a new Java class with the name Priority.
[02:59] Inside this class we are going to create four different constants representing the four different task
[03:07] priorities that we have discussed.
[03:08] Like we discussed in the previous sections, we have to follow certain standards whenever we are trying
[03:13] to create a constant files.
[03:15] The standard is we need to type public followed by static, and we need to make sure we are creating
[03:21] the constant as final so that no one can change the value inside it.
[03:25] After this, I'm going to mention that data type of my constant, which is int followed by
[03:31] I'm going to mention low as a constant name.
[03:33] Since this is a constant variable name, I need to make sure I'm using uppercase letters post that I'm
[03:39] trying to assign a value to this low constant.
[03:43] So whenever someone is trying to send the value zero, I'm going to consider that as a low priority
[03:49] task.
[03:49] Similarly, let me try to create few more constants.
[03:53] The next constant that I want to create here is medium.
[03:56] For this medium, I'm going to assign the value as one, followed by I'm going to create high constant,
[04:03] and to this the value I'm going to assign is two.
[04:06] And at last I can create one more constant with the name adjacent to this constant I'm going to assign
[04:13] the value three.
[04:14] So based upon these four constants.
[04:16] Now I need to write a business logic which is going to accept these task priority as an input and return
[04:23] the total number of expected completion days to address a given task.
[04:29] To build the logic, I'm going to create a new Java class.
[04:33] The class name is TaskUtil because inside this I'm going to write a utility logic related to my task.
[04:40] Inside this class, I'm going to write a method which is public static int followed by a method name
[04:49] which is getEstimatedCompletionTime().
[04:55] So this is the method name.
[04:56] And this method is going to accept an int
[05:00] datatype as an input.
[05:01] The parameter name I can give as priority, and inside this method we can use if blocks or switch blocks
[05:09] to return the estimated completion time based upon the task priority.
[05:13] What I can do here is,
[05:14] here I'm going to return the switch expression for the same.
[05:18] First let me type return followed by switch to this switch expression
[05:22] I'm going to pass the priority as an input.
[05:25] Now inside the switch expression I'm going to handle various cases.
[05:29] The very first case that I want to handle is low priority tasks.
[05:33] That's why after case I'm going to mention zero which represents my low priority task.
[05:39] After zero I need to mention this symbol followed by seven, which indicates for the low priority task,
[05:46] we are going to return seven days as an output.
[05:49] Similarly, let me try to copy this code multiple times and this time for the medium priority.
[05:56] I'm going to return the output as five, followed by for high priority
[06:00] I'm going to return the number of days as three and a class for agent priority task, which is three.
[06:06] I'm going to return the number of days as one. So we are getting a compilation error saying that we
[06:12] have not covered all the possible input values.
[06:15] We can try to insert a default branch which is going to throw IllegalStateException.
[06:21] You can see this is a simple switch expression which is accepting my priority as an input value, and
[06:27] it is returning the estimated completion time in number of days as an output.
[06:33] Instead of hard coding these values like zero, one, two, and three, what we can do is we can refer
[06:39] the constants directly. Here instead of zero
[06:41] I can mention Priority.LOW.
[06:45] Similarly, I can also mention for other constants as well.
[06:48] Here instead of low, I can mention medium followed by instead of two
[06:53] I can mention high followed by instead of three
[06:56] I can mention urgent.
[06:59] So the advantage that I'm going to get if I directly mention these constants instead of hard coded values
[07:04] is, in future
[07:05] if I'm trying to change this value from zero to some other value, then I need to change only in this
[07:11] place.
[07:11] And I don't have to change here because I'm trying to refer the constant present inside the Priority
[07:17] class.
[07:17] Now we have our business logic ready.
[07:19] As a next step, let's try to see the demo of this task util method that we have created.
[07:24] For the same,
[07:25] I'm going to create a new Java class with the name TaskPriorityConstantDemo.
[07:33] Inside this class
[07:34] first we need to create the main() method post that using the taskUtil() method, I'm going to invoke the
[07:39] static method that we have written, which is getEstimatedCompletionTime().
[07:44] So here for this method I'm trying to pass the value as zero.
[07:48] The output
[07:48] from this method I can try to print out with the help of System.out.println().
[07:54] So I can move all this code as an input to the println() method.
[07:58] The same I can try to repeat by passing various task priority like one, two and three.
[08:05] So if I try to execute this program, you will be able to see the output like seven, five, three and
[08:11] one.
[08:11] So this is working like we expect.
[08:14] Let's see what is going to happen if we try to send a invalid value.
[08:18] Like maybe I'll try to send ten instead of zero.
[08:21] In this kind of scenario, obviously we are going to get a IllegalStateException because we have a
[08:27] default case inside our switch expression handling the invalid input data.
[08:32] With this business logic, you might be under the assumption that this is working perfectly, and there
[08:37] are no drawbacks with this approach.
[08:38] But there are good amount of drawbacks with this constant approach, which we are going to discuss in
[08:44] the next lecture.
[08:45] I hope you are with me.
[08:46] Once we discuss about the drawbacks of the constants approach, we are going to build the same solution
[08:51] with the Enums that you're going to appreciate the benefits provided by the Enums.
[08:56] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
