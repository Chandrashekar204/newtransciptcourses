# 8.16 — Deep dive on for loop - Theory

> Section 8: Control flow statements in Java

[00:00] Inside Java
[00:01] we can also build the looping logic with the help of for loop as well.
[00:06] As of now, we discuss everything about the while statements and do while statements.
[00:10] For the next few lectures we are going to focus on for loop and for loop is the most commonly used looping
[00:17] logic compared to the while loop.
[00:19] So for loop has its own advantages.
[00:21] So first let's try to understand what is the syntax that we need to follow whenever we want to build
[00:27] a Java logic with the help of for loop.
[00:29] Like you can see here, every for loop has to start with the for keyword.
[00:34] After mentioning the for keyword inside the parentheses, you're going to write three expressions.
[00:40] The very first expression we call it as initialization, the second expression we call it as condition,
[00:47] and the third expression we call it as update expression.
[00:50] So all these expressions they have to be separated with the semicolon.
[00:54] So let's try to understand what is the purpose of all these expressions.
[00:58] The initialization statement or the initialization expression that you are going to write inside the
[01:03] for loop
[01:04] it is going to be executed only once before your for loop starts and usually we use these initialization
[01:13] expression to initialize the looping related variables.
[01:17] After the initialization we have condition expression.
[01:20] So this condition expression or condition statement
[01:23] it is going to be evaluated at the beginning of each iteration.
[01:28] If you define your for loop to be executed for ten times, so whenever the iteration is about to be
[01:34] executed, this condition will be evaluated.
[01:38] And if this condition returns true, then only the for loop iteration will continue.
[01:43] Otherwise the execution of the for loop will be terminated, and the last expression that we have is
[01:49] update expression or the update statement.
[01:51] With the help of this update statement, we can write an update logic, which is going to be executed
[01:58] after each iteration.
[02:00] When I show you some examples and when we discuss some examples, it is going to make more sense to
[02:05] you.
[02:05] For now, please note that each for loop they are going to have three parts initialization, condition
[02:11] and update all of them
[02:13] they have to be separated with the semicolon.
[02:16] So once you have defined this, you need to mention the curly braces.
[02:19] And inside the curly braces you can write your Java statements which are going to be executed multiple
[02:25] times based upon the conditions that you have defined.
[02:28] And here you may have a question which is when to use the while loop and when to use the for loop.
[02:34] The answer is very simple.
[02:36] There is no strict rule that you need to use while loop, or you need to use for loop
[02:41] in these kind of scenarios, you can use any kind of approach, but in general for loop is going to
[02:47] be used when you know how many times you want to iterate in advance.
[02:52] For example, if you clearly know that you're going to execute your for loop only ten times in such
[02:59] scenarios, going with the for loop is going to make more sense compared to the while loop.
[03:04] I hope you are clear with the syntax of the for loop.
[03:07] Now let's try to take an real life example to understand this
[03:11] for loop. Think of the same childhood scenario where when a child is suffering from the flu, the parents,
[03:17] they are going to take their kid to the doctor.
[03:19] This time the doctor is going to write a prescription such a way that please give the syrup for the
[03:26] next five days.
[03:28] So here the parents know that they have to give the syrup only for the five days.
[03:32] So for these kind of scenarios, we can write the for loop saying that first we can perform the initialization.
[03:39] So I'm trying to declare a variable which is int day = 1 .
[03:43] So when my for loop is about to be executed very first time, we are creating a variable day and assigning
[03:49] a value one and post that we have written an condition expression
[03:53] or condition statement, which is day less than or equal to five.
[03:58] So whenever the for loop is about to be executed, a particular iteration each time it is going to evaluate
[04:05] this condition.
[04:06] If this is true only then the for loop is going to be executed.
[04:10] Otherwise it is going to terminate the execution of the for loop.
[04:13] And at last, under the update expression, you can see I'm trying to update the day variable by adding
[04:19] one with the help of post increment operator.
[04:22] So with this you can see we have all kind of control within the for loop itself.
[04:28] Whereas inside the while loop we need to define these variables outside and we need to do the increment
[04:34] of this day variable inside the while loop.
[04:36] Whereas with the help of for loop, we can define the loops in a more compact manner.
[04:42] So this for loop it is going to execute five times.
[04:45] After each iteration, the day variable is going to be incremented by one.
[04:50] At some point of time this condition is going to become false, and with that, the execution of the
[04:55] for loop is going to be terminated.
[04:58] Let's see one more example of
[04:59] for loop.
[05:00] This time my requirement is to print the file table like 5 * 1 = 5,
[05:06] 5 * 2 = 10.
[05:07] So I want to print the five table up to the multiplier of ten.
[05:12] So for these kind of requirements also we can use a for loop.
[05:15] Like you can see this is the logic that I have written.
[05:18] So first we are trying to initialize the i variable with the one since we want to start with the
[05:25] 5 * 1.
[05:25] So I have mentioned the multiplier as one, and I want to do the multiplication up to the multiplier
[05:32] ten.
[05:32] That's why the condition I have defined is I less than or equal to ten.
[05:37] And post that I'm trying to increment my i operator by one after each iteration.
[05:43] That's why I have defined i++ and inside the for loop you can see,
[05:48] first I'm trying to multiply i with the five.
[05:52] So during the first iteration of the for loop the i value will be one.
[05:56] So 1 * 5 = 5 will be the result.
[05:58] So the same I'm trying to print with the help of this println() statement.
[06:02] So five asterisk I'm trying to mention as a hard coded String value.
[06:07] Because this five asterisk is always going to be the same post that I'm trying to append the value of
[06:14] i, and after appending this value I'm mentioning is equal to.
[06:18] And at last I'm trying to append the value of result.
[06:22] So when you try to execute this program, your output is going to look like this.
[06:26] Like five asterisk one is equal to five five asterisk two is equal to ten.
[06:31] So this multiplier like one two, three up to the ten were able to control with the help of this i variable.
[06:38] Once the i variable reaches to the 11 the for loop execution will be terminated.
[06:44] I hope with this example it is more clear for you.
[06:46] So this style of for loop we call it as traditional for loop.
[06:50] But inside Java there is one more compact form of for statement is also available.
[06:56] The name of that for loop is for each or enhanced for loop with the help of this for each or enhanced
[07:04] for loop.
[07:04] We can further compact the for loop syntax.
[07:08] This for each and enhanced for loop is more useful in the scenarios of iterating the elements of an
[07:15] array or the elements of an collection object.
[07:18] So when we start discussing about the arrays and the collections inside Java in the coming sections,
[07:24] I'm going to explain you about the for each and enhanced for loop.
[07:28] Right now, I can't give you a demo because we're ready to discuss about the arrays and the collections.
[07:33] So more details about this for each
[07:34] we are going to discuss in the coming sections.
[07:37] As of now, you should be pretty clear about how to use the for loop, and inside each for loop we are
[07:43] going to define three different expressions like initialization, condition and update expressions.
[07:49] So there are certain rules that you need to be aware regarding each of these expressions.
[07:54] So let's try to understand what are those.
[07:56] Whenever you are trying to define an initialization section for a for loop statement inside that expression,
[08:03] you can either include a variable declaration statement or declaring one or more variables of the same
[08:10] type, or you can mention list of expression statements separated by commas.
[08:15] So all these are allowed to define inside the initialization section.
[08:20] So let me give some examples here.
[08:23] Inside the very first example you can see I'm trying to declare two variables i and j.
[08:29] And this is completely allowed inside a for loop.
[08:32] But please make sure both i declaration and j declaration they are separated with the comma but not
[08:39] the semicolon.
[08:40] So semicolon between the multiple expressions of your initialization is not allowed.
[08:47] We should always use the comma.
[08:48] So here I'm trying to declare two variables which belongs to the same data type.
[08:54] But if I try to do the same by using different data types like here
[08:58] first I'm trying to declare an int post that I'm trying to declare a variable j of type double.
[09:05] So this is not allowed because you're trying to declare variables of two different types.
[09:11] So that's why this statement compilation is going to fail.
[09:14] Just like variables declaration, we can also write some expressions as well inside the initialization
[09:21] section of for loop.
[09:22] If you closely look at the third example, I'm trying to decrement my i variable.
[09:28] So i-- is an expression.
[09:31] So these kind of expressions are also allowed inside for loop.
[09:35] If needed I can simply write some System.out.println() and hello world as well inside my initialization
[09:41] section.
[09:42] And if you look at the last example here we have two expressions which is i-- comma
[09:49] System.out.println( " Hello World" )
[09:50] .
[09:51] So there are two expressions which are separated by comma.
[09:54] This is completely acceptable inside the initialization section.
[09:58] Let me share
[09:59] more examples around the initialization section this time you can see first here I'm trying to simply
[10:05] declare an variable which is int i =9.
[10:09] So this is going to work perfectly.
[10:11] Whereas in the next example you can see outside of my for loop I already declared this i variable with
[10:17] the value nine.
[10:18] So if I try to declare the same I variable one more time, I'm going to get a compilation error because
[10:24] the i variable is already declared.
[10:27] So that's why
[10:28] please always make sure you are not re declaring the variables again, which are already declared outside
[10:35] the for loop, whereas re initialization is perfectly allowed
[10:39] for example, here in the very first statement, I'm trying to declare the i variable.
[10:44] In the next statement, I'm trying to re initialize it with the new value six.
[10:49] If needed, you can try to re initialize the value inside your for loop by simply mentioning i is equal
[10:55] to ten.
[10:56] So with this it should be pretty clear for you're declaration of the variables is not allowed, whereas
[11:02] reinitialization of the variable values is allowed inside the initialization section.
[11:08] Now let's try to understand about the condition expression.
[11:12] The condition expression has only a single rule that you need to follow.
[11:16] Your condition expression should always give a boolean value as an output.
[11:21] It can be true or false. Other than the boolean value,
[11:25] if your expression is resulting an int value or any other data type, it is always going to result into
[11:32] an compilation error.
[11:33] After the condition expression, we have update expression.
[11:37] The other name for the update expression is expression list.
[11:40] Inside the update expression, we are allowed to only define the expressions, but we are not allowed
[11:47] to define the variables.
[11:48] For example, here you can see under the update expression I'm trying to declare a variable which is
[11:55] int j = 10.
[11:57] So this is not allowed because inside update expression our expression list section only the Java expressions
[12:06] are allowed.
[12:06] But since this is a Java declaration statement, you're going to get a compilation error.
[12:12] Whereas if you see in the next example i++ is a Java expression.
[12:17] And very similarly i++ System.out.println()
[12:21] there are two different expressions which are separated by comma.
[12:24] So these kind of expressions are acceptable inside your last section of your for loop.
[12:31] But please note that you cannot declare the variables inside the update section.
[12:37] I hope you are clear with the rules of the three sections.
[12:40] So all these three sections are not mandatory.
[12:43] You can simply ignore them while defining the for loop.
[12:47] Let me show you how that is going to look like.
[12:49] Here you can see I have provided two flavors of for loop.
[12:53] Both of them
[12:53] they are going to execute infinite number of times, because we have not defined any of the components
[13:00] like initialization, condition and update expression.
[13:04] So whenever you want to ignore, you can simply mention a space followed by semicolon.
[13:10] With this you can see all these three sections are not present inside this for loop.
[13:15] And this confirms that these are optional.
[13:17] So whenever you're not mentioning them, then in such cases your for loop is going to be executed infinite
[13:24] number of times.
[13:25] But you need to take care of defining the statements for your for loop.
[13:30] Defining a statement inside the body of the for loop is mandatory.
[13:35] In case if you don't have any statements to define, at least you need to make sure you are mentioning
[13:41] an empty body with the help of the curly braces
[13:44] like you can see here.
[13:45] It is an empty for loop.
[13:47] If you don't want to mention these curly braces, you can simply terminate your for loop by mentioning
[13:53] a semicolon, because semicolon is also a valid empty statement or a null statement
[14:00] inside Java. I'm going to show you examples of all of them in the Demo.
[14:04] Let's try to build some examples using for loop in the next lecture, and in the same process, we can
[14:10] see the demo of all the topics that we have discussed under the for loop.
[14:14] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
