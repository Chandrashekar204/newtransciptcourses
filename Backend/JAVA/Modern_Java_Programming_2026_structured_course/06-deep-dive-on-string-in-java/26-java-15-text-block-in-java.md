# 6.26 — [JAVA 15] Text Block in Java

> Section 6: Deep dive on String in Java

[00:00] Think like, I want to store this exact text data with the help of String data type.
[00:06] You may have a question here.
[00:07] What is so special about this String we saw previously, we were able to store any kind of data with
[00:12] the help of String.
[00:14] The speciality of this String is, after the word John
[00:17] I pressed enter.
[00:19] The next content is moved to the next line.
[00:22] So I want to store the exact text data along with the moving of the sentence to the next line after
[00:28] the John word.
[00:29] Let's try to store the same with the help of String data type.
[00:32] Obviously we are going to face some challenges once we saw the challenges.
[00:36] I'm going to show you how to overcome those challenges.
[00:39] To show you the demo, I'm going to create a new class here.
[00:43] The class name is going to be TextBlockDemo.
[00:47] You'll come to know in few minutes why I'm giving the class name as TextBlock.
[00:51] Inside this class I want to create a main() method, and inside the main() method I want to create a String
[00:57] object with the name input.
[01:00] Now to this input object I want to assign the String data and the String data is going to be
[01:06] Hello,
[01:07] my name is John and after the John we want to move to the next line and I want the same to be stored
[01:15] inside my input String data.
[01:17] So to move to the next line I'm going to press the enter inside my keyboard.
[01:22] As soon as I try to press enter, you can see what is going to happen.
[01:25] My IntelliJ Idea created a new empty String and the new empty string and the previously typed string
[01:32] it is trying to concatenate with the help of this plus symbol.
[01:36] That means whenever I want to move to the next line with the help of the String data type, definitely
[01:41] this plus symbol is going to come, and whatever I want to type in the next line, I need to type it
[01:47] as another string.
[01:48] And at the end of the day, both my Strings
[01:50] they are going to be combined and they are going to be assigned to the input object.
[01:54] Let me type here the next content.
[01:57] The next content is and I am 25 years old.
[02:02] At last I'll keep a full stop.
[02:04] And now, as a next step, let me try to print out this string data and let's try to understand how
[02:11] this is going to be saved behind the scenes.
[02:13] So if I try to execute this program, you can see I got a statement which is Hello, my name is John
[02:20] and there is no space after John and after the John word we have and I am 25 years old, that means
[02:27] everything is getting saved as a single line.
[02:31] Sometimes you may get some requirements inside your real projects where you have to save the string
[02:36] data along with the content, like moving to the next line, pressing the enter so all such things
[02:41] if you want to save then this option, whatever we are considering it is not going to work.
[02:45] So how to introduce the next line between these two strings?
[02:49] One approach is with the help of \n, so we can mention \n.
[02:56] And behind the scenes the JVM is going to consider this as a next line.
[03:00] And whatever content that we have mentioned here this is going to be printed in the next line.
[03:05] Now let me try to execute this program.
[03:07] This time you can see the two strings are displayed in two different lines like we are expecting.
[03:13] So this is one of the basic approach.
[03:16] But this is a super inconvenient process.
[03:19] Think like I want to store some HTML code or some SQL queries inside my String in such scenarios
[03:26] let me show you how inconvenience this approach is,
[03:30] to save some time
[03:31] here I'm trying to paste a few lines of code.
[03:35] You can see this is the code that I'm trying to paste here
[03:38] it should be pretty clear for you.
[03:39] I'm trying to create an object of String with the name HTML code, and inside this HTML code object,
[03:45] I'm trying to save some HTML code like HTML, and inside the HTML we are going to have body, and inside
[03:51] the body we are going to have paragraph and inside the paragraph I'm trying to have a content which
[03:56] is Hello World.
[03:58] And at last I'm trying to close the body tag and HTML tag.
[04:02] I'm assuming you are aware about the basics of HTML.
[04:04] If not, don't worry.
[04:05] Please just focus on the problem that we are facing with this approach.
[04:10] If I try to print these HTML code object, you'll be able to see all my HTML code is going to be displayed
[04:17] properly in multiple lines, like here you can see its , , ,, and .
[04:24] So how this is possible because we are using these \n at the end of the each line.
[04:30] That's why our string is getting moved into the next line whenever we are trying to print the same on
[04:36] the console.
[04:36] But don't you think this is very inconvenience to the developers every time giving this \n?
[04:42] And for some reason, if they forget mentioning a \n, then obviously your string data is not
[04:48] going to be saved properly.
[04:50] So to solve these kind of challenges inside Java 15 version, a new syntax of string literal is introduced.
[04:58] And this new syntax literal
[05:00] we call it as text block.
[05:02] That's why I have given that name to this class as TextBlock.
[05:05] Now let me show you how easy it is to print the same kind of HTML code with the help of text block syntax.
[05:12] For the same,
[05:13] first I am going to create a String object with the name textBlock.
[05:18] After defining the textBlock string object, we need to press the double quotes three times.
[05:24] So I'm trying to press double quotes three times.
[05:27] So you can see as soon as I try to press double quotes three times my intelliJ, it is also giving
[05:32] me the another set of three double quotes.
[05:35] So we need to close the statement here with the help of semicolon.
[05:38] Now you can see this is the starting for my String and this is the end for my String.
[05:44] Inside these two pairs of triple, double quotes, I can type whatever I want when I'm typing my string
[05:52] data.
[05:52] If I press enter behind the scenes, my text block is going to retain whatever I am typing, including
[06:00] the enter button.
[06:01] Let me type some content here very quickly.
[06:04] So to type the content in between these two symbols, we need to press enter first
[06:09] and I'm going to type first and post that
[06:14] I'm going to press enter and I'll give some tab space
[06:17] and here and this time I'm going to type followed by enter
[06:23] and after the body I'm going to give .
[06:26] And after giving the I'm going to type Hello World.
[06:32] And I'm going to close the paragraph.
[06:34] And after closing the paragraph I'm going to come back to the same position where I have the tag.
[06:40] So here the tag started.
[06:42] So after coming to the same position, I'm going to close the tag and post that
[06:47] I'm going to press enter and I'll move back to the same position where my tag is started.
[06:53] So this is the place where it has started.
[06:55] Here I'm going to type closing tag of .
[06:58] So you can see this time I just typed very freely without worrying about the next line tab spaces.
[07:05] So this is like typing inside your word document or inside a text file.
[07:09] So now let me show you how the output is going to look like.
[07:13] For the same,
[07:13] I'm going to print the textBlock object.
[07:17] If I try to print this this time, you will be able to see the beauty of the textBlock.
[07:22] So whatever I have typed, the same exactly is saved inside my String object, and during my typing
[07:29] I might have used an enter button, or I might have used a tab space.
[07:34] So all such kind of special characters or special
[07:37] control buttons are also going to be captured by my String object whenever I'm using these textBlock
[07:44] syntax, which is
[07:45] I need to mention the double quotes three times at the starting and at the end
[07:49] also, I need to mention three double quotes in between these symbols
[07:54] you can type whatever you want and whatever you type, the same exact sentence or string data is going
[08:00] to be saved inside the String object.
[08:03] I hope you are clear the advantage of TextBlock for your quick reference.
[08:08] I have mentioned the details about the text block in Java in these two slides, so please refer them
[08:14] whenever you have some questions.
[08:15] The text block syntax we can also use in the scenario of format string as well.
[08:21] Here you can see I have created a message String object with the help of text block syntax.
[08:25] And inside the string I'm trying to use some placeholders like %s and % d, and after
[08:32] mentioning the placeholders, I'm sending this message object as an input to the format() method.
[08:37] This means text blocks
[08:38] they are also allow you to define a format string with the help of placeholders.
[08:43] But please note that like I highlighted in the slide, this option is available only from the Java 15
[08:51] version.
[08:51] If you are going to work in an real project which is using the Java version like eight and 11, then
[08:58] obviously you cannot use these feature.
[09:01] So to use this feature, you should have at least JDK 15 at Java 15 installed inside your system.
[09:08] I hope you are clear.
[09:09] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
