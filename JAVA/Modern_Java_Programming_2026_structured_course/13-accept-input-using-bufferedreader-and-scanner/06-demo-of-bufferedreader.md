# 13.6 — Demo of BufferedReader

> Section 13: Accept input using BufferedReader and Scanner

[00:00] Inside this lecture, let's try to build a simple program with the help of BufferReader object.
[00:06] And in the same process, we can try to accept the input data from the end user.
[00:10] For the same
[00:11] I'm going to create a new class inside the package java.eazybytes.input.
[00:17] The class name I'm going to give here is BufferReaderDemo.
[00:21] Once this class is created as usual, first we need to create the main() method by using the public static
[00:28] void main.
[00:29] Inside this main() method, I'm going to create the object of BufferReader class.
[00:34] For the same, let me give the object reference name as bf is equal to new BufferReader.
[00:42] But if I try to invoke that default constructor, I'm going to get a compilation error because there
[00:47] is no default constructor inside the BufferReader.
[00:51] At least I should provide an object of reader.
[00:55] For example, if I click on this BufferReader, you can see I have two options.
[00:59] One is either I can pass the Reader object as an input, and the other option is I can pass the Reader
[01:06] object and the buffer size.
[01:08] For now, let's not worry about the buffer size, because the default 8kb size is more than enough
[01:13] for the most of the scenarios.
[01:15] With that, I should at least pass the object of Reader as an input parameter to the constructor of
[01:22] BufferReader.
[01:22] But can I create the object of Reader?
[01:25] We can't create it because this is an abstract class.
[01:28] Instead of trying to create the object of this abstract class, we can try to create the object of the
[01:34] subclasses of this Reader superclass.
[01:36] You can see in the comments they have provided list of all the Readers which are extending these class.
[01:43] For example, if I can open these InputStreamReader, it is extending the Reader abstract class so
[01:49] I can try to create the object of InputStreamReader.
[01:52] But you may have a question here.
[01:54] I have so many options here.
[01:56] Why should I use only the InputStreamReader?
[01:59] It's very simple.
[02:00] Whenever you are trying to accept from an input device like keyboard.
[02:05] In such scenarios you should use InputStreamReader.
[02:08] Whereas if you are trying to read the data from a file, then you should use a FileReader.
[02:14] So these are the mostly commonly used readers, but if you are looking for other options, my recommendation
[02:20] is to read the documentation of all the remaining readers.
[02:24] But like I said, for the most of the scenarios, these two readers should be more than enough since
[02:29] we are trying to accept that data from an end user using keyboard, I need to pass the object of
[02:36] InputStreamReader to the BufferReader constructor, so I can first try to create the object of InputStreamReader
[02:42] with the variable name as isr, followed by new off InputStreamReader.
[02:49] But unfortunately InputStreamReader does not have default constructor.
[02:55] While we are trying to create the object of InputStreamReader, we should tell what is the input stream
[03:00] where this reader has to read the data.
[03:02] Since we are trying to read the data using keyboard, we can use System. in to pass as an input parameter.
[03:12] So whenever we invoke the System,in, it is going to create the object of InputStream.
[03:18] So the same object we are trying to feed to the InputStreamReader object.
[03:21] Once this InputStreamReader object is created, we are trying to feed the same to the BufferReader.
[03:27] So now my BufferReader is completely initialized.
[03:31] As a next step, I should be easily read that data with the help of these BufferReader object.
[03:36] So first let me try to use a System.out.println().
[03:40] And here I'm going to mention the same statements like you can see here I can copy this code and I can
[03:47] paste it here saying that please enter a value.
[03:51] After this I'm going to use the bf object.
[03:54] And using this you can see we have various options like read read line.
[03:59] So there are many methods available for now let me invoke the read method.
[04:04] So we are getting a compilation error related to exception handling.
[04:08] For now we can click on this add exception to the method signature.
[04:11] And with that this throw statement is going to be added to the method.
[04:15] So this read is also going to give the output in the int format.
[04:20] That's why I'm trying to assign the output from this read method to this num variable.
[04:24] And the same I'm going to print using the System.out.println().
[04:28] So let me execute this program.
[04:30] So it is asking me to enter a value.
[04:32] I'm going to enter a value which is 5647.
[04:35] And you can see here also we have the same problem which is it is printing only the ascii value of the
[04:42] first character.
[04:43] But don't worry and demotivated.
[04:45] Let's solve this problem using the same BufferReader.
[04:48] This read method is exact copy of same code that we have seen before, like inside this JavaBasicInputDemo
[04:54] .
[04:55] This time, instead of read, I'm going to invoke the readLine() method.
[04:59] So the readLine() method is going to give the input in an String format.
[05:05] So I can change the variable name to String input, and the same I can pass to this System.out.println().
[05:13] .
[05:13] This time let's see the magic if it is going to work or not.
[05:17] So I'm trying to enter a value which is 5375.
[05:20] Hooray!
[05:21] This time we are getting the exact output which is 5375.
[05:25] Let me try to execute this program one more time, and this time I'll try to enter my name, which is
[05:31] Madan, and if I try to press enter, I'm getting a value which is user entered a value Madan.
[05:38] So every time after entering the value, you need to press the enter so that the next piece of code
[05:44] is going to be executed inside your Java program.
[05:47] So this confirms readLine() is a better method compared to the basic read() method.
[05:52] I'm going to run this program one more time.
[05:54] This time I'm going to enter my complete name like Madan Reddy and press enter
[06:03] and this time you can also see it is capable of accepting reading multiple words as well.
[06:10] This way we can try to enter any amount of data.
[06:13] Like I can say my name is Madan and I am trying to teach Java, so now I'm pressing enter.
[06:25] The same is getting printed onto the console.
[06:29] With this, it should be pretty clear for you that readLine() is a better option.
[06:33] But the problem with read line is it is always going to give the output in a String format.
[06:38] Even if you enter a number, it is still going to give in a String format.
[06:42] It is the developer responsibility to convert that String into a int or double based upon the content
[06:48] of the String data.
[06:49] So to overcome this challenge, we have a better option, which is Scanner class.
[06:53] We're going to discuss about Scanner class in in the coming lectures.
[06:56] For now let's focus on these BufferReader alone.
[06:59] So with this piece of code we are able to successfully accept any kind of data from an end user.
[07:06] And the same is being processed inside my business logic.
[07:09] For now, I'm just trying to print the input data entered by the end user.
[07:13] In the next lecture, I'm going to show you a sample program and how to accept a number.
[07:18] And based upon the number, we can decide if a number is a prime number or not.
[07:23] But before I try to close this lecture, I want to highlight you one important point.
[07:27] Whenever you are trying to deal with the BufferReader or Scanner or any other kind of class object
[07:33] which are dealing with the input and output data, we need to make sure we are closing them before the
[07:40] end of the program.
[07:41] Let me tell you what do I mean by closing using the bf object, I can invoke the close() method.
[07:47] So what is this close() method is going to do?
[07:50] It is going to close the connection with your console or with your file which you are trying to read.
[07:56] It can be any InputStream.
[07:58] Just like in our real life, whenever we want to water, we will open the tab.
[08:03] Once we are done using the water or drinking the water, we are going to close the tab.
[08:08] If we don't close the tab, what is going to happen,
[08:10] all the water will be wasted.
[08:12] So the same is going to happen inside Java.
[08:15] also, whenever you are trying to deal with the object, that is going to help you to read the data.
[08:20] So in all these kind of scenarios, you need to make sure you are closing the connection.
[08:25] If you don't close the connection with the file or with your console.
[08:29] So it is going to create some memory leak, or it may create some performance issues inside your real
[08:35] production applications.
[08:36] Maybe for these kind of smaller programs, you may not see any impact.
[08:40] The program may work even without these closed statement, but it is a very good practice to always
[08:46] close the stream or the resource or the object that you have opened to read the data, or to fetch the
[08:54] data.
[08:55] That's why I'm making sure to invoke this close() method using the BufferReader object at the end of
[09:00] the program.
[09:01] When we discuss about the exception handling, there is a better standard way that we need to follow
[09:05] to invoke this close() method.
[09:07] I'm going to discuss that in the coming sections.
[09:09] For now
[09:10] please note that whenever you are dealing with the resource related object like like Stream objects,
[09:16] please make sure you are closing those with the help of close() method.
[09:19] I hope you're clear.
[09:20] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
