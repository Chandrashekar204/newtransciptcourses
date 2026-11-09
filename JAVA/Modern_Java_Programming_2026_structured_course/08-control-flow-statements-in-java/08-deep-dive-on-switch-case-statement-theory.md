# 8.8 — Deep dive on switch case statement - Theory

> Section 8: Control flow statements in Java

[00:00] As of now, we discuss on how to write the conditional Java statements with the help of if statements.
[00:07] On the very similar lines
[00:08] we can also use switch case statements to write conditional statements inside Java.
[00:15] So there are two approaches for the developers.
[00:17] One is with the help of if statements and the other one is with the help of switch case statement.
[00:23] Here you may have a question, which is why we have two different approaches inside Java and when to
[00:29] use which approach.
[00:30] To explain you about the same.
[00:32] First, let me give you a problem.
[00:34] Think like there is a supermarket and inside this supermarket they are going to sell lot
[00:39] many fruits like banana, apple, grapes, pineapple, mango.
[00:43] So for each of the fruit the price is going to be different.
[00:47] So the owner of the supermarket, he asks you to develop a Java logic to determine what is the price
[00:54] that he has to charge to the customer based upon the fruit selected by the customer.
[00:59] To solve this problem,
[01:01] if you go with the if statement approach, your logic is going to look like this.
[01:05] Like first I'm going to check if the fruit name is equal to banana
[01:09] if yes, I'm going to print a statement,
[01:11] $1 is charged and post that I can write else if statements to check apple, to check grapes to check
[01:19] pineapple and to check mango.
[01:22] And at last I can have an else statement if my fruit name is not equal to any of the valid fruit names,
[01:28] I'm going to print a statement which is pick a valid fruit with the help of else statement.
[01:34] This may look very good for you, but if you closely observe this Java program that we built with the
[01:39] help of if statements, we are trying to evaluate the condition at multiple places at each if block
[01:47] and else if block,
[01:48] I'm trying to check whether my fruit name is equal to so and so value.
[01:52] So the condition is getting evaluated multiple times.
[01:55] On top of that, my code also is looking very lengthy and clumsy.
[02:00] So as the conditions that you have to evaluate is going to increase, the amount of code that you are
[02:07] going to write is also going to be increased.
[02:09] On top of that, you need to evaluate the condition for each and every if and else if blocks.
[02:16] So to overcome this challenge we have switch case statement inside Java.
[02:21] So whenever you have these kind of scenarios where you have to evaluate lot many conditions, in such
[02:27] cases you can use more efficient approach which is switch case statement.
[02:34] I hope you are clear when to use switch case statement. As a next ste,
[02:38] let's try to understand the syntax of the switch case statement.
[02:42] The syntax of the switch case statement is going to be very simple.
[02:46] Like you can see
[02:47] first we need to start the switch statement with the help of switch keyword.
[02:51] And after that inside the parentheses you need to write an Java expression, which is going to be evaluated
[02:57] only once based upon the outcome from the expression
[03:00] one of the case that we have defined inside the switch block is going to be executed.
[03:06] You can see I have so many case statements.
[03:09] With the help of case, I have defined a label1, label2, label3.
[03:13] So if my expression is evaluated to a value which is equal to label1, then whatever statements I
[03:21] have written under this case is going to be evaluated.
[03:24] Similarly
[03:25] the same is going to happen for label2 and label3.
[03:28] If my Java expression is not evaluated to any of the label values in such scenarios, the default block
[03:36] is going to be executed.
[03:38] So under default I can write some Java statements.
[03:41] And if you closely observe the syntax, we also have a break keyword used inside each of the case,
[03:48] including the default.
[03:49] The purpose of the break is whenever your expression is evaluated to one of the label,
[03:55] whatever Java statements that you have under that label case are going to be executed.
[04:00] Once these execution of this statements is completed, you want to break the flow and come out of this
[04:07] switch expression.
[04:08] If you don't have this break, then your switch case is going to execute the next case labels as well.
[04:14] So this break is completely optional.
[04:17] If you don't mention this break keyword inside all your case labels and default block, then in such
[04:23] scenarios you may get an unexpected results.
[04:27] For example, think like this expression is evaluated to a label2.
[04:31] In this scenario, you might be expecting only the case label2 to be executed, but in the scenario
[04:38] where you are not mentioning the break, all the next label cases and the default block also is going
[04:44] to be executed.
[04:45] So as soon as this case label2 is executed, since there won't be any break, the execution will
[04:50] jump to the label3.
[04:52] And if the label3 also does not have break statement, it will go to the last block which is default
[04:57] block.
[04:58] So to avoid this kind of behavior
[05:00] always make sure you are mentioning the break keyword inside each of your cases, including the default
[05:08] one.
[05:08] So we have an expression after the switch keyword.
[05:11] So the value that is going to be derived from this expression has to be of type byte, short, char, int, enum
[05:21] or String.
[05:22] Remaining data types are not allowed.
[05:24] For example, the boolean is missing from this list and float, double, long
[05:30] all these values are missing from this list.
[05:32] That means you cannot write an Java expression, which is going to result as a boolean, or a float,
[05:39] or a double, or a long,
[05:41] whenever you are using the switch case statement.
[05:44] On top of that, one more important point that you need to take care is whatever label1, label2
[05:51] values that you are going to define against each of the case.
[05:54] They have to be compile time constant expressions.
[05:58] You can't define a variable or an expression against these labels like label1, label2 and label3.
[06:04] .
[06:05] I'm going to show you all these in demo.
[06:07] Then it is going to make more sense to you.
[06:09] So whenever you are trying to build a switch case statement, by following this syntax, all these steps
[06:14] are going to be executed.
[06:16] First
[06:16] the Java expression is going to be evaluated and based upon the value derived, one of the case label
[06:23] will be selected and all the statements inside the case label block will be executed by the switch statement.
[06:30] So this way with the help of switch case statement
[06:33] also, we're able to control the execution of the Java statements.
[06:36] Let me show you an example on how to write the switch case statement
[06:41] by taking the same supermarket example.
[06:44] Here you can see first I have a fruit name as mango.
[06:47] So this fruitName variable I'm trying to send as an expression to my switch statement.
[06:53] At runtime, my switch statement is going to look what is the fruitName value that I have under the
[06:59] variable fruitName.
[07:00] Accordingly, it is going to select one of the case label.
[07:04] For example, here we have a mango as an value.
[07:08] So it will go to the mango case block.
[07:12] And inside the mango case block we have System.out.println() which is $3 charged.
[07:18] Post that we have a break statement.
[07:20] You can see this time the code is looking very neat and we are not evaluating the condition at the multiple
[07:27] places.
[07:27] We are simply evaluating that Java expression only once and based upon the value from the Java expression,
[07:35] we are going to execute one of the case.
[07:38] I hope you are clear.
[07:39] Now let me share more important details about the switch case statement.
[07:43] Like I said before, whenever you are trying to use the switch case statement, please make sure that
[07:48] your expression is not going to evaluate a value of type boolean, long, float, and double.
[07:56] Even if you try to pass a variable of type boolean, long, float and double to your switch statement,
[08:03] you are going to get an compilation error.
[08:05] And the second point that I want to highlight here is the break statement, like we discussed is used
[08:11] to exit the switch statement once the corresponding code segment is executed.
[08:17] Otherwise all the following cases will be executed.
[08:21] That's why always make sure you are mentioning the break statement inside your switch case statement.
[08:28] If you closely look at this switch case statement, the last case that we have is default.
[08:33] So default also has a break statement.
[08:35] And here you may have a question which is anywhere below the default
[08:40] we don't have any other cases to be executed with that assumption
[08:44] you might be thinking why should we mention break statement inside the default?
[08:48] I agree with you.
[08:49] Technically the final break is not required because the flow anywhere falls out of the switch statement,
[08:57] but using a break statement is strongly recommended so that in future, if any of the other developer
[09:04] he's trying to add more number of cases after the default case in such scenarios, if the new developer
[09:10] forget to mention the break statement, then in such scenarios you are going to get unexpected result
[09:15] that's why always make sure you are maintaining the break statement in all the case statements, including
[09:22] the default.
[09:24] As of now, you can see inside my switch case statement, I'm using an expression which which is going
[09:29] to be evaluated as a String object.
[09:32] So using the String object inside the switch expression is allowed only from the Java 7 version.
[09:39] Before Java 7 version, we are only allowed to use int, byte short, but from Java 7 even the
[09:48] String objects are also allowed to use as part of the switch expression.
[09:53] Let's see what do we have as a next point?
[09:56] The next point is related to that default label that we have.
[10:00] So here inside the program, I have mentioned the default label at the end, but it is not mandatory.
[10:07] You can always build your switch case statement without default label as well.
[10:12] On top of that, whenever you are defining the default label, you don't have to be the last label.
[10:17] You can use this default label even at the starting or in the middle of the switch case statement.
[10:23] And please note that at max we can only define one default label inside switch case statement.
[10:30] I hope you are clear about that default label.
[10:32] Now moving on to the normal case labels.
[10:35] Whenever you are trying to define case labels inside a switch statement, we cannot define two case
[10:42] labels with the same value.
[10:44] For example, here I have a case banana,
[10:46] I can't create one more case with the same banana that is not allowed, and I'm going to get a compilation
[10:53] error that is very obvious.
[10:55] Why do we want to maintain duplicate cases or conditions inside our program?
[11:01] And the last important point that I want to highlight here is, what our case labels that we have defined
[11:07] inside our switch case statement
[11:09] we need to make sure these values like banana, apple, grape.
[11:14] So all of them they should be compile time constant.
[11:17] Like I said before, I can't define a String variable or String object or a Java expression as a case
[11:25] label.
[11:25] I should always make sure I'm mentioning a compile time constant value
[11:30] otherwise I'm going to get a compilation error.
[11:33] I hope you are clear with these points.
[11:35] Now very quickly let me show you the same program with a different flavor.
[11:41] Here my requirement is for both banana and apple,
[11:44] I should charge the same $1 in this kind of scenarios, where you want to have a common logic for different
[11:50] cases, you can achieve that easily by following these kind of syntax.
[11:54] You can see first I have mentioned the case banana.
[11:57] Immediately I have mentioned a different case, which is case apple.
[12:01] And at these two cases I can define my Java statements which are going to be executed if my fruit name
[12:08] is banana or apple.
[12:10] So whenever you have this kind of common business requirements, you can also try to have a common Java
[12:16] statements for multiple case labels.
[12:19] So whatever we are discussing right now this is a switch case statement.
[12:24] But from Java 14 a new syntax of switch statement is introduced.
[12:29] And the name of that switch statement is switch expression.
[12:33] Obviously there are some drawbacks with the switch case statement,
[12:36] that's why Java team they have introduced a new form of switch statement which is with the name switch
[12:43] expression.
[12:43] So the switch expression is more convenient to use compared to the switch case statement.
[12:49] So we are going to discuss about the switch expression as well in the coming lectures.
[12:53] But here you may have a question then if there is a more convenient way which is switch expression is
[12:59] available inside Java, why are you teaching us about the switch case statement?
[13:03] The question is very valid, but let me clear your question.
[13:07] Though a new switch expression is introduced inside Java.
[13:11] The Java team did not removed or deprecated the switch case statement.
[13:16] Even today from the latest versions of Java, you can use either switch case statement or switch expressions.
[13:22] Both of them are valid and many Java projects which built before Java 14
[13:28] they will have lot of these switch case statements inside the Java code.
[13:32] So that's why as Java developer, you should know the both flavors of the switch statement.
[13:38] Once you understand both flavors of the switch statements, it's up to you which one to use based upon
[13:44] your business requirements.
[13:45] You may work in an legacy project or a world project where they might be using a Java version which
[13:51] is less than Java 14.
[13:53] In such scenarios, you don't have any option.
[13:56] You have to use the switch case statement.
[13:58] Whereas if you are going to work on a Java project where they are going to use the version which is
[14:03] above or equal to Java 14, then obviously you're going to always go with the switch expression, because
[14:09] that supports more convenient syntax.
[14:12] I hope you are clear with this very quick introduction about the switch statement in the next lecture,
[14:17] first, let me try to build a Java program with the help of switch case statement.
[14:21] Once we are clear about everything about the switch case statement, we can explore the switch expression
[14:27] as well.
[14:28] Thank you bye.

----------------------------------------
