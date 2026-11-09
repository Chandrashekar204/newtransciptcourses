# 2.7 — How to name a java variable

> Section 2: Primitive data types in Java

[00:00] As of now
[00:01] we discussed on how to create variables with the help of primitive data types and how to assign data
[00:08] or values to these variables.
[00:10] So if you see here I'm trying to use a variable name as b.
[00:14] And very similarly here I'm using a name as num.
[00:17] So you might be under the assumption we can do any name except the Java keyword with any format.
[00:24] But I want to let you know that there are certain standards that we need to follow while declaring variable
[00:30] names.
[00:31] So let's try to understand what are those standards.
[00:33] Because without knowing these standards, you may end up defining some variable names which are against
[00:39] to the standards.
[00:40] And with that, whenever someone sees your code, it clearly conveys that you're not an experienced
[00:45] developer or you don't know enough about Java.
[00:48] So to avoid such scenarios, I want to share more details about the naming conventions that we need
[00:54] to follow while defining variable names.
[00:56] Whenever we want to define a name to a variable, we are encouraged to follow the camel case approach.
[01:03] So let's try to understand what is a camel case approach.
[01:07] We all know that a variable or identifier, is simply a name that we are trying to give to a memory
[01:12] location, where we want to store a value that is supported by a given primitive data type.
[01:18] We can also give an identifier to a Java class or to a Java method and the method input parameters.
[01:24] So there are many places in Java where we can define these identifiers or variables.
[01:29] But right now, since we are focusing on primitive data types inside this section, let's try to focus
[01:34] on the Java naming conventions that we need to follow,
[01:38] while we are trying to declare variables with the help of primitive data types.
[01:43] If your variable has a single word like num or number, you can always follow the lower case alphabets.
[01:49] But sometimes your variable name may contain compound words.
[01:54] Think like you want to give a name as first name.
[01:56] In such scenario, the very first point that you need to aware is space is not allowed inside the variable
[02:02] names.
[02:03] So that's why you need to give first and name without any space.
[02:07] And at the same time, whenever you are trying to use multiple compound words inside your variable name,
[02:12] you need to always make sure the very first letter inside your variable name is starting as lower case.
[02:18] Post that every subsequent word that you are trying to append to your variable name has to start with
[02:25] a capital letter.
[02:26] So first is a word, and name is a word.
[02:29] So if I try to combine them as a variable name, the first name should be like you can see in the screen.
[02:34] So this is the firstName.
[02:35] And very similarly if I want to give a variable name as totalAmnt for the amount, I'm trying to
[02:41] use a shortcut as Amnt.
[02:43] So here total is a word and Amnt is a another word.
[02:47] So total has to be completely in small letters, whereas the second word first letter has to be in the
[02:53] capital letter.
[02:54] The same applies for isValid, numOfWords.
[02:57] So in the numOfWords you can see there are three words
[03:00] num indicates number, Of and words.
[03:03] So if I combine all these three words as a single variable name, obviously all the letters inside the
[03:09] first word has to be completely lowercase, and the second word first letter, which is O, is going
[03:15] to be capital.
[03:16] And the third word first letter, which is W, is going to be capital again.
[03:20] So this kind of naming convention we call it as camel case.
[03:24] We as Java developer, we are encouraged to follow this standard.
[03:27] Even if you don't follow these camel case standard, the Java compiler is not going to throw any error.
[03:34] Your code still is going to work, but you will be treated as a Java developer who are not going to
[03:39] follow any standards.
[03:40] So that's a bad reputation, which you should avoid.
[03:43] So always follow the camel case for the variables that you are trying to create with the help of primitive
[03:49] data type.
[03:50] Apart from camel case convention, there are also certain other rules that we need to follow.
[03:55] We all know that variable names are case sensitive, and these variable names can be formed only with
[04:00] the help of alphabets, numbers, and apart from alphabets and numbers, your variables can also contain
[04:08] only two special characters, which are dollar ($) value and underscore(_).
[04:13] So your variable name always can get started with a letter or a dollar sign, or the underscore character.
[04:20] But never ever
[04:21] your variable name should start with a number, so you can start your variable name with the help of
[04:27] dollar and underscore.
[04:28] In general, it is not recommended to start your variables with a dollar and underscore, so the standard
[04:35] is,
[04:35] always start your variable names with the letter and post that you can have numbers or special characters
[04:42] like dollar and underscore.
[04:44] And apart from these standards, we should also take care of choosing a name for a variable in full
[04:50] words rather than cryptic abbreviations.
[04:53] For example, think like you want to create variables like amount, speed, and gear in such scenarios
[04:59] it is always recommended to mention the complete word like amount, speed, and gear instead of doing
[05:06] this,
[05:06] if you try to create the variables with the cryptic abbreviations like a, s, g, then in such scenarios
[05:13] the other developers who are trying to read your code, they're not going to understand your code very
[05:19] easily because you didn't define the variable names that are meaningful.
[05:23] So that's why always go with the meaningful words rather than cryptic variable names.
[05:31] By following these standard, you are always going to improve the readability of your code.
[05:36] And at last, the final standard that you need to be aware is we should not choose a variable name,
[05:42] which is of a Java keyword and a reserved word.
[05:44] So what is a reserved word?
[05:46] false, true,
[05:47] null.
[05:48] So these are all the reserved words in Java.
[05:51] That's why we are not allowed to create a variable with a reserved word like true, false, null.
[05:57] And the other Java keywords that we have inside the Java programming language.
[06:01] I know you may have some questions here.
[06:03] That's why
[06:03] let me give you some examples
[06:05] and in the same process we can try to understand more about these standards.
[06:09] So here I have a table where first I am going to show you what is the variable name, our identifier
[06:14] name.
[06:15] You should tell me whether it is going to be a valid if it is valid,
[06:19] what is the reason, if it is not valid, what is the reason?
[06:22] So the first identifier name that we have here is, firstName1.
[06:26] So here first is a word,
[06:27] name is a word and 1 is a another word.
[06:30] So we're trying to form a single variable name.
[06:33] That's why we don't have any space here.
[06:35] first, name and one inside the name which is the second word we have N capital letter.
[06:41] So this is following the camel case approach.
[06:43] So do you think this is valid one or not.
[06:45] Off course this is a valid one because it contains alphanumeric values.
[06:49] So the answer is going to be yes and it contains letters and number.
[06:53] Now let me show you the next identifier.
[06:55] The next identifier is $personName.
[06:58] So can you tell me whether this is valid or not.
[07:00] We discussed every variable can start with a letter or dollar or underscore.
[07:06] So with that reason this is going to be valid.
[07:10] But like I said before, please try to avoid using the dollar and the underscore as the very first letter
[07:16] inside your variable name, because this is not a standard or a recommended approach.
[07:21] Now let's try to move on to the next identifier which is
[07:25] 7firstName.
[07:26] Do you think this is going to be valid?
[07:28] Off course this is not because the variable name is starting with a number.
[07:33] Can we try this once in the jshell.
[07:35] So let's go to the jshell and try once.
[07:37] So here I'm trying to create an int variable with the name as
[07:43] 7firstName
[07:44] and what is the value.
[07:46] I'll give you some random numeric value which is six.
[07:49] So if I try to execute this you can see I'm getting an error because I'm not allowed to use the numeric
[07:55] value as a very starting letter of my variable.
[07:58] I hope you're clear.
[07:59] Now moving on to the next identifier,
[08:01] here I have age _of_person, but each word is separated by underscore.
[08:06] Do you think this is valid?
[08:08] Off course this is valid because there is no wrong inside this variable name.
[08:12] We are using letters and underscores like we discussed
[08:15] only two special characters are allowed inside the variable name, which are dollar and underscore.
[08:21] Moving on to the next identifier here I have person name.
[08:24] So this is going to be easy for you.
[08:26] Do you think this is valid?
[08:28] Yes, you are right.
[08:29] This is not a valid identifier name because we have a space here inside the variable name spaces are
[08:35] not allowed inside the variable names.
[08:37] With that reason this is going to be invalid.
[08:40] The next identifier that I have here is personName* .
[08:43] This one also is going to be easy for you.
[08:45] This identifier is also invalid because we have a special character which is asterisk which is not allowed.
[08:54] Please note that only dollar and underscore are only allowed inside the variable name.
[09:00] The next identifier is going to be tricky.
[09:03] I'm not expecting you to answer this because this is a completely new information for you.
[09:07] So here I have a identifier name as $.
[09:10] Inside Java we can have a identifier name as $.
[09:14] So there is no wrong.
[09:16] This is going to work perfectly without any issues.
[09:19] Very similarly, can we create a variable name with _?
[09:23] You may answer yes here, but the answer is no because from JDK 9, using of an underscore as a standalone
[09:31] identifier is no longer permitted.
[09:34] Before JDK 9, it used to work, but right now it is no longer permitted.
[09:39] The next variable name that I have here is firSTName,
[09:41] But here you can see I have mentioned the capital letters and small letters wherever I want.
[09:47] Off course, this is not a valid identifier if I go with the camel case standards, but like I said before,
[09:55] following camel case is completely optional.
[09:58] That's why,
[09:59] your compiler still is going to accept this name as valid identifier name.
[10:05] But if you follow these variable name or identifier name inside your code, you're going to be recognized
[10:10] as a new Java developer who don't know about the camel case approach.
[10:15] The last identifier name that I have here is 654.
[10:18] So do you think this is going to work?
[10:20] Yes, you are correct,
[10:21] this is not going to work because the variable name has completely all numbers which is not allowed
[10:28] inside Java.
[10:28] So always note that you need to pass two steps whenever you are trying to define a name for the identifier.
[10:35] The very first step is you need to make sure you are satisfying your Java compiler by following all
[10:40] the standards, so that the Java compiler is not going to throw any error.
[10:45] Once you satisfied your Java compiler as a next step, it is always recommended to follow the camel
[10:52] case approach as a standard.
[10:55] Even without following the camel case approach, your compiler is not going to throw any error.
[11:00] But like I said, it just a standard that everyone supposed to follow, because defining the variable
[11:06] names with the camel case is going to improve the readability.
[11:10] If I randomly put capital letters and small letters wherever I want, do you think it is going to be
[11:15] easy for someone to read?
[11:17] Off course it is not
[11:17] that's why please always follow the camel case approach.
[11:21] At last I want to highlight that three words which are true, false, and null.
[11:26] These are also not allowed as a variable names.
[11:30] Off course, you may think these are like Java keywords, but they are not Java keywords.
[11:34] Those are literal values only which are preserved with a meaning.
[11:38] So what is the meaning of true inside Java?
[11:40] True means something correct, false means something wrong, and null indicates there is no value and
[11:46] it is an empty.
[11:47] I hope you're clear.
[11:48] So let's try to try some of these identifier names inside the jshell and see what kind of errors we
[11:54] are getting.
[11:55] So here I'm going to define a variable with a simple $ and I'm going to assign a number seven.
[12:02] So you can see this is completely fine.
[12:05] There is no issue.
[12:06] Now similarly I'm going to assign _.
[12:08] And here I'm getting an error because underscore is not allowed from java 9.
[12:14] Now as a next step I can create a variable name which is against the camel case sensitivity.
[12:20] So here you can see I'm trying to give some random letters numbers and special characters.
[12:26] So with this it should work without any issues because I'm following all the rules of Java compiler.
[12:32] But this is not a standard to follow inside your actual code.
[12:36] So your compiler is not complaining. This time
[12:39] let me try to create a variable with a number like 666.
[12:43] And to this I'm going to assign a number seven.
[12:46] So you can see I'm getting an compilation error.
[12:49] I can also try to create a variable with the reserved literal which is false.
[12:53] And to this false I'm going to assign a number.
[12:56] You can see I'm getting an compilation error.
[12:58] Very similarly, I can also try by mentioning null as an variable name.
[13:04] For these I'm going to assign a number seven.
[13:07] So this is also not acceptable inside the variable names.
[13:11] So now I'm assuming you are clear about the standards that we need to follow while defining the identifiers.
[13:18] Apart from these standards, we should also make sure our variable names are always meaningful.
[13:23] We should not use short forms to give a name to a variable.
[13:26] Suppose think like
[13:27] I'm trying to give a variable name as a and to this a
[13:32] I'm trying to assign some number.
[13:35] So here my a has a value as 9.
[13:38] But if someone sees at this code, do you think they are going to get anything from this.
[13:42] They don't know,
[13:43] what is this a represent.
[13:44] They don't know what is this nine represent?
[13:46] If I try to change the same variable name to int age is equal to nine this time, this is going to make
[13:54] sense to anyone, because it is clearly conveying that this age variable is going to represent,
[14:01] so someone has an age of nine years.
[14:03] Let me show you another example.
[14:05] This time I'll just mention int salary is equal to 1000.
[14:10] So this is clearly conveying that I'm trying to store the salary of a person inside the salary variable.
[14:17] But if I store this variable as int s is equal to 1000.
[14:21] So compiler is not going to complain anything, but it is not going to make any sense to anyone.
[14:27] That's why, like we discussed, always, always go with the meaningful words for your variables.
[14:34] If needed
[14:34] you can have compound words also as your variable names.
[14:38] I know this might be too much heavy for you right now, but don't worry,
[14:42] throughout this course, whenever I'm trying to create variables, I'll always make sure I'm following
[14:47] the standards that we discussed, in the same process
[14:49] you can also try to observe what are the standards that I'm following and follow the same
[14:55] while you are practicing the Java code inside your local system, please note that
[14:59] " Rome is not built in a single day ".
[15:02] Very similarly, you're not going to become a perfect Java developer in a single day or in a single
[15:07] month.
[15:08] It is going to require a lot of practice,
[15:10] you need to make a lot many mistakes,
[15:11] you need to learn from your mistakes.
[15:13] So it's a very beautiful, painful journey that you need to go through to become a perfect Java developer.
[15:20] I hope this makes sense to you.
[15:22] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
