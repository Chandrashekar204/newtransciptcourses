# 8.10 — [JAVA 14] Deep dive on switch expression - Theory

> Section 8: Control flow statements in Java

[00:00] Let's try to understand about switch expression.
[00:03] Like I said before, this switch expression we can only use from Java 14 version.
[00:09] That's what I have highlighted inside this slide as well.
[00:13] With the help of the switch expression, we can build switch statement in a more compact form or a concise
[00:21] form.
[00:21] For example, you can see inside the screenshot I have used the switch expression using the switch expression
[00:28] I have written the conditional logic for the supermarket scenario.
[00:33] So whenever we are trying to use a switch expression, we need to make sure we are using these arrow
[00:38] symbol in the case of colon.
[00:41] So this is our differentiator for your Java compiler to understand whether a developer is using switch
[00:47] expression or a switch case statement.
[00:50] In the case of switch case statement, after the case label, we are supposed to mention colon, whereas
[00:57] inside the switch expression we can mention the arrow symbol.
[01:01] Immediately after the arrow symbol, you can build your Java statements, and whenever you have a scenario
[01:07] where you want to execute a common logic for different case labels, you can simply mention all those
[01:14] labels by using comma separator.
[01:17] You don't have to repeat the case banana and the case label multiple times.
[01:21] The case word can only be mentioned once, followed by all your labels separated by comma.
[01:28] So this is one of the improvement introduced in the switch expression.
[01:32] Apart from these improvements, whenever you are trying to use a switch expression, you don't have
[01:36] to specifically mention a break statement.
[01:39] By default, switch expression is going to consider a break statement for each of your case, including
[01:47] the default statements.
[01:48] With that, we are going to save a lot of space inside our Java program.
[01:53] So that's why these days most of the Java developers, they prefer switch expression compared to the
[01:59] switch case
[02:00] wherever possible.
[02:01] I would also recommend you to follow the switch expression if your project is using a Java version which
[02:07] is greater than or equal to 14.
[02:09] I hope you are clear with these initial introduction about the switch expression.
[02:14] Now let me explain you more important points around the switch expression.
[02:19] As of now, you can see inside my business logic, I have only a single Java statement to be executed
[02:26] for each of the case label.
[02:28] But if you have a scenario where you want to execute to multiple Java statements in such scenarios,
[02:34] whenever you are using switch expression, you need to surround all your multiple Java statements with
[02:40] a curly brace.
[02:41] So as soon as you mention the arrow symbol, you need to start the opening curly brace and post that
[02:46] you can mention any number of Java statements.
[02:49] And at last you need to close your curly brace with the help of closing curly brace.
[02:53] The same you need to follow for all your cases wherever you want to execute multiple Java statements,
[02:59] whereas this is not the requirement for the switch case statement. Inside the switch case statement
[03:04] under each case, you can define any number of Java statements without mentioning curly braces.
[03:11] And one more important point that you need to be aware whenever you are using switch expression is whenever
[03:17] you are using this syntax, your switch expression is going to expect you to implement default as a
[03:24] mandatory.
[03:24] If you forget to mention default related statements and the default case, the switch expression immediately
[03:31] is going to throw an compilation error.
[03:33] This way, switch expression is going to provide an advantage to the developers to make sure that we
[03:39] have handled all possible cases.
[03:42] Maybe if my end user is not giving a valid fruit name, then in such scenarios we are not going to get
[03:48] any output if we don't use the default case.
[03:50] So to handle these kind of scenarios, the switch expression is going to mandate you to implement the
[03:57] default case.
[03:58] I'm also going to show you a demo about this in the next lecture.
[04:02] Apart from all these advantages, whenever you are using switch expression, if needed, we can return
[04:08] a value from the switch expression.
[04:10] So here you can see I have returned the switch expression as an expression and the output from the switch
[04:17] expression I'm trying to assign to the String object with the name output.
[04:22] So each of my case present inside my switch expression
[04:25] they are going to return a String object.
[04:28] So after the arrow symbol I have a String the same
[04:31] I'm going to return whenever my fruit name is banana or apple.
[04:35] The same applies for grapes, pineapple, mango and default.
[04:39] So whatever we are trying to send from our case statements, the same is going to be assigned to this
[04:45] output variable and the same
[04:47] we can try to print out with the help of this single System.out.println().
[04:52] This way, whenever it is needed, we can use our switch expression to return a value.
[04:57] The same is not possible with the
[04:59] switch case statement.
[05:01] I hope you are clear with the discussion around the switch expression.
[05:05] In the next lecture,
[05:06] let's try to build an Java program with the help of switch expression.
[05:11] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
