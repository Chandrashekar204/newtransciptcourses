# 7.10 — String Concatenation Operator

> Section 7: Operators in Java

[00:00] We previously discussed that whenever you are trying to provide two numeric operands to the plus operator,
[00:07] it is going to perform pure mathematical addition operation.
[00:11] Whereas if one of the operand is of type String, then it is going to act as an string concatenation
[00:18] operator.
[00:19] Around this we also discussed various examples previously.
[00:23] For example, if you try to mention plus operator between Hello and world, it is going to concatenate
[00:29] both of them and the output is going to be hello world.
[00:32] But around this String concatenation operator
[00:35] also there are some special scenarios or there are some puzzle scenarios which you need to be aware.
[00:40] So that's why inside this lecture I'm going to give a few puzzles and I'll ask you what will be the
[00:46] output once we are done with the guessing of the output, I'm going to explain what are the reasons
[00:52] that we have on getting a specific output.
[00:55] So can we start this puzzles ?
[00:57] So here is your first puzzle.
[00:59] So I have an expression four 4 + 2 + "goals".
[01:03] So here what is the output
[01:05] you are thinking whether I am going to get 6 goals or 42 goals based upon our assumption,
[01:11] if one of the operand is String, then addition operator is going to purely convert other operands also
[01:19] as strings and concatenate all the string.
[01:22] With that assumption our clarity you may think like output we are going to get is 42 goals,
[01:29] but we are not going to get 42 goals,
[01:32] instead, we are going to 6 goals as an output.
[01:36] So let's try to understand the reason behind it.
[01:39] For the same,
[01:39] here I'm going to create an String which is output.
[01:44] And to this output String I'm going to assign 4 + 2 + another String where I'm going to mention
[01:52] space goals.
[01:53] So if I try to execute this program by putting a breakpoint here, we'll be able to see what is the
[01:59] runtime value under output.
[02:02] So you can see we are getting 6 goals.
[02:05] Do you know what is the reason I'm going to give you a clue for you here.
[02:09] Think about the associativity of the plus operator.
[02:12] So how it is going to evaluate an expression?
[02:15] Is it from left to right or right to left?
[02:18] Based upon our previous discussions, the plus operator is always follow left associativity.
[02:25] That means it is always evaluate the expression from left to right.
[02:30] With that assumption, it is going to start first with the 4 + 2,
[02:34] so since both of them are numeric values, it is going to perform the mathematical addition operation
[02:41] and four plus two is going to perform six.
[02:44] That means the expression is going to become as 6 + goals. In this expression,
[02:52] now my plus operator has two operands and one of the operand is String.
[02:57] Since one of the operand is String, the other one is also going to be converted as an String, and
[03:03] it is simply going to perform the pure string concatenation operation, and the output is going to be
[03:10] 6 goals.
[03:11] I hope you are clear.
[03:12] Can we move on to the next puzzle?
[03:15] So here I'm using the hard coded numeric literal values.
[03:19] You will be able to see the same behavior even if you use the int variables like I can use num1 + num2,
[03:27] and I can define this num1 and num2 here as 4 and 2.
[03:33] With these also, you're going to get the same behavior, which is 6 goals as an output.
[03:38] The same applies for String
[03:39] also, instead of hard coding the value here, you can try to assign this to another String variable
[03:46] here, the variable name can be String str1.
[03:49] And to this variable I can assign the value space goals.
[03:53] And now here I can mention the variable name which is str1.
[03:58] Even in this scenario also the output is going to be the same which is 6 goals.
[04:04] I hope you are clear.
[04:05] Let me release this breakpoint.
[04:07] Now are you ready for the next puzzle?
[04:09] For the next puzzle, I'm going to write an expression which is output = num1 + parentheses
[04:18] and inside the parentheses I'm going to write num2 + str1.
[04:24] So what is the output you are thinking here?
[04:27] Like we discussed before, whenever we have an expression between the parentheses, then the associativity
[04:34] and the precedence rules will be ignored by your Java compiler or JVM.
[04:40] Always the first priority will be given to the expression which is present within the parentheses.
[04:46] With that
[04:47] now the calculation will not start from the num1.
[04:50] Instead, first this expression is going to be evaluated.
[04:54] So what will be the expression num2 + str1.
[04:59] Since str1 is of type String,
[05:01] num2 is of type int.
[05:03] The String concatenation will happen and the output from this expression is going to be 2 space goals.
[05:10] With that, the expression will become like num1 + 2 goals.
[05:16] So with this expression now the addition operation will start from the left hand side.
[05:20] So num1 is an int whereas the second operand is an String operand.
[05:26] That's why the String concatenation is going to happen.
[05:29] And the output we are going to get is 42 space goals.
[05:33] We can also confirm the same by running the program
[05:36] and this time you can see under the output we have 42 goals.
[05:41] This way whenever you have some requirements where you want to change the associativity of an operator,
[05:47] or if you want to ignore the priority of an other operators, you can always give highest priority to
[05:54] your expression by providing these parentheses.
[05:57] I hope this is clear.
[05:58] Now let me give the next puzzle.
[06:00] The next puzzle is also going to be on the similar line.
[06:03] So let me take this line of code and paste it here and remove the parentheses that I have here.
[06:10] After removing these parentheses, I am going to mention an empty String value at the starting, and
[06:17] I'm going to add the same to the remaining expression.
[06:20] With this, we are going to get the same 42 goals as an output.
[06:24] The reason is in this scenario we have not given any parentheses
[06:28] that's why the execution will start from the left hand side.
[06:32] So the very first operand that we have here is String.
[06:35] So String + num1 will convert to a num1 value for as an String value.
[06:41] So this expression is going to become like four in the String format + num2 + str1.
[06:50] So four is a String and num2 is an integer.
[06:53] So string plus integer will again do the String concatenation.
[06:57] And the expression is going to convert as four to in string format followed by str1.
[07:04] And at last we are going to get an output which is 42 goals in an String format.
[07:11] So this is how it is going to work the same behavior.
[07:14] You can also see if you try to mention these empty String just after the num1.
[07:19] So here also we are going to get the same behavior.
[07:22] I hope you are liking these puzzles.
[07:24] Let me give one more puzzle here.
[07:26] This time I'm going to create a boolean variable with the name b, and inside this boolean variable
[07:33] I'm going to store a value false.
[07:35] Now I can take this Java expression and paste it just after the boolean variable and remove this empty
[07:43] String value.
[07:44] With this we know what is the output we are going to get.
[07:46] We are going to get 6 goals as an output. But this time I'll mention b + num1 and you
[07:54] can see we are getting a compilation error.
[07:56] Do you know what is the reason, inside this syntax
[07:59] the addition operation will start from the left direction and b is a boolean and num1 is an int.
[08:06] Like we discussed before, we cannot use boolean data type values as part of the addition operation.
[08:13] That's why we are getting these compilation error.
[08:15] So to resolve this compilation error I can try to put parentheses around the right hand side expression.
[08:22] So with this now my num1 + num2 + str1 will be executed first.
[08:28] And the output from these inner expression is going to be 6 goals.
[08:34] And with that this entire inner expression is going to have an String value.
[08:40] And the expression is going to be converted as b +
[08:44] and what is the string value we are going to have.
[08:46] It is going to be String goals.
[08:50] Now one of the operand we are going to have as string and the other operand is boolean.
[08:55] When we are using string concatenation operator, any kind of other operand will be eventually converted
[09:01] to a String value.
[09:03] So the output from this expression is going to be
[09:06] false 6 goals.
[09:09] We can also confirm the same by running these program.
[09:12] So let me run this program.
[09:14] You can see under output we have the value which is false 6 goals. I hope you are clear,
[09:22] if you don't like using these parentheses, you can simply copy this expression and remove the parentheses.
[09:30] After removing the parentheses, you can mention the empty String just before the b or just after the
[09:37] b variable.
[09:38] And with that, this addition is going to act as an String concatenation and there won't be any compilation
[09:45] errors.
[09:46] Moving on to the last scenario, this scenario is about the null value inside the String objects.
[09:52] So first let me try to create an String variable with the name str2 and inside this str2,
[09:59] I'm going to store a null value and post that
[10:02] I'm going to create one more String variable which is str3.
[10:06] And to this I'm going to assign an expression which is 6 + str2.
[10:12] Very similarly I can also write one more expression which is string str4 is equal to instead of
[10:18] six
[10:19] I'm going to mention goals.
[10:20] So if you try to execute this program, you'll be able to see that str3 is going to have a String
[10:27] value which is 6null.
[10:29] And str4 is going to have a string value which is goalsnull.
[10:34] That means whenever you are trying to concatenate your String variables or String literals with the
[10:41] null variable,
[10:42] the null variable value is also going to be appended to your String.
[10:47] But here there is a special scenario which you need to be aware, to show you the same
[10:51] let me release this breakpoint.
[10:53] The special scenario is whenever you are trying to use concatenation operator by mentioning that direct
[10:59] null values like 6 + null, you are going to get an compilation error.
[11:05] Because my concatenation operator does not know this null belongs to the String object or Person object.
[11:12] That's why this plus operator is not going to be either normal addition or String concatenation.
[11:19] Whereas if I try to mention this String in an integer format, then this plus operator is going to act
[11:25] as an String concatenation.
[11:27] That's why never try to append that direct null values to the numerical data types, like 6.
[11:34] Instead, the approach that you need to follow is you need to make sure at least one of the operand
[11:39] is of type String.
[11:41] So instead of mentioning this null directly, you you can use this str2.
[11:45] And with that your plus operator will know that you're trying to add the null representation of the
[11:52] String object, and it can act as a string concatenation operator.
[11:56] I hope you are clear about all the scenarios and puzzles that we have discussed.
[12:01] I also mentioned about all the puzzles that we have discussed, along with the explanations on why we
[12:07] are going to get a given output, so please refer them whenever you have some questions with this discussion.
[12:13] I'm assuming right now you are clear on how the precedence and associativity is going to work inside
[12:20] Java.
[12:21] And here you may have $1 million question, which is how do I know what is the associativity or priority or
[12:28] the precedence of a given operator. So don't worry about them
[12:32] I'm going to give you a good tabular explanation at the end of this section, where inside the table
[12:38] you will be able to find all the details like what is the precedence number or the priority number of
[12:43] an operator, along with the details whether the given operator is left associative or right associative.
[12:51] I hope you're clear.
[12:52] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
