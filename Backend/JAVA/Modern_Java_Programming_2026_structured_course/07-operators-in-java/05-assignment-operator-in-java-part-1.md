# 7.5 — Assignment Operator in Java - Part 1

> Section 7: Operators in Java

[00:00] Inside this lecture, let's talk about a simple operator available in Java, which is assignment operator.
[00:08] We have been using this a lot in lot many examples.
[00:12] So this is going to be super easy for you to understand as well.
[00:16] That's why I'm starting the discussion of Java operators with this
[00:20] operator.
[00:20] So what is an assignment operator.
[00:23] With the help of this operator, we can assign a value which is present on the right hand side to the
[00:29] variable on the left hand side.
[00:31] Since this assignment operator is going to operate on two operands, one is on the left hand side,
[00:37] the other one is on the right hand side.
[00:39] We can call this operator as a binary operator.
[00:42] So how to use this assignment operator.
[00:45] It is very simple.
[00:46] You already know about this.
[00:47] Like you can see here I have written three lines of Java code where I'm trying to use this assignment
[00:53] operator.
[00:54] So whenever we want to use this assignment operator you need to use a symbol which is is equal to don't
[01:00] try to use double is equal to because double is equal to is a different operator in Java, which we
[01:06] are going to discuss in the coming lectures.
[01:08] If you observe any of these three Java statements on the right hand side, we are mentioning a literal
[01:14] value.
[01:15] So this is one operand on the left hand side of the assignment operator
[01:20] we are mentioning a variable name.
[01:22] And this is going to be a second operand.
[01:24] So whatever value that we are mentioning on the right hand side is going to be assigned to the variable
[01:31] present on the left hand side.
[01:33] So this is the simplest form of using the assignment operator.
[01:37] With this you should not be super confident that you know everything about the assignment operator.
[01:42] There is lot we need to discuss.
[01:44] Each operator has some special scenarios.
[01:46] We are going to focus on all those special scenarios so that you can become a master in Java programming
[01:52] language.
[01:53] The very first important information that I want to share here is whenever you are using this assignment.
[01:59] Operator.
[02:00] It is going to work based upon the right associative.
[02:03] That's why we can also call this assignment operator as an right associative operator.
[02:09] The reason why it is called as right associative operator is it is going to be evaluated from right
[02:15] to left.
[02:16] If you take the Java statement which is int num = 98.
[02:20] First this is equal to operator is going to look what is the value that it has on the right hand side.
[02:26] Once it is clear what is present on the right hand side, the same data it is going to assign to the
[02:31] variable which is present on the left hand side.
[02:34] Since the evaluation process is getting started from the right hand side and ending on the left hand
[02:40] side, we can consider this operator as an right associate to operator.
[02:45] I can give one more example
[02:47] also.
[02:47] Here you can see I have declared two variables like num1 and num2 and post that I have built a chained
[02:55] assignment operator expression.
[02:57] So this is also perfectly possible in Java.
[03:01] I can build expression like num1 = num2 = 98.
[03:05] So how this is going to work, the evaluation of these expression is going to start from the right hand
[03:10] side.
[03:10] So what do we have on the right hand side,
[03:12] we have 98 value.
[03:13] This 98 value is going to be assigned to the num2.
[03:17] Once this num2 = 98 is evaluated
[03:22] whatever result that we get from the num2 = 98 is going to be assigned to the num1.
[03:28] So what do we get from the num2 = 98
[03:30] we are going to get a value which is 98, and the same is going to be assigned to the num1 which is
[03:36] present on the left hand side.
[03:38] You can see there is also an arrow I have mentioned, and how the direction is going to be followed
[03:44] when this expression is going to be evaluated, the direction is from the right hand side to the left
[03:50] hand side.
[03:50] That's why we can call this as an right associative operator as well.
[03:55] So here I have used the chained assignment operator only with the help of two variables.
[04:01] But if needed you can use the chained assignment operator with any number of variables like you can
[04:08] see here.
[04:09] I'm trying to build and chained assignment expression by using so many variables like num1, num2, num3,
[04:15] num4, num5.
[04:17] Whenever you want to write these kind of expression, first you need to make sure you are declaring
[04:22] the variable names.
[04:23] Once the declaration is completed, you can assign a same value like 98 by chaining all the variables
[04:29] with the help of assignment operator.
[04:32] I can also show you this with the help of a demo for the same
[04:35] let me go to the IntelliJ inside my IntelliJ
[04:38] as of now you can see we are working on the project which is section6.
[04:42] But right now we started a new section which is section7.
[04:46] For that reason, since we are into the new section, I want to create a new Java project using which
[04:52] I can build all the examples that we are going to discuss inside this section.
[04:57] For the same
[04:58] the steps are going to be very simple.
[05:00] You
[05:00] already aware about these steps, you can go to the File, New, Project and type the project name as
[05:07] section7 and post that I want to save this project inside a location
[05:12] Storage, workspaces, java.
[05:15] So let me select this java folder.
[05:17] Once the location is provided, I want to select the language as Java, Build System as IntelliJ and
[05:22] JDK as Corretto 21.
[05:24] So let me click on this create button.
[05:26] You can see I got a brand new Java project with the name section7.
[05:31] Inside the src folder I'm going to create a new Java class and the class name
[05:37] I'm going to keep it as AssignmentOperatorDemo inside this class
[05:42] first let me create a main() method by using psvm shortcut.
[05:47] Now here I'm going to create multiple variables like num1, num2, num3, num4, num5.
[05:54] So there are two approaches that we can follow.
[05:56] One is the very basic approach which is we can declare all these fields in different lines like num1
[06:02] and num2, num3.
[06:05] So this is the most basic approach.
[06:07] Instead of that, we can try to declare all the variables in a single line by using a separator comma.
[06:15] So let me do that int num1, num2, num3, num4, num5.
[06:23] So here you can see with a single expression I'm trying to declare five different variables of type
[06:31] int to all these variables
[06:33] if needed I can assign different, different values with the help of assignment operator.
[06:39] For example, I can provide a value 16 to the num1,
[06:44] very similarly, for the num2, I can assign a value 17.
[06:48] So this way we can individually assign different values with the help of assignment operator.
[06:53] You already aware about this syntax, but what if you want to assign a same value to all the variables
[06:59] in such scenarios you can simply type num1 = num2 = num3 = num4 =num5 =
[07:09] and what is the value that you want to assign.
[07:15] So here I can type 98.
[07:17] So this is the value that I want to assign.
[07:19] And you need to terminate the expression with the help of semicolon.
[07:24] Like we discussed the assignment operator is always going to execute from right to left.
[07:30] So on the very right hand side what do we have,
[07:32] we have a literal value which is 98.
[07:35] So this value is going to be assigned to the num5 first.
[07:39] So once this num5 = 98 is evaluated behind the scenes.
[07:44] The num5 variable is going to hold the data 98. Post that the expression is going to change as num5
[07:51] .
[07:52] So this is how the expression is going to be changed behind the scenes when the assignment operator
[07:56] is being executed by your JVM or Java interpreter.
[08:01] So what do we have inside num5.
[08:03] So num five holds a data which is 98.
[08:06] The same is going to be assigned to the num4.
[08:08] This way the whole expression is going to be evaluated from right to left.
[08:14] I hope you're clear.
[08:15] We need to discuss a lot more about assignment operator.
[08:18] That's why let's continue this discussion in the next lecture as well.
[08:22] Thank you
[08:22] and I'll catch you in the next lecture bye.

----------------------------------------
