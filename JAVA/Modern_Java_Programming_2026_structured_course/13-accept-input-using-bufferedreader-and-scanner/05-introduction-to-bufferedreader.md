# 13.5 — Introduction to BufferedReader

> Section 13: Accept input using BufferedReader and Scanner

[00:00] Let's explore the very first option that we have inside Java to accept the input data efficiently,
[00:06] which is BufferedReader.
[00:08] This is a class available inside the Java library under the package java.io.
[00:14] We can also confirm the same by looking for this class BufferReader.
[00:18] So this is a class belongs to the package java.io.
[00:22] So let me open this class.
[00:23] This class extends another Reader class which is an abstract class.
[00:29] If you can open this Reader class, it is an abstract class.
[00:32] We should always use BufferReader because we can't create the object of abstract class which is Reader.
[00:38] So BufferReader is an implementation of Reader.
[00:42] So basically Reader is going to provide the capability to the BufferReader to read the input data from
[00:49] the given input stream.
[00:51] On top of that, BufferReader has additional logic, which is going to read the input data in a byte
[00:58] stream format.
[00:59] We can also read the documentation of this class.
[01:02] If you can scroll up here
[01:04] you can see the Java team highlighted.
[01:06] This class helped to read text from a character InputStream, buffering characters so as to provide
[01:13] for the efficient reading of characters, arrays, and lines.
[01:17] So why this approach is efficient compared to the basic approach that we have discussed in the previous
[01:22] lecture is, this approach is capable of reading a single character, a word, a sentence, a file,
[01:31] regardless of whatever amount you are trying to provide as an input.
[01:35] This BufferReader is capable of reading efficiently.
[01:39] I'm highlighting the word efficiently here, so let's try to understand what makes these BufferReader
[01:45] option as an efficient option.
[01:47] If you can scroll down inside this class, you will be able to see the constructors related to this
[01:53] class.
[01:53] So whenever we want to create an object of BufferReader to read the input data from an end user, these
[01:59] constructors, they are going to be invoked.
[02:02] So inside these BufferReader there is no default constructor.
[02:05] There are only two constructors which are going to accept input parameters.
[02:10] The first constructor that I want to talk here is, this constructor, which is going to accept the input
[02:15] parameter of type Reader.
[02:17] So Reader is an abstract class
[02:20] it is going to accept the object of all the subclasses which extends these abstract class.
[02:26] So you can see these are all the Reader classes which extends the abstract class Reader.
[02:31] So we'll be able to send the object of BufferReader, LineNumberReader, CharacterReader,
[02:37] InputStreamReader, FileReader, FilterReader.
[02:39] So there are many Readers available which we can leverage to create the object of these BufferReader.
[02:45] So when we try to create the object of this BufferReader with the help of a given reader, it is going
[02:51] to invoke the other constructor inside the same class with the two parameters.
[02:55] One is the InputReader object that we have provided.
[02:59] The other parameter is default care buffer size, so this is a constant present inside the same class
[03:05] you can see by default, whenever we are trying to create this BufferReader object, it is going to
[03:10] have a buffer size of eight kilobytes or 800192 bytes capacity.
[03:16] So the purpose of this buffer size is think like you're trying to provide a file to this BufferReader
[03:22] object to read the data.
[03:24] So inside your file you may have hundreds or thousands of lines.
[03:28] If you don't have this buffer size concept, this BufferReader object, it is going to end up reading
[03:35] character by character from your file.
[03:37] So every time you want to read a character, it will go to your file.
[03:41] It will read the character and it will load into the memory.
[03:44] So this is going to be a super inefficient process and it may create the performance issues.
[03:50] So to overcome these challenges, Java team decided to provide some buffer capacity to the BufferReader
[03:57] object.
[03:57] So with this capacity what is going to happen is your BufferReader object
[04:02] it is going to read based upon chunks.
[04:04] So whenever it is trying to go and read the content inside a file, it is going to load 8kb of
[04:11] data at once into the memory location and post that it is going to process character by character from
[04:19] the memory itself.
[04:20] So processing of the data from the memory is more faster compared to the reading of the data from the
[04:26] file which is present inside the disk.
[04:28] If needed
[04:29] we can also change these buffer size.
[04:31] Maybe if you are trying to read a very big file, you can try to improve these buffer size with the
[04:37] help of the second constructor.
[04:39] So whenever you are trying to create the object of BufferReader, you can try to provide the object
[04:44] of Reader.
[04:45] And the second parameter is size
[04:47] but for the most of the scenarios, this default size should be good enough, like 8192.
[04:53] If needed, you can increase based upon your business requirements in real projects.
[04:58] So now I'm assuming
[04:59] you are clear why these processes are efficient, especially while reading the data from the file.
[05:05] Maybe when you are trying to access the data from an end user.
[05:09] Maybe in those scenarios, these buffer size may not be super helpful because the end user at max he
[05:14] may enter a value, a character, or a word or a sentence.
[05:18] But in the scenarios of file reading, this buffer size is going to bring a lot of efficiency.
[05:23] I hope you are clear about the introduction of the BufferReader in the next lecture
[05:27] using the constructors that we have inside this BufferReader class, we can try to create an object
[05:32] of BufferReader, and we can try to accept the input data from an end user.
[05:38] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
