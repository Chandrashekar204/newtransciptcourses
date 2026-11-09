# 7.8 — Addition Operator in Java - Part 1

> Section 7: Operators in Java

[00:00] Let's start discussing in detail about the Arithmetic operators.
[00:04] So this slide is going to give a very quick summary about addition, subtraction, unary minus and multiplication
[00:11] operators.
[00:12] With the help of plus operator we can perform two kind of operations.
[00:16] If you are using these plus operator between two operands, then it is going to act as an addition.
[00:22] If the two operands are pure numeric values, it is going to be mathematical addition like
[00:29] 8+ 8 = 16.
[00:30] Whereas if one of the operands is a String, then definitely it is not going to act as an mathematical
[00:37] addition.
[00:38] Instead, it is going to perform the String concatenation which we discussed previously.
[00:43] Apart from addition and string concatenation, whenever you use this plus operator with a single operand
[00:50] like a numeric value, then in such scenarios, the plus operator is going to use to express a positive
[00:57] number like plus 16.
[00:59] Now coming to the subtraction, with the help of this minus operator or hyphen operator, we can subtract
[01:06] two numeric values.
[01:07] And this subtraction operator we cannot use with the String variables.
[01:12] The plus symbol is the only Arithmetic operator that we can use with the String variables.
[01:18] So subtraction symbol also can be used both with the two operands and a single operand.
[01:24] If you are using with two operands, it is going to perform the simple subtraction.
[01:28] Whereas if you are using this hyphen or minus on top of a single operand, in such scenarios it is going
[01:35] to act as an unary minus operator.
[01:38] We can use this unary minus operator to represent a negative values or negative numbers.
[01:45] So you can see here int negativeNum = -8 is used to represent the negative value
[01:51] of eight.
[01:52] If you try to perform this minus two times, like you can see in the second statement, minus of minus
[01:58] is going to become a positive number.
[02:00] And after this unary minus you can see we have a multiplication operator which is asterisk.
[02:06] With the help of this asterisk symbol, we can perform multiplication of two operand numeric values
[02:12] like eight
[02:13] asterisk two will give you the result, which is 16.
[02:16] So this is a very quick introduction about these operators.
[02:19] But let me try to discuss more details about the addition operator.
[02:23] When I say addition operator or an addition, you might be thinking it is very simple.
[02:29] We can always use this operator to add two numeric values, or we can also use this on top of a string
[02:35] variable to perform the string concatenation.
[02:37] But apart from this, there are some special scenarios and rules also that you need to be aware if you
[02:44] want to climb yourself as an master of Java.
[02:47] So let's try to understand what are those rules?
[02:50] In the simplest form, we can perform addition of two numerical operand values like four plus seven
[02:57] will give the output as 11.
[02:59] Apart from numeric literal values, we can also use this operator on top of variables, expressions,
[03:06] or method calls.
[03:07] So whenever you use this addition operator, the resultant data type follows certain rules.
[03:13] You need to understand those rules because these rules carry significant consequences.
[03:19] So the very first rule is if one of the operand is a double value, then the other second operand is
[03:26] also automatically converted to double and the resultant data type is going to be of type double.
[03:32] Whereas if one of the operand is float, then the other one is also going to be converted to float,
[03:38] and the resultant data type is going to be float.
[03:41] Here you may have question which is what if one operand is double and the other operand is float?
[03:46] In such scenarios, the first priority will go to the first rule since one of the operand is double,
[03:51] then other float operand also is going to be converted to double.
[03:55] The third rule is if one operand is long, then the other is also going to be converted to long and
[04:01] the resultant value is going to be of type long.
[04:05] If none of the above rules applies, then all operands are converted into int and the resultant value
[04:13] is going to be of type int.
[04:15] So please remember this fourth rule.
[04:17] It is very very important to discuss about this fourth rule
[04:20] I'm going to give you an example.
[04:23] First thing like you have declared a variable num1 of type byte.
[04:27] And to this num1 variable you are trying to assign a value eight.
[04:31] So this works perfectly.
[04:33] There won't be any issues inside your Java code and very similar lines
[04:37] let me show you another example where we are trying to assign the eight numeric value to the byte data
[04:44] type variable, like you can see here, I have num1 and num2, num3 byte data type variables num two holds
[04:51] five and num3 holds three.
[04:53] If I write an expression which is num1 = num2 + num3, I'm going to get a compilation
[05:00] error.
[05:00] We'll go in detail why I'm going to get an compilation error, but here you might be surprised.
[05:05] The same eight value and the left hand side we are able to assign to the num1 without any issues.
[05:12] Whereas on the right hand side example, if I'm trying to use the plus operator and try to combine five
[05:18] plus three as an eight and assign to the num1 and getting an compilation error, do you know why
[05:24] we are going to get compilation error?
[05:25] This is due to the rule number four.
[05:28] If none of the operand is double float and long, then all your operands are going to be converted to
[05:35] int and the resultant type is also going to be int.
[05:39] So to understand more details about it, let's try this example inside IntelliJ IDE.
[05:44] Inside my intelliJ I'm going to create a new class and the class name I'll keep it as AirthmeticOperatorDemo
[05:52] .
[05:54] So this is the class name.
[05:55] Inside this class I'm going to create public static void main() method.
[05:59] Here
[05:59] first let me try to create a variable byte num1.
[06:03] And to this num1 variable I'm going to assign a value eight.
[06:07] So with this you can see there is no compilation error
[06:10] I'm able to assign a value eight to the byte variable.
[06:14] But if I try to assign the same eight value with the help of Arithmetic plus operator, I'm going to
[06:20] get an error.
[06:21] Let me show you that very quickly.
[06:22] For that first I'm going to create byte num2 variable.
[06:27] And to this I'm going to assign a value five followed by I'm going to create a num3 variable with
[06:34] a value three post that
[06:36] I'm going to perform the addition operation with the help of a Java expression, which is num1 = num2 + num3
[06:43] num1 = num2 + num3.
[06:46] You can see as soon as I write these expression I'm getting a compilation error.
[06:51] Let's try to understand why we are getting these error.
[06:54] To understand these error, you need to look at the rule number four one more time.
[06:58] If none of the above applies, all operands are going to be converted to int.
[07:04] So as of now, what is the data type of num2 and num3
[07:08] those are bytes.
[07:09] That means these byte data type variables
[07:12] they are going to be converted to int variables because I'm using this plus operator and this plus operator.
[07:19] If my operands are not double float and long, it is simply going to convert them into int data type.
[07:26] So the conversion is going to happen like byte two int.
[07:30] So the automation conversion of byte to int will happen behind the scenes.
[07:35] And what will be the output from these num2 + num3.
[07:39] The resultant type is also going to be the int data type.
[07:43] And this resultant int data type
[07:46] we are going to assign to an num1 which is of type byte.
[07:50] So since we are trying to downgrade an into to the byte, we are getting an compilation error.
[07:57] So how to resolve this?
[07:59] To resolve this, first we need to surround these num2 + num3 with a parenthesis followed
[08:05] by we need to typecast the result from this expression into the byte.
[08:10] So to typecast the int to the byte, we need to use this byte typecasting.
[08:15] With that, you can see we are able to resolve the compilation error.
[08:20] The same kind of behavior you can see if you use short as well instead of byte.
[08:25] So that's why whenever you are trying to use byte and short to perform the Arithmetic addition operation,
[08:32] then please make sure you are aware about the rule number four that we have discussed.
[08:37] So this can be a trickiest question that you can face inside your Java interviews.
[08:43] Here you may also have a thought why we should mention these parentheses around num2 + num3.
[08:49] Can't we simply write num one is equal to byte typecasting followed by num2 + num3.
[08:58] So this is not going to resolve your compilation error.
[09:02] There are two reasons for this.
[09:04] The very first one is inside this expression you have two operators.
[09:09] One is the plus operator and the other one is the casting operator.
[09:13] Casting is also an operator inside Java.
[09:17] If you try to use multiple operators inside Java, then Java compiler or JVM is going to consider the
[09:24] priority like which operator has the highest priority.
[09:28] So the operators which has higher priority, they will be calculated or they will be processed first.
[09:34] So inside this expression, since the casting operator has an highest precedence, this expression is
[09:41] going to be evaluated which is byte of num2, num2
[09:46] you are trying to typecast to byte, but num2 is already byte post that this byte num2 you are
[09:53] going to add to the num3 with the help of this plus symbol, because plus has lowest priority.
[09:59] And with that, you will go back to the same problem where you are trying to append the two byte operands,
[10:05] and the plus operator is going to convert them into the int operand value.
[10:10] And the resultant from the addition is going to be the int.
[10:13] And since num1 cannot hold the int data type value, you are going to get a compilation error.
[10:20] So this is one reason.
[10:22] The other reason is you might be thinking why my JVM did not perform num2 + num3 first,
[10:29] instead why it is trying to come from this direction, which is byte num2 + num3.
[10:35] This is because the addition operator follows left associativity,
[10:40] that means it is
[10:42] always evaluate the expression from the left hand side to the right hand side, so this is entirely
[10:48] an expression.
[10:49] Once this expression is calculated, a final value will come from this expression.
[10:55] The same is going to be given to the assignment operator that we have here.
[11:00] So assignment operator always try to execute from right to left.
[11:05] That's why it is keep waiting for these right side operation to complete.
[11:09] Whereas the addition operator always try to evaluate from left hand side to the right hand side.
[11:15] That means it will not perform num3 +num2.
[11:18] It is always going to perform num2 + num3.
[11:21] On top of these associativity rule, we also have priority rule as well, since this typecasting operator
[11:29] has highest priority compared to the addition operator.
[11:32] First, this byte of num2 is going to be executed, which will make num2 as byte and the byte
[11:39] num2 value is going to be added to the byte num3, which will make your entire resultant as
[11:45] an int value.
[11:46] So how to resolve this whenever you have these kind of situations, if you want to override the priority,
[11:53] then you can simply mention parentheses or brackets around your expression.
[11:59] So with this change, whatever expression that we have inside the parentheses or the brackets
[12:05] it is going to be always executed.
[12:08] Post that only the other operators will be considered inside the expression.
[12:13] So what is the other operator?
[12:15] The other operator that we have here is typecasting
[12:18] operator.
[12:19] So here you may also ask me this
[12:21] typecasting also has brackets here
[12:23] or parentheses here.
[12:25] Please note that there is a difference between these expression and this,
[12:29] this is an operator,
[12:30] this is not an expression.
[12:31] Whereas inside these parentheses we have an expression.
[12:35] So that's why always Java compiler or JVM is going to give first preference to these num2 + num3
[12:41] post that the typecasting will be done with the help of this casting operator.
[12:46] And at last, once all this is converted into an byte, the same will be assigned to the num1 with
[12:53] the help of this assignment operator.
[12:55] I hope this scenario is super clear for you.
[12:57] I have mentioned all the points that we have discussed in this slide, and in the next slide as well.
[13:03] Please always refer them if you have any questions about the precedence order and about the associativity
[13:10] of the addition operator. We need to discuss more about the addition operator.
[13:15] Let's try to continue this discussion in the next lecture as well.
[13:18] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
