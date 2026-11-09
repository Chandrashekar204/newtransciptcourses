# 2.5 — Syntax to declare primitive data types & store data using them

> Section 2: Primitive data types in Java

[00:00] As of now we have basic idea about primitive data types.
[00:04] The immediate question that you may have here is, how can I store the data with the help of the primitive
[00:11] data types that we have discussed in the previous lectures?
[00:14] So let me try to explain you about the same inside this lecture.
[00:18] Whenever we want to store data with the help of primitive data types inside Java, we need to follow
[00:24] a syntax.
[00:24] So let's try to understand what is the syntax and the rules that we need to follow,
[00:28] while we are trying to store the data inside primitive data types think like I want to store a boolean
[00:35] value which is false using my Java programming language.
[00:40] In such scenarios, we need to write a Java statement, which is boolean b is equal to false, and
[00:46] at last we need to mention semicolon.
[00:48] So let's try to understand more details about this Java statement.
[00:51] The very first word that you can see here is boolean.
[00:55] So what is this boolean.
[00:56] It is a primitive data type.
[00:58] It is also a Java keyword which we can use to convey to the Java compiler that I'm trying to create
[01:05] a variable of data type boolean.
[01:08] And whenever you are trying to mention this boolean, please make sure you are mentioning the same spelling
[01:13] with the same case sensitive values.
[01:15] So all your alphabets inside boolean has to be lower case.
[01:19] After you have mentioned what is a primitive data type, you need to give a name to your variable.
[01:25] So the name that I'm trying to do here is a simple name which is b.
[01:29] So this b is going to act as a variable or an identifier using which I can store my data
[01:36] or I can try to read my data.
[01:38] So think like there is a memory location inside the system or inside the computer, inside that memory
[01:45] location
[01:45] my Java program is going to store the data that I'm trying to give, but whenever I want to access my
[01:51] data, I can't tell to my Java saying that, please go and fetch the data from so-and-so memory location.
[01:58] We can't do that because we never know where the Java is storing that value or data.
[02:03] So that's why,
[02:04] so to overcome this challenge, we need to have the variable name or identifier name.
[02:09] So if I tell to my Java please fetch me the data present inside the variable or identifier b it's internally
[02:17] knows where that data is going to be available.
[02:20] So it will go to that memory location and fetch the data and give it to me.
[02:24] And based upon the value that I receive, I can execute any business logic.
[02:28] Once you have defined this variable name or identifier you need to mention is equal to.
[02:33] After is equal to,
[02:34] you need to mention what is that data that you want to store here?
[02:38] I want to store the data
[02:39] false.
[02:40] So this data or this value we call it as literal.
[02:44] In other words we can also say it as variable value.
[02:47] So regardless of whatever name that we try to use, whether it is a literal or whether it is a variable
[02:53] value, please always make sure you are mentioning the variable value only and the right hand side
[02:58] after mentioning that is equal to like you know, every Java statement has to be terminated with a semicolon.
[03:05] That's why we need to mention the semicolon value.
[03:08] Are you clear about this syntax.
[03:10] So let's try to do this exercise one more time with a different primitive data type. Like you can see
[03:15] here,
[03:16] this time I'm trying to use a into primitive data type. Using into primitive data type,
[03:21] I'm trying to create variables and try to assign the values to them.
[03:25] But this statement is tricky compared to the previous statement.
[03:29] In the previous statement, we only created a single variable and we assigned a value to that variable.
[03:34] But here you can see I have two variables I, j because I have separated them with the help of comma.
[03:41] So with this statement first my Java compiler will look int i.
[03:44] That means it will assume i is a variable.
[03:47] So for i variable did I assign any value?
[03:50] I didn't assign any value.
[03:52] That's why behind the scenes my Java compiler is going to assume a default value for the i.
[03:58] So what is the default value for into primitive data type?
[04:01] It is zero, so it is going to assign zero to the i.
[04:05] Whereas for the second variable which is j, I assign the literal value with the help of is equal to.
[04:11] So after is equal to,
[04:12] I have mentioned 8.
[04:13] So with this my Java is going to assign a value eight to the j variable.
[04:19] So this way you can create any number of variables using a single Java statement.
[04:25] So please make sure you are separating all your variables with the help of comma.
[04:29] In case if you want to assign a value to the i also, then the Java statement is going to be int i is
[04:35] equal to two comma j is equal to eight.
[04:38] In such scenarios, the literal value two will be assigned to the i, whereas for the j it is going
[04:44] to be eight.
[04:44] So if you try to observe both of these statements, whatever we are trying to perform here, we call
[04:49] it as declaration and initialization.
[04:53] In the very first statement, which is boolean b is equal to false.
[04:56] I'm trying to do both the declaration of variable
[05:00] and initialization of variable with the data.
[05:02] So b is a variable which I have declared, and I also initialize a b with a literal value, which is
[05:09] false.
[05:09] So that's why whenever we are trying to declare a variable and assign a literal immediately, we are
[05:14] going to call that as both the declaration and initialization. In the second statement
[05:20] also, I'm trying to do both the declaration and initialization for the j variable, whereas for i variable
[05:27] I have done only declaration.
[05:29] Now let's try to understand how to not declare and initialization in a single statement. Like you can
[05:35] see here,
[05:36] I have mentioned a statement which is double num and semicolon value.
[05:40] So here you can see I simply mentioned what is a primitive data type that I want to use which is double
[05:46] and what is a variable or identifier name.
[05:49] So the variable name that I have given is num.
[05:52] So for this num variable we are not trying to initialize any value.
[05:56] So behind the scenes my Java is going to hold that default value inside this num.
[06:03] The default value is going to be 0.0 for double. Later on
[06:08] if you want to change you can write one more Java statement, which is num is equal to 1.0 or 6.0 based
[06:15] upon your requirements.
[06:16] So that way we can also do declaration and initialization in two different Java statements.
[06:23] I'm going to show you that in practice in few seconds.
[06:26] I hope you are clear about what is declaration and initialization.
[06:30] If you still have some questions, don't worry
[06:32] I'm going to give you a real example here.
[06:34] Think like you have an habit of drinking coffee.
[06:37] If you try to compare these declaration and initialization with the coffee scenario, with the declaration,
[06:43] we are going to have a empty cup in your hand, whereas with the declaration and initialization you
[06:51] are going to have a cup, and inside the cup you're going to have full of coffee.
[06:56] Off course, you may argue here like there'll be a default value if you follow only declaration.
[07:02] I agree with you to some extent
[07:04] we can't say the cup is completely empty, but when we try to discuss the same concept of declaration
[07:11] and initialization with the reference data types or the complex data types.
[07:16] Whenever we do only declaration, then that particular variable of reference data type is going to have
[07:22] a null value or empty value.
[07:24] So it is going to make more sense to you when we try to discuss complex data types or reference data
[07:30] types in the coming sessions.
[07:31] But I can still feel here
[07:33] we can take this as an example.
[07:35] Even in the case of primitive data types.
[07:38] I hope you are clear about the syntax that we need to follow while we are trying to store the data with
[07:43] the help of primitive data types, please make sure you are always mentioning the literal value on the
[07:50] right hand side.
[07:50] So whatever value that you have mentioned on the right hand side, it is called as literal.
[07:55] These literals
[07:56] they will include the integer or decimal numbers or single characters, or the boolean values like true
[08:02] or false.
[08:03] You should be able to see at the end of the slide
[08:05] I have mentioned some example values that we can assign to the primitive data types. So 1 we can
[08:12] use for all data types like byte, short, int, long, whereas 1.0 we can use for float and double.
[08:19] Since they are going to support decimal values 'M' and 'f' in a single quotes, we can use them in the scenario
[08:27] of char data type true and false.
[08:29] You already know we can use them for boolean data type.
[08:32] So now let's try to take this knowledge and try to create some variables literals with the help of primitive
[08:40] data types in the next lecture.
[08:42] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
