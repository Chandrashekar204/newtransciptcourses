# 24.5 — How to build Lambda expressions

> Section 24: [JAVA 8] Functional Programming using lambda expressions

[00:00] Inside this lecture, let's try to understand how to define lambda expressions by taking normal Java
[00:07] methods as a reference.
[00:09] On the left hand side, you can see I have a normal Java method with the name print hello, and the
[00:15] return type of this method is void and the access modifier of this method is public.
[00:19] Inside this method I have a business logic just to print a hello world!
[00:23] By taking this method as a reference, let's try to define an equivalent lambda expression.
[00:29] We know the lambda expression does not going to have any name.
[00:33] That's why we don't have to mention these method name.
[00:36] And we don't have to mention these access modifier and return type.
[00:40] With that we can straight away start with the input parenthesis.
[00:45] Since my method is not accepting any input parameters, I have mentioned that empty parenthesis here.
[00:51] After the input parenthesis, we need to mention these lambda expression symbol, which is hyphen followed
[00:58] by greater than symbol.
[01:00] And after that these curly braces.
[01:03] You need to start and close.
[01:05] So inside these curly braces you need to write your business logic.
[01:09] The business logic that we want to write is System.out.println.
[01:13] And with the same we want to print these hello string.
[01:16] So this is the equivalent to lambda expression for this method.
[01:20] But like I said before, whenever your lambda expression body has a single Java statement or a single
[01:26] Java expression, you can remove these curly braces as well.
[01:30] And with that, this is how it is going to look like.
[01:33] So this is the simplest lambda expression that you can write whenever you have a single Java statement
[01:39] inside your business logic.
[01:41] So this is the example one.
[01:43] Similarly I have two more examples.
[01:45] But before we try to discuss remaining examples, let me try to build the lambda expression manually
[01:51] by taking these methods.
[01:52] So here I'm just giving a screenshot.
[01:54] But let me show you the process that I will go through whenever I try to build a lambda expression.
[02:00] So inside my text editor you can see I have a Java method.
[02:03] I'm not going to do this inside Intellige because we can't write lambda expression wherever we want.
[02:10] We can only define lambda expressions under the context of functional interfaces.
[02:16] I'm going to discuss about functional interfaces in the coming lectures.
[02:19] For now, let's try to get familiarized with the lambda expression syntax.
[02:23] So for this method, if I want to build a lambda expression, first I need to get rid of the method
[02:30] name access modifier and return type.
[02:33] I don't have to mention any of them.
[02:35] That's why I can straight away start with the parentheses.
[02:39] And since my print hello method is not accepting any input parameters, I have mentioned empty parentheses
[02:45] here post that I'm going to mention hyphen followed by greater than symbol.
[02:50] With that it is going to look like an arrow.
[02:52] So please make sure there is no space between the hyphen and greater than symbol.
[02:56] After this, we can mention that curly braces and inside these curly braces we can mention the business
[03:03] logic which is system dot out dot print.
[03:05] Hello.
[03:06] So this is one style of writing the lambda expression.
[03:08] The other style is.
[03:10] Since you have only a single Java statement inside your lambda body, you can get rid of these optional
[03:17] curly braces, and you can directly mention your single Java statement immediately to the Lambda symbol.
[03:24] So these are lambda symbol.
[03:26] Immediately after this lambda symbol, we need to give a space followed by your single Java statement.
[03:31] I hope you are clear.
[03:32] Now let's go to the second example.
[03:35] Inside my second example, you can see I have a method with the name ad, and this method is going to
[03:41] accept two input parameters of type int.
[03:44] The parameter names are Num1 Num2.
[03:46] Coming to the business logic that I have inside my method is, I'm trying to add both of my numbers
[03:52] and assign the output to the variable result.
[03:55] So the same variable result I'm trying to print out onto the console with the System.out.println.
[04:00] Let's try to build the equivalent to lambda expression for this method.
[04:05] As usual, we don't have to mention the public void add.
[04:09] Since the lambda expressions are not going to have any name, we can get rid of the name, and similarly,
[04:14] we don't have to mention the return type and the access modifier.
[04:17] With that, I can straight away start with the input parentheses and inside the input parentheses,
[04:23] I need to mention my input parameter names like num1 and num2.
[04:27] And the beauty of the lambda expression is we don't even have to mention the data type of your parameters.
[04:33] I'm trying to mention directly the Num1 and Num2.
[04:36] I'm not trying to mention into Num1 comma into Num2.
[04:39] With that, you may have a question, which is then how my Java compiler will know whether num1 is a
[04:45] int or a string, or a double, or a person.
[04:48] How does my compiler will know the data type of this Num1 and Num2.
[04:52] So that can be your question for now.
[04:54] Please hold your thought on this when we start discussing about the functional interfaces from the next
[04:59] lecture.
[04:59] It is going to be clear for you.
[05:01] So the point that I want to highlight here is whenever you are trying to mention the parameters list
[05:06] to your lambda expression, you don't have to mention their data type.
[05:10] They are completely optional.
[05:12] So that's why I'm trying to directly mention Num1 and Num2.
[05:15] And these parameter names also don't have to be the same like Num1 and Num2.
[05:19] Instead, you can also use a comma b as well, and post that we need to mention the lambda symbol followed
[05:27] by curly braces.
[05:28] So inside my curly braces, I'm trying to mention the same business logic like we have on the left hand
[05:33] side.
[05:34] So here, since I have two Java statements, these curly braces are mandatory, but if I can manage
[05:40] combining these two Java statements into a single Java statement like you can see here, in such scenarios
[05:46] we can get rid of these optional curly braces.
[05:49] So here in a single statement I'm trying to perform the addition and the result from this addition,
[05:55] I'm trying to assign directly to these println method.
[05:58] You may have many questions running behind the scenes.
[06:00] What are the advantages that we are getting by writing my business logic in the form of these ugly lambda
[06:06] syntax.
[06:07] So this can be all your questions.
[06:09] But believe me, once we master these lambda syntaxes and start using them inside our Java programs,
[06:15] it is going to bring you a wow feeling for you.
[06:18] That's why my humble request is please be patient here and first try to learn the basics of functional
[06:24] programming, which is on how to define an lambda expression.
[06:28] Let's try to build this lambda syntax manually by going to the text editor.
[06:32] Here I'm going to first delete all these previous example code post that I'm going to paste the method
[06:39] that we have discussed.
[06:40] So this is the method.
[06:42] The equivalent lambda expression for this method is we can straight away start with the input parameters
[06:48] inside these parentheses I'm going to mention the parameter name as num one comma num2.
[06:53] Please make sure whatever number of parameters that your method has the same number of parameters you
[06:58] you have to mention inside your lambda expression as well.
[07:01] After mentioning these input parameter details, I'm going to mention the lambda symbol followed by
[07:07] curly braces.
[07:08] Inside the curly braces I'm going to define these business logic.
[07:13] So this is one style of writing the lambda expression.
[07:17] But like I said before, if we can able to build a business logic within a single statement, then we
[07:23] can completely get rid of these curly braces.
[07:25] Like you can see here.
[07:27] I'm trying to get rid of this curly braces and post that.
[07:30] I'll try to remove these addition operation and bring these line next to the lambda symbol.
[07:37] And here I will try to mention same Num1 plus Num2.
[07:43] So whatever names that you have given here inside the parentheses, the same variables you have to use
[07:48] inside your lambda expression body as well.
[07:52] For example, it is not mandatory to use Num1 Num2 only like same as your method.
[07:58] Instead you can use a comma b representing two different numbers.
[08:03] But since the parameter names are mentioned as a comma b, we need to use the same variable names here
[08:08] like a plus b.
[08:09] Otherwise you're going to get a compilation error.
[08:12] So these are example two.
[08:13] Now let's try to take the third example.
[08:16] The third example is very similar to the example two, except that the return type of this method is
[08:21] going to be int.
[08:22] So after the addition I'm going to return the result as an output from this method.
[08:28] In this kind of scenario.
[08:29] Also you don't have to mention these public int and add.
[08:33] You can straightaway start with the parentheses.
[08:35] And inside these parentheses you can mention the parameter names like a comma b I'm trying to mention
[08:42] here.
[08:42] Mentioning these integer data type is optional inside the lambda syntax.
[08:47] After mentioning these a comma b, I'm trying to mention the lambda symbol followed by curly braces
[08:52] inside the curly braces.
[08:54] I have written all the business logic with these two Java statements.
[08:57] If I can able to combine these two Java statements into a single Java statement, then I can get rid
[09:03] of these curly braces as well.
[09:05] So here you can see I can straight away write return a plus B.
[09:10] But one more beauty of lambda expression is whenever you have a single Java statement inside your lambda
[09:16] expression body, mentioning the return is also optional.
[09:20] So whenever you're trying to define a logic with the help of lambda expression, and if you have a single
[09:25] Java statement, don't try to mention return keyword as well because it is completely optional.
[09:31] But here you can see I'm trying to mention the return keyword.
[09:34] The reason is here inside the lambda expression body we have multiple Java statements.
[09:39] So in this kind of scenarios mentioning the return keyword is mandatory.
[09:44] But like you can see here, wherever you have a single Java statement you can get rid of this return.
[09:50] So it is going to be optional.
[09:52] And here also you may have question which is nowhere inside my lambda expression.
[09:56] I have mentioned what is the return type of this lambda expression.
[10:00] Then how my compiler is going to validate.
[10:02] If I'm trying to return an int or a string or a double or a person object.
[10:07] Like I said, don't worry.
[10:08] When we start discussing about the functional interfaces, it is going to make more sense to you.
[10:13] Let's try to manually build this lambda expression by taking this Java method inside my text editor.
[10:18] I'm going to delete this previous example code and post that I'm going to mention the example three.
[10:24] So let's try to build the lambda expression for this method.
[10:28] So first we need to start with the parentheses.
[10:30] And inside the parentheses I'm going to give the name to my parameters like a comma b followed by I
[10:36] need to mention the lambda symbol.
[10:39] After the lambda symbol, I need to mention the curly braces inside my curly braces.
[10:43] I can copy paste these business logic, so when I copy pasted this business logic, I have the variable
[10:49] names as Num1 and Num2.
[10:51] With this I'm going to get a compilation error.
[10:53] Instead I should use a plus B.
[10:56] So this is one style of defining the lambda syntax for the example three method.
[11:01] The other style is.
[11:03] If we can able to merge these two statements into a single Java statement, then we can get rid of the
[11:09] curly braces for the same.
[11:10] Let me type return a plus b.
[11:13] So this is going to be a single Java statement.
[11:16] So in this kind of scenario I can get rid of the curly braces and straight away mention this statement
[11:21] just after the lambda symbol.
[11:23] So we need to mention return a plus b.
[11:26] We can surround this a plus b.
[11:27] So this is going to be the equivalent lambda expression for this Java method.
[11:32] But like I said before, whenever you have a single Java statement mentioning this return keyword is
[11:37] completely optional.
[11:38] That's why I'm trying to mention a plus B directly here.
[11:41] Do you see the power of lambda expression here?
[11:43] Just with a single line of small code?
[11:47] I'm able to implement a method now where I'm trying to create a class no where I'm trying to give a
[11:53] name return type.
[11:54] What is the data types?
[11:56] I'm trying to get rid of all those boilerplate code with the help of Lambda syntax.
[12:01] With the three examples that we have discussed so far, you might be clear on how to build the lambda
[12:06] syntaxes based upon a normal Java method, but still, you may have a lot of questions or confusion,
[12:12] like how my compiler will know how to invoke my lambda expression, what is the name it is going to
[12:17] use, how it is going to identify the data type of my input parameters, and how it is going to identify
[12:23] the return type of my lambda expression.
[12:25] So let's try to answer all these questions in the next lecture.
[12:29] Thank you.
[12:29] Bye.

----------------------------------------
