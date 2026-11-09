# 13.12 — Scanner example to read the file content

> Section 13: Accept input using BufferedReader and Scanner

[00:00] As of now, we are clear on how to accept the input data from an end user with the help of Scanner class.
[00:07] As a next step, let's try to understand how to read the data present inside a file with the help of
[00:14] Scanner class.
[00:15] It is going to be a super simple task.
[00:17] First, we need to go to the FileReaderWithBFR class.
[00:21] So let's try to copy the same class into the same package.
[00:26] But this time the class name is going to be FileReaderWithScanner and post that
[00:31] inside this class we need to make some changes.
[00:34] The very first one is we need to remove the code related to the BufferReader.
[00:40] Instead, I'm going to mention the Scanner sc is equal to new Scanner() and to the Scanner
[00:48] we need to mention the details of file.
[00:51] So how to mention that details of file with the help of File class.
[00:55] So there is a File class inside the java.io package.
[00:58] So first we need to create the object of the File using the constructor of File class.
[01:04] And to this constructor of the File class, we need to mention the path of the file.
[01:09] So what is the path of the file.
[01:11] So this is the path
[01:12] let me try to copy the same and paste it inside the constructor of the File class.
[01:17] And with that now I have an object of File which I can pass to the constructor of the Scanner class.
[01:23] After making these changes, I will try to invoke the sc.close() at the end to resolve this compilation
[01:29] error.
[01:30] The last step that is pending right now here is we need to update the expression inside the while statement.
[01:36] So as of now, you can see we're trying to read the content with the help of readLine() method of
[01:43] BufferReader.
[01:43] And if the content is not null, then only we are trying to execute the looping logic of the while statement.
[01:50] Instead of this, we can simply mention sc.hasNextLine() and this hasNextLine() method.
[02:00] It is going to give me a boolean value if there is some data available in the next line, this expression
[02:06] is going to give the output as true.
[02:09] And in that scenario, the while looping logic is going to be executed when the looping logic reaches
[02:14] to the end of the file.
[02:16] In such scenarios, the hasNextLine() method is going to give the output as false, and with that we'll
[02:22] be terminating the execution of the while statement.
[02:25] I hope you are clear.
[02:26] So as of now you can see we are only checking if the data is present inside the next line or not, but
[02:31] we are not actually trying to read the data.
[02:33] That's what I'm going to do inside the while loop.
[02:36] So inside the while loop, just after this println() method, I'm going to invoke the nextLine() method.
[02:43] So the output from these nextLine() method I'll be providing to the println() statement.
[02:48] And with that we don't need this String line variable because we are directly trying to send the input
[02:54] data that we are trying to read to the println() method.
[02:57] So if I try to execute this program this time also, you should be able to see the same output.
[03:03] And with this it should also pretty clear for you right now, which is the logic that we are going to
[03:09] write with the help of Scanner is always simple compared to the BufferReader.
[03:14] The next question that you may have here is and are which scenarios I should use the BufferReader and
[03:20] Scanner.
[03:20] You may tempted to use the Scanner approach all the time, but there are certain scenarios where you
[03:27] should prefer BufferReader.
[03:29] So let's try to understand the differences between these two approaches in the next lecture.
[03:34] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
