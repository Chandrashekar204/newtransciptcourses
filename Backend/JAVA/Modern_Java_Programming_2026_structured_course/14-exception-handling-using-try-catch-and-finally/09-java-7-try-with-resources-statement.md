# 14.9 — [JAVA 7] try- with-resources statement

> Section 14: Exception handling using try, catch and finally

[00:00] Inside this lecture, let's try to discuss about a special try block which is try with resource statement.
[00:08] In the previous lecture we discussed about finally block and what is the purpose of finally Block.
[00:13] We need to use these finally block in the scenarios where we are dealing with the IO resources like
[00:20] Scanner, BufferReader, Files or database connections
[00:24] in all such scenarios, the developer has to make sure he's writing a finally block and he's making
[00:30] sure to close the resources.
[00:32] But what if developer forgets to close the resources
[00:35] or if he's not closing properly to handle these kind of scenarios?
[00:40] A special form of try statement introduced inside java7.
[00:45] This special try block is try with the resource statement.
[00:49] So the syntax to use this is whenever you are trying to create a try block inside the parentheses.
[00:55] After the try keyword, you can try to declare the object of your resources.
[01:00] For example, you can see inside the try block parentheses itself.
[01:04] I'm trying to declare the object of Scanner and the same Scanner object I can use inside my try block.
[01:11] The advantage that we get with these try with resource statement is the developer.
[01:15] He don't have to write the finally block behind the scenes, the java or the JVM
[01:21] it is going to take care of closing your Scanner object in all type of scenarios, regardless whether
[01:28] an exception happens or not.
[01:30] So that's the beauty of this try with resources statement.
[01:33] This is introduced in java7.
[01:35] Let's see the demo of this statement very quickly.
[01:38] I'm going to create a new Java class.
[01:41] The class name is going to be TryWithResourcesDemo inside this
[01:49] first let me try to create the main method post that I will try to copy the content of the main() method
[01:55] that is present inside the ExceptionDemo and paste the same inside the TryWithResourceDemo main()
[02:01] method.
[02:02] So you can see
[02:02] as of now we have the same code.
[02:04] This time, instead of defining the Scanner object inside the try block, I'm going to use that try
[02:11] with resources.
[02:12] So how to define the same just after the try keyword and before the curly brace, you can mention the
[02:18] parentheses followed by.
[02:19] You can try to move this code off object creation of Scanner into the try block parentheses.
[02:27] So let me mention Scanner before the object reference name and post that
[02:32] we can also remove these Scanner declaration that we have.
[02:36] With this we don't have to maintain the finally block.
[02:39] I can simply remove this because now the responsibility of closing the resource that is open due to
[02:46] the Scanner object is going to be with the Java or JVM at runtime.
[02:50] So as soon as my try block or catch block is executed at last, this Scanner connection is going to
[02:57] be closed behind the scenes by invoking the close() method.
[03:00] So this semicolon is optional.
[03:02] We can remove this.
[03:03] So this is going to be the correct and accurate syntax.
[03:06] Now let me try to execute this program this time
[03:09] also the behavior it is going to be same.
[03:11] Like if I try to enter three you're going to get a valid output.
[03:15] Whereas if I try to enter an invalid input I'm going to get an message from the catch block.
[03:21] But behind the scenes the Java taken care of closing the connection that is open due to these scanner
[03:28] declaration and initialization.
[03:30] I hope you are clear.
[03:31] So whenever you are trying to work with a IO resources like Scanner, BufferReader or anything related
[03:37] to the files database connections.
[03:39] In all such scenarios, you can simply use the try with resources and you can get rid of the finally
[03:45] block.
[03:45] Let's try to discuss more details about this
[03:47] try with resources.
[03:49] Whenever we are using this try with resource statement, we can specify multiple resources as well inside
[03:56] the statement.
[03:57] As of now, we saw the demo that I'm trying to create only the object of Scanner, but if needed you
[04:02] can create multiple objects inside that try with resource statement itself.
[04:06] Like I can create a Scanner object, BufferReader object database connection File object.
[04:11] It's up to us based upon our business requirements, we can create any number of objects with the help
[04:17] of this statement.
[04:18] The next important point is whenever we are using these try with resource statement.
[04:22] You should not be under the assumption that we can't use the finally clause.
[04:27] It is still allowed to have the finally block for any other requirements inside the application.
[04:33] With the help of try with resources, the Java is only going to take care of closing the connection,
[04:39] but if you want to perform any other cleanup activities in such scenarios, definitely there is no harm
[04:45] having the a finally block
[04:47] along with that try with resource statement and whatever resources that we are trying to create with
[04:52] the help of try with resources.
[04:54] All these resources are objects that are going to have reference variables or object variables.
[04:59] All these objective variables are reference variables, they are going to be implicitly final are effective
[05:06] final,
[05:06] that means we can't perform the reassignment within the try block by assigning some other object or
[05:13] by assigning some other value.
[05:15] So this is very similar to the multiple catch blocks scenario that we have discussed previously.
[05:20] What I mean here is we are trying to create an object of Scanner.
[05:24] So this Scanner it is going to be implicitly final.
[05:27] So if I try to reassign with the some other different value inside the try block, I'm going to definitely
[05:35] get an compilation error saying that cannot assign a value to a final variable Scanner.
[05:42] So this confirms that this Scanner variable that we are trying to create with the help of try with resources,
[05:48] it is implicitly final or
[05:50] effective final.
[05:51] We know that this try with resource statement is introduced in java7 before java 1.6
[05:58] the try block should be followed by either a catch block or a finally block.
[06:03] We can't define an try block alone, but with the java7 we can only have try with resource block
[06:12] without any catch block or finally block.
[06:14] This is because the try with resource statement behind the scenes, they are going to generate a finally
[06:20] block which is capable of closing your resources.
[06:24] So that's why
[06:24] please note that from java7 we can write try with the resource statement alone, and your try with
[06:32] resource statement don't have to be followed by a catch block or finally block.
[06:38] But if you are creating a normal try block, then in such scenarios it should definitely be followed
[06:44] by a catch block or finally block.
[06:47] I hope you are clear.
[06:48] In the next lecture, let's try to discuss formally what are the rules and guidelines that we need to
[06:53] follow whenever we are trying to define, try, catch and finally blocks inside a Java class.
[06:59] Thank you,
[07:00] bye.

----------------------------------------
