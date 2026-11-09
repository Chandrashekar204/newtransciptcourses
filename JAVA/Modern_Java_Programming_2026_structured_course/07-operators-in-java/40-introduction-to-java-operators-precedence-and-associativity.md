# 7.40 — Introduction to Java operators Precedence & Associativity

> Section 7: Operators in Java

[00:00] We discussed about all the operators that are available in Java.
[00:04] As a next step, we need to discuss about a very important topic related to the Java operators.
[00:11] And this topic is Java operators precedence and associativity.
[00:16] First, let's try to discuss about operators precedence.
[00:19] Many times inside your real projects, you may end up using multiple operators inside your Java expressions.
[00:28] In such scenarios, Java is going to follow operators precedence to execute or to evaluate your Java
[00:36] expression.
[00:36] With the help of this precedence, Java maintains what is the priority or the precedence number for
[00:43] each operator.
[00:44] So if there are multiple operators available inside your expression Java first it is going to evaluate
[00:50] the operator which has highest precedence, followed by operator which has lowest precedence.
[00:57] To understand more about these precedence, let me take an example.
[01:02] Like you can see here we have an example which is inte calNum = 16 - 8 * 2.
[01:11] So inside this we have multiple operators like is equal to is an assignment operator, minus is an another
[01:19] operator followed by asterisk.
[01:21] So there are three different operators.
[01:24] At least for my Java
[01:25] it should be pretty clear whenever we are using Assignment operator
[01:28] first it needs to evaluate what is present on the right hand side.
[01:32] Post that whatever value that we derived from the right hand side, it is going to assign the same to
[01:38] the left hand side variable, which is calNum.
[01:40] But if you look at the right hand side expression here we are using two different operators.
[01:46] One is minus or subtraction and the other one is asterisk which indicates multiplication.
[01:53] If you closely observe these expression, there are two kinds of outcome I can expect.
[01:58] Think like first my JVM or Java has evaluated 16 minus eight.
[02:04] So in this scenario we are going to get eight into two which will make the overall output as 16.
[02:10] Whereas if you think like if my Java executed 8 * 2 two expression first, in such scenario 16 -16,
[02:18] we are going to get the output as zero.
[02:21] So based upon how Java is going to evaluate my expression, the output is also changing in my scenario.
[02:27] Do you think in this kind of scenarios Java is going to randomly execute my expression?
[02:33] Off course not
[02:33] that should not be a proper way of handling for a mature language like Java.
[02:38] So Java always follow operators precedence in these kind of scenarios.
[02:43] So Java thinks about which operator has highest precedence between subtraction and multiplication.
[02:50] Multiplication has the highest precedence.
[02:53] That's why first it is going to perform the operation of 8 * 2 post that the expression is
[03:00] going to become 16 -16.
[03:03] And that's why we are going to get the output as zero.
[03:05] So here you may have a question where can I find all these operators, precedence details and associativity
[03:12] details.
[03:13] So for now don't worry about that
[03:15] in the next lecture I'm going to give a table
[03:17] inside that table I'm going to show you all the operators of Java, along with their precedence number
[03:24] and associativity details.
[03:26] For now, I'm assuming you are clear about these expression
[03:28] we are going to get the output as zero.
[03:31] In case if you are looking to change the way how Java evaluates your expression, then you can mention 16 - 8
[03:39] inside a parentheses.
[03:41] Like we discussed previously, whenever we are using the parentheses, then we are going to change the
[03:47] precedence because Java is always going to give first priority to evaluate the expression which is present
[03:54] inside parentheses.
[03:55] With this expression, the multiplication has highest precedence compared to the subtraction operator
[04:02] still, 16- 8 is going to be evaluated first because we have surrounded that expression with
[04:08] a parentheses.
[04:09] That's why the overall output from this expression we are going to get as 16.
[04:14] So if you have these kind of scenarios where you are looking to change the default to Java operators
[04:19] precedence values, then always parentheses is your silver bullet.
[04:23] So as of now we saw an expression where we have multiple operators and all these operators
[04:30] they have different precedence values.
[04:32] But sometimes we may have an expression which has multiple operators and all of them have same precedence
[04:40] value.
[04:40] For example, here you can see I have an expression which is 16 * 5 /
[04:47] and after the division operator I have two.
[04:50] In Java, both multiplication and division and modulus operator, all of them, they have a same precedence.
[04:57] So in this kind of scenarios how do you
[05:00] the Java is going to evaluate my expression.
[05:03] So when these kind of scenarios where all the operators have the same precedence, my Java is going
[05:08] to follow the associativity of the operators inside Java multiplication, division, and modulus operators
[05:16] they are going to follow the left to associativity,
[05:19] that means the expression is going to be evaluated from left to right. With that rule
[05:25] first, on the left hand side, expression is going to be evaluated.
[05:29] So 16 multiplied by five we are going to get the output as 80 and 80
[05:33] if you try to divide it with the 2 the overall output, we are going to get as 40.
[05:39] So that's what I tried to explain with the statement also here for your quick reference.
[05:43] But in these kind of scenarios, also, if you are looking to change the behavior of Java default precedence
[05:49] and associativity rules, you can use the parentheses.
[05:53] So you can see I have used the parentheses around five divided by two.
[05:58] So with this first my division operation is going to be performed.
[06:02] So five divided by two we are going to get the output as two.
[06:06] Was that 16 multiplied by two is going to be evaluated.
[06:10] That's why the overall output we are going to receive is 32.
[06:14] I hope you are clear.
[06:15] What is an associativity?
[06:17] We also discussed about these associativity previously for your reference
[06:22] I also mentioned more details about these associativity
[06:26] inside this slide.
[06:27] In Java, we have two types of associativity left associative and right associative.
[06:33] When an operator follows left associative, it is going to evaluate the expression from left to right,
[06:40] whereas if the operator follows right associative,
[06:43] in such scenarios, the expression is going to be evaluated from right to to left.
[06:48] For example, in the expression a+b+c, we have an operator which is addition operator.
[06:55] Addition operator
[06:56] we know it is always going to follow left associative.
[07:00] So that's why first a+b will be calculated.
[07:04] The result from the a + b will be added to the c.
[07:07] This way the calculation always going to happen from left to to right.
[07:12] Whereas if you take the another operator which is Assignment operator inside, the expression
[07:19] a = b = c.
[07:20] Since the Assignment operator is going to follow the right
[07:24] associativity,
[07:25] first, the assignment of c to b is going to happen.
[07:29] Post that the outcome from the b is equal to c is going to be assigned to the variable a.
[07:35] I hope you are clear.
[07:36] What is precedence and associativity?
[07:39] Let me quickly show you the behavior of these expressions inside IntelliJ.
[07:44] Inside my Intellige, I'm going to create a new class and the class name is going to be PrecedenceAssociativityDemo
[07:54] .
[07:55] In real projects
[07:56] don't try to give such a lengthy class name to make it more clear for you.
[08:00] I'm trying to give you a detailed Java class name.
[08:02] Once this class is created, I'm going to create a main() method by following the shortcut psvm.
[08:09] And here I'm going to write the same expression which is int calNum, calNum indicates calculated number.
[08:17] With this I'm going to assign an expression which is 16 - 8 * 2.
[08:23] So by default if you try to execute this program we are going to get the output as zero.
[08:28] The reason is since the multiplication operator has highest precedence,
[08:34] so first eight into two is going to be calculated.
[08:37] With that the overall expression is going to be 16 -16.
[08:41] And that's why we are going to get the output as zero.
[08:44] I can also try to confirm the same by printing the variable into the console.
[08:48] You can see we are getting the output as zero.
[08:50] If I want to change this behavior, I can do that by putting parentheses around my 16 - 8.
[08:58] And in this scenario, the output we are going to get is 16 because we change that default behavior.
[09:05] Very similarly
[09:05] let me build one more expression which is calNum to the same calNum variable,
[09:12] I'm going to assign an expression which is 16 * 5 / 2.
[09:18] With this I'm trying to perform multiplication and integer division.
[09:22] So by default with this expression we are going to get the output as 40.
[09:27] If I try to execute this program you can see we are getting the output as 40.
[09:31] Whereas if I want to change this behavior I need to put the parentheses around my division operation.
[09:38] And with that we are going to get the output with this
[09:41] I'm assuming your super clear about what is Java operators precedence and associativity.
[09:47] The only million dollar question right now you may have is what are the precedence values and associative
[09:55] values for all the operators that we have discussed so far?
[09:58] I'm going to answer
[09:59] your question in the next lecture.
[10:01] Thank you
[10:02] bye.

----------------------------------------
