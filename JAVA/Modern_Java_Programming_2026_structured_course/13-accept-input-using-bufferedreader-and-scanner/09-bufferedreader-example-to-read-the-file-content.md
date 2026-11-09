# 13.9 — BufferedReader example to read the file content

> Section 13: Accept input using BufferedReader and Scanner

[00:00] Inside this lecture, let's focus on other common operations that we can perform with the help of
[00:07] BufferReader.
[00:08] As of now, we are accepting the input data from end user based upon our business requirements.
[00:14] The next common operation that you may see inside your real projects is to read the data from a file.
[00:21] Maybe there is a file inside your system or inside a server.
[00:24] You want to read the content of the file in this kind of scenarios
[00:28] also we can use BufferReader object.
[00:31] So let's try to understand how to achieve the same here.
[00:34] Inside the section 13 project I'm going to create a new Java class with the name
[00:43] FileReaderWithBFR.
[00:44] So BFR means buffered reader inside this class.
[00:48] First I need to create the main method and post that we want to create the object of BufferReader.
[00:55] So how to create the BufferReader object?
[00:57] We can simply use the BufferReader class.
[01:00] And here I'm trying to give a object name as reader.
[01:03] And to this we are going to assign the code which is new BufferReader logic.
[01:09] But like we discussed previously, we can't invoke that default constructor of BufferReader.
[01:14] At a minimum, we should pass an object of class which extends the Reader abstract class.
[01:21] Previously, when I was talking about Reader class, I told you that using InputStreamReader, we
[01:25] can read the data from an input device like keyboard, but coming to the file, we should not use the
[01:32] InputStreamReader, we should use a FileReader.
[01:35] That's why I'm going to create the object of FileReader first with the class, which is FileReader
[01:41] itself, and this is also present inside the package java.io.
[01:45] So the object name I'm going to give as FileReader.
[01:48] And to this I'm going to assign the code which is new FileReader.
[01:52] But you can see here also we are getting a compilation error because whenever we are trying to create
[01:57] an object of FileReader, we can't use the default constructor.
[02:01] At a minimum, we should tell the path of the file where it is present.
[02:05] Otherwise, how my file reader know where is my file is present, and what is a file that I'm trying
[02:11] to read.
[02:11] So that's why, as an input to this constructor of FileReader(), I'm going to provide the path details
[02:17] of my file by using the String value.
[02:20] So to demo you about the file reading operation, I have created a sample text file inside my desktop.
[02:27] So this is the sample text file storage dot txt the file name inside this file I have some random story
[02:34] present inside this file.
[02:35] So now using the BufferReader, we want to read this content inside this file and display the same
[02:41] unto the console.
[02:42] So now I have a file ready
[02:43] as a next step, I need to make sure I'm providing the path details of this file to the constructor
[02:49] of FileReader().
[02:50] Let me take the file details by copying the file path.
[02:54] Now I'm trying to paste the file path here so the file is present inside the user/easybytes/Desktop
[03:00] and the file name is story.txt.
[03:03] If you are trying to build along with me, I would request you to create some text file inside any folder
[03:10] location and provide the path of the file like I'm trying to do here.
[03:14] As soon as we provided the path of the file, we are getting a compilation error saying that we are
[03:18] not handling the exception which is file not found exception.
[03:22] So to fix this issue for now, I can simply add exception to the method signature.
[03:27] And you can see we are trying to use the throws keyword followed by FileNotFoundException.
[03:32] Now I have my FileReader object ready.
[03:35] I can take this object and provide as an input to the constructor of BufferReader and post that I'm
[03:41] going to create a String variable, which is line, and to this line I'm going to assign the content
[03:47] that we are going to read with the help of BufferReader and invoking the redLine() method.
[03:52] Here you can see we are getting an compilation error saying that we are not handling the IOException.
[03:57] So what I can do is I can try to add IOException to the throws block by using a comma operator.
[04:05] And with that, I'm getting a warning here saying that there is a general exception which is IOException
[04:10] in the throws list already.
[04:12] And with that, we don't have to again mention that redundant exception which is FileNotFoundException.
[04:18] So the IOException is capable of handling FileNotFoundException as well, because it is a more general
[04:25] exception compared to the FileNotFoundException.
[04:27] So these things which are related to the exception handling may not be super clear for you right now.
[04:33] But don't worry, I'm there for you.
[04:35] I'm giving my assurance that I'm going to teach you everything about the exception handling in the coming
[04:40] sections.
[04:41] For now, let's remove the FileNotFoundException and we should be good.
[04:45] As a next step, I want to print out the content of line String object.
[04:50] If I try to execute this program, you can see I'm getting only the first line because with the help
[04:55] of readLine() method, I will be able to read only one line.
[05:00] line at a time.
[05:00] So what do we have as a first line inside our file we have the the Enchanted Forest.
[05:05] The same is being displayed on the console.
[05:07] So the challenge right now that we have is how to read all the content inside the file.
[05:11] So think like there are more than 20 lines of content inside your file.
[05:16] So you want to read line by line.
[05:18] In this kind of scenarios of course we can use looping logic.
[05:23] We are expects around the looping logic.
[05:25] Let's try to use a while loop to read the content of the file by using the object of BufferReader and
[05:31] readLine() method.
[05:32] So what I'm going to do is, I'm going to simply write a while block.
[05:36] And inside this while block I'm going to mention this statement which is System.out.println().
[05:41] And to this println() I'm trying to pass the object of String, which is line.
[05:45] You may have $1 million question here.
[05:48] What is the condition that I need to define here inside my while statement.
[05:53] So let's imagine for a second what we are trying to achieve.
[05:56] We are trying to achieve the content of a file.
[05:58] And how can I convey the same to my while block?
[06:01] We should tell to the while block saying that please keep invoking the redLine() method continuously
[06:07] until you see the end of the file.
[06:09] So how my BufferReader will know that it has reached the end of the file whenever the readLine() method
[06:14] gives the null as an output, that indicates that my BufferReader reached the end of the file.
[06:21] Using the same logic, let's try to define the while expression.
[06:25] So here I'm going to mention the same logic which is line is equal to reader.readLine().
[06:33] I'm trying to read the current line by using these logic, and this code is going to be invoked continuously
[06:40] during each iteration of the while loop.
[06:44] So first it is going to read the first line.
[06:46] Next it will move to the second line third line.
[06:48] So the looping logic is going to keep on executing until a given condition become false.
[06:53] So right now I'm getting a compilation error because this is not a boolean expression.
[06:58] So here I want to build a boolean condition by using the line String object.
[07:04] Whenever these line String object is not a null, then only I want my while block to continue the execution.
[07:10] Otherwise I want my while block to stop the execution.
[07:13] So let's try to see how to achieve the same.
[07:15] First, I'm going to put the parentheses around my code.
[07:20] As of now you can see inside these parentheses we have this logic which is going to give the current
[07:25] line String content into this line object the same
[07:29] I want to check if it is not equal to null.
[07:33] So whenever this Line object is not equal to null, I want the execution of the while block to continue.
[07:38] So what do I have inside my while block?
[07:40] I'm just printing the current line.
[07:42] So with this we should be good.
[07:44] But before I try to execute this program, we need to make sure we are closing the connection that
[07:50] BufferReader opened with the file.
[07:53] So how to do that?
[07:54] We need to invoke the close() method on top of the Reader object, which belongs to BufferReader class.
[08:00] So we missed
[08:01] mentioning these close() method in all the three examples that we have discussed previously.
[08:06] Let me mention very quickly inside these examples as well.
[08:10] Inside the PrimeNumberChecker I need to mention at the end bf.close(), I'm going to copy the
[08:17] same content and mention inside other two examples as well.
[08:22] Now let me go to the other example which is BufferReaderEvenOddDemo here also I'm trying to mention.
[08:29] So we rectified the bug that we have inside our examples.
[08:32] Now let me go to the FileReaderWithBFR.
[08:35] As a next step I'm going to execute this program.
[08:38] Let's see what is going to happen this time.
[08:40] You can see I have my complete file printed onto my console.
[08:45] Hooray!
[08:46] We achieved this!
[08:48] A huge congratulations to both of us, because this is a very complex process and we are able to achieve
[08:53] this very easily with the help of BufferReader.
[08:57] Think what is going to happen if you don't have BufferReader, you have to read a character by character
[09:02] from a file.
[09:03] It is going to create super super performance issues, but with the help of BufferReader, whenever
[09:09] it is trying to interact with the file, it is going to read the data in chunks at a time.
[09:15] It is going to load data which is equal to the size of 8kb.
[09:20] Once that 8kb of data is loaded into the memory, it is going to perform the red line operation.
[09:27] Once all the data inside the memory is read, it will go to the file and load the next check of data.
[09:33] And this operation is going to keep on running until we receive the end of the file.
[09:38] And how can we know that we received the end of the file whenever the red line method is giving the
[09:43] output as null, that indicates we have reached the end of the file, and once this condition is met,
[09:49] the while block execution is going to complete and the program will continue with the next set of statements.
[09:55] I hope you are clear with this example.
[09:58] With this we are done discussing everything.
[09:59] Thing related to that BufferReader.
[10:01] All the concepts and topics that we have discussed around the BufferReader.
[10:05] I have mentioned them in these slides for your reference.
[10:09] I also mentioned all the examples that we have discussed as well, along with the code snippets.
[10:14] So please refer these slides in future whenever you want to quickly brush up your knowledge around the
[10:20] BufferReader.
[10:21] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
