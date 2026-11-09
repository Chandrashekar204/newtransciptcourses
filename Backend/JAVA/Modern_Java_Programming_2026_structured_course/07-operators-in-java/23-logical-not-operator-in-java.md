# 7.23 — Logical NOT operator in Java

> Section 7: Operators in Java

[00:00] The simplest Logical operator we have is Logical Not operator.
[00:05] The syntax to use this operator is,
[00:07] you need to first mention the exclamatory mark followed by your operand.
[00:12] The operand can be a direct to boolean literal value, or a boolean variable, or a Java expression
[00:19] that is going to return a boolean value as an output.
[00:22] Like we discussed in the previous lecture, whenever we are giving an input to this Logical Not operator,
[00:28] it is going to negate the boolean value of its operand, and the reverse value of the boolean is going
[00:35] to be returned as an output from this operator.
[00:38] For example
[00:39] here you can see I have few lines of code.
[00:41] In the very first line I have created a boolean variable which is isValid post that to
[00:46] this isValid,
[00:47] I'm trying to assign an expression where I'm trying to use the Logical Not operator.
[00:53] So first I have mentioned the exclamatory mark followed by boolean literal value, which is true.
[00:58] So if I run the second line, the outputs that we are going to store inside the isValid is false because
[01:04] like we discussed, this Logical Not operator, it is always going to negate the boolean value.
[01:10] It will convert the true as false and false as true.
[01:14] In the next statement
[01:15] you can see I have given the false as an input to the Logical Not operator, and I'm going to get
[01:20] the true as an output value.
[01:22] So in the second line and third line, we are trying to provide the boolean literal values directly.
[01:27] Instead, we can also give an Java expression as an input to these Logical Not operator.
[01:34] If you see the last line, I'm trying to check if the num1 > num2.
[01:39] So my greater than operator, which is an Relational operator, I know it is going to give a value either
[01:45] true or false.
[01:46] So in this scenario, since num1 is greater than num2, I am going to get the output as true from
[01:52] these inner expression that I have written within the parentheses.
[01:56] And since we are going to feed that true value as an input to the Logical Not operator, we are going
[02:02] to get the output as false, and the same is going to get stored inside
[02:06] this variable isValid.
[02:08] So whenever you are using the Logical Not operator, please make sure you are providing the operand
[02:13] of type boolean.
[02:15] And since it is an unary operator, it is always going to expect only one operand as an input.
[02:22] Understanding Logical Not operator should be very simple.
[02:25] Now with these understanding, let's try to see a quick demo of these Logical Not operator inside IntelliJ.
[02:31] Inside my IntelliJ I am going to create a new Java class, and the Java class name is going to be Logical
[02:38] LogicalOperatorsDemo.
[02:40] Inside this class first
[02:42] as usual, we need to create the main() method because we want to execute all the lines of code in Java.
[02:49] Whenever we want to initiate the execution, we need to make sure we have a main() method inside the Java
[02:55] class.
[02:55] So now inside this main class, first I'm going to create a boolean which is isValid and here I'm simply
[03:02] doing the declaration.
[03:03] I'm not doing any initialization or assignment post that to
[03:07] this isValid,
[03:08] I'm going to assign an expression which involves Logical Not operator.
[03:13] And here I can directly mention the literal value.
[03:16] Very similarly, I can also mention false
[03:19] also, as a next step, I'm going to assign a Java expression to the Logical Not operator for the same,
[03:25] first, let me create two int variables with the value nine and six.
[03:30] So the variable names are num1 and num2.
[03:34] Now to that isValid boolean,
[03:36] I'm going to assign an expression which involves Logical Not operator.
[03:40] So here I'm going to mention parentheses.
[03:43] And inside the parentheses I can give an expression which is num1 > num2.
[03:49] So please make sure you are surrounding the Java expression with parentheses.
[03:54] Otherwise you're going to get a compilation error.
[03:56] Let me show you that if I remove these parentheses, I'm going to get a compilation error because immediately
[04:02] after the Logical Not operator we have mentioned num1.
[04:05] So what is a num1 data type,
[04:07] it is an int.
[04:08] That's why I am going to get an compilation error.
[04:11] Whereas if you keep the parentheses like we discussed before, first whatever expression that we have
[04:16] defined inside the parentheses is going to be evaluated.
[04:20] So once this expression is evaluated we are going to get the output as a boolean value which is true.
[04:26] So if you try to provide that true value as an input to these Logical Not operator, then there will
[04:32] not be any issues
[04:33] and I'm going to get the output.
[04:35] Let me try to execute this program in a debug mode by keeping a breakpoint at line number six.
[04:40] Once the program is started in debug mode, you can see the program is passed at the breakpoint, which
[04:46] is present at the line number six at this point of time,
[04:50] now, if I try to step over to the next line, you can see after executing the line number six, the
[04:57] value that I have inside is valid is four.
[05:00] The same
[05:00] we can also see here as well.
[05:02] Now the isValid is changed to true and once we executed the last statement, the isValid is going
[05:09] to become false. Because we are trying to provide true value as an input to that Logical Not operator
[05:16] and true off Logical Not operator is going to give false as an output.
[05:21] I hope you are clear.
[05:22] And here you may have a burning question, which is we are learning lot of operators, but where we
[05:28] are going to use them in real projects at this point of time, I would say don't worry about them because
[05:34] we are yet to discuss about more complex topics inside Java.
[05:38] In the coming sections, I'm going to teach you how to write the business logic based upon some conditions.
[05:44] For example, you may have some business requirement inside your Java only if the person age is greater
[05:51] than 18,
[05:52] that means only if the person is an adult, then only execute a piece of logic.
[05:57] Otherwise you want to execute some other business logic.
[06:00] For such conditional behavior, we can use the logical operators to a great extent.
[06:05] So all the operators that we are discussing throughout this section, they have a purpose in Java,
[06:10] when we start learning and exploring about the advanced topic in Java, then it is going to make more
[06:16] sense to you.
[06:16] What is the role that these operators are playing inside the Java programming language?
[06:21] For now, my humble request is to simply focus on understanding what are these operators, what is the
[06:27] syntax to use them, what kind of input we can give them, what kind of output we can expect from them.
[06:33] So please focus on all those basic details for now.
[06:36] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
