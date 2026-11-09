# 7.39 — Ternary or Conditional operator in Java

> Section 7: Operators in Java

[00:00] Inside this lecture, let's try to discuss about ternary operator or conditional operator.
[00:06] So we have two names
[00:07] for this operator.
[00:09] We can either call it as ternary operator or conditional operator.
[00:13] This is the only operator in Java which is always going to expect three operands.
[00:18] That's why the other name for this operator is ternary operator, the symbol that we need to use whenever
[00:24] we want to use this conditional operator in Java is question mark, followed by colon.
[00:30] But don't be under the assumption we need to mention question mark colon immediately without any space.
[00:36] So there is a clear syntax that we need to follow.
[00:39] Let's try to understand what is that syntax.
[00:41] Whenever you are using these conditional operator like we discussed we need to provide three operands.
[00:47] The very first operand should be an boolean expression or a boolean value or a boolean variable.
[00:54] Once you mention your operand1, you need to mention a question mark followed by a true expression.
[01:00] So a true expression means this second operand or this true expression is going to be evaluated in the
[01:08] scenarios
[01:08] if your first operand is going to give the output as true.
[01:12] Whereas if your first operand, which is boolean expression, if it is giving the output as false,
[01:18] then it is going to execute the false expression or the code that you have written as part of the third
[01:24] operand.
[01:25] So first you need to mention what is your boolean expression followed by question mark, followed by
[01:29] what is your true expression followed by colon?
[01:32] And at last you can mention what is your false expression that you want to be executed whenever the
[01:38] boolean expression returns a value of false.
[01:41] I know it is super hard to digest this syntax.
[01:44] That's why let me try to make it more clear for you by taking an example.
[01:48] So here you can see I have an int variable x which has a value ten.
[01:54] And similarly I also have another variable which is y with the value 20.
[01:59] Now using the conditional operator I want to understand which is the maximum number between my x and
[02:06] y.
[02:07] That's why I'm going to write an Java expression with the help of conditional operator. To achieve the
[02:12] same,
[02:12] you can see
[02:13] first I'm trying to create an integer variable max followed by is equal to and to this max variable
[02:19] I'm going to assign an expression, which I'm going to build with the help of conditional operator.
[02:25] So first we need to give an boolean expression as a first operand.
[02:29] When I say boolean expression, whatever code or whatever variable or whatever literal that you are
[02:35] going to mention as part of operand1, it should always give an boolean as an output.
[02:41] So here the condition that I want to check is is x greater than y.
[02:46] If this returns true, then I want to return a value x.
[02:50] So that's why after question mark I have mentioned x followed by colon and after the colon I have mentioned
[02:57] y.
[02:57] So conditional operator is an short form of writing an if else statement, we are yet to discuss about
[03:05] if and else statements in the coming sections,
[03:08] we are going to discuss about them using the if else statement or using the conditional operators
[03:13] we can write conditional logic.
[03:15] So here it is pretty clear that when this expression is true, I want this code to be executed, which
[03:22] is written under the operand2.
[03:24] Otherwise I want to execute the expression which is written and at the operand3.
[03:29] So based upon how my input is changing, the output is also going to change conditionally based upon
[03:35] the logic that I have written.
[03:37] So in the place of if else statements, we can always use these conditional operators as well.
[03:42] If you want to achieve the same results in a concise way.
[03:46] But please don't try to overuse these conditional operators, because sometimes these operators, they
[03:52] are hard to read for new people who are trying to learn the Java until
[03:57] unless someone knows the syntax about the conditional operator, they cannot really understand what
[04:03] is this expression is going to do?
[04:05] I hope you are clear with this theory discussion.
[04:07] Now let me try to execute the same example inside my IntelliJ inside my IntelliJ,
[04:12] I'm going to create an new class and the class name is going to be TernaryOperatorDemo.
[04:20] Inside this class
[04:22] first I'm going to create an main() method here
[04:25] inside this method, first let me try to create an variable x and to this I'm going to assign a value
[04:31] ten, followed by I'm going to create another int variable y with a value as 20.
[04:38] Now as a next step I'm going to create an variable with the name max.
[04:42] And to this I'm going to assign an expression, which I'm going to build with the help of conditional
[04:48] operator or ternary operator.
[04:50] So the very first operand that we need to pass to the ternary operator is the boolean expression that
[04:56] we want to execute.
[04:58] So the boolean expression that I want execute
[05:00] here is is x > y?
[05:03] If x greater than y, then I want that x to be returned and the same to be assigned to the max variable.
[05:11] Otherwise I want the y to be assigned.
[05:14] So with this input we are going to get the y as an output from this expression that's y under the max
[05:21] we are going to have the value 20.
[05:23] I can also confirm you the same by printing the max variable.
[05:28] So let me print this and you can see we have the output as 20.
[05:32] This way we can build any kind of logic.
[05:35] Maybe I can try to build a small logic to identify if a given number is an even number or not.
[05:42] First, let me create a boolean variable with the name
[05:45] isEven.
[05:46] To this I'm going to assign an Java expression, which I'm going to build with the help of ternary operator.
[05:52] Inside the boolean expression, I'm going to check whether a given number is an even number or not.
[05:58] So how to check whether a given number is even number or not?
[06:01] We need to divide it with the two.
[06:03] If the remainder is zero, then we can safely assume it is an even number
[06:08] otherwise it is not an even number.
[06:10] For example, I can take the number 14 and I'm going to use a modulus operator.
[06:15] After the modulus operator I'm going to mention two.
[06:18] So with this the division will happen
[06:20] and I want to check if the output from this expression is equal to zero or not.
[06:25] So I can keep these 14 module two inside an parentheses,
[06:31] so first this expression is going to be evaluated.
[06:34] And the output we are going to check if it is equal to zero or not.
[06:38] So based upon this comparison I'm going to get the output whether it is true or not.
[06:43] If I get the output as true, I want to simply return the true as an output, otherwise the false.
[06:50] So this confirms me whether a given number is an even number or not.
[06:55] So let me try to execute this program.
[06:57] You can see we are getting the output as true, whereas if I try to give some odd number, maybe I'll
[07:02] give 11.
[07:03] This time we can expect the output as false.
[07:06] Did you see how powerful this operator is?
[07:09] As we explore more and more about Java, you're going to get more interest and you may feel it is very
[07:15] tough, but my sincere request is don't lose hope and always keep doing the hard work.
[07:21] Once you find a sweet spot inside the Java, nothing can stop you.
[07:25] So please always have strength and keep trying.
[07:29] If you face any issues or if you face any errors, don't get demotivated.
[07:33] We need to keep trying until we understand the issue and resolve it this way.
[07:38] We are going to learn a lot and we are going to mature day by day inside the Java programming.
[07:44] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
