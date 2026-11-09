# 6.13 — Changing the case in String

> Section 6: Deep dive on String in Java

[00:00] Under a few scenarios, you may want to display your String data in entire capital letter or in entire
[00:07] small case letter.
[00:08] I can also provide you an real time scenario.
[00:11] Think like an end user entered some text inside a website, and the input he has entered is a combination
[00:19] of both small letter and capital letter.
[00:21] But before you try to save that data into the database, you may want to convert that entire String
[00:27] data entered by the end user either into completely capital letter or completely lowercase letter.
[00:33] So in this kind of scenario, the requirement is very clear.
[00:36] We want to change the case of the content inside a String object.
[00:40] But these kind of scenarios, we have certain methods inside String that we can leverage to change the
[00:46] case very easily.
[00:48] Let's try to see what are those methods under String
[00:51] we have two types of instance methods or non-static methods.
[00:55] And these method names are very self-explanatory.
[00:58] The methods are toUpperCase(), which is going to convert your String data entirely into the capital
[01:04] letter.
[01:05] And the other method that we have is toLowerCase().
[01:08] This toLowerCase() method is going to completely convert your letters inside your String data into lowercase
[01:15] format.
[01:16] For example, here you can see
[01:17] first I have created an original String with a value Java J is capital letter and the remaining letters
[01:24] are completely in small letter. Using these original String object
[01:28] if I try to invoke that two uppercase, all the content of Java is going to be converted into uppercase
[01:35] letter.
[01:36] But if I invoke toLowerCase() method, then the content of the Java word is going to be converted into
[01:42] completely lowercase.
[01:44] So here we are trying to change the content of the original String into a completely different case
[01:51] based upon our requirements.
[01:53] And I want to highlight one more time about the String immutability here as well.
[01:58] We know that the content of the String once created, they are immutable.
[02:02] That means the content of the String object are going to be unchangeable.
[02:06] So here you can see first I have original String.
[02:09] So inside this object we are going to have this content.
[02:12] But when I'm trying to invoke these toUppercase() and toLowerCase(), I'm trying to catch the output
[02:17] in a separate String object.
[02:19] That means the original data that we have inside the original String is not going to change.
[02:25] But here you may have a question, which is what if I assign the output from the toUpperCase() and
[02:31] toLowercase() to the same String object, which is original String?
[02:35] Let's see how the code is going to look like for this scenario
[02:38] like you can see here, I'm trying to invoke the toUpperCase() method from the original String object.
[02:44] The output from the toUpperCase() method I'm trying to assign back to the same object original String.
[02:50] So this is going to give an illusion that we are able to change the content of String object, but we
[02:56] can't change the content of String object once it is created.
[03:00] What is going to happen behind the scenes when we run this code is think like when we ran the first
[03:05] line of code.
[03:06] The original String object is pointing to a memory location called one, two, three.
[03:12] Inside these memory location 123 we have these original String, which is Java, where J is capital
[03:19] letter.
[03:19] Behind the scenes, the JVM is going to create a new memory location, maybe 456
[03:25] and inside this new memory location, the new string content, which is Java in capital letters is going
[03:32] to be saved.
[03:32] And my original String object reference is going to point to the new memory location 456.
[03:39] Then what is going to happen to the old memory location which is 123?
[03:43] Obviously our friend Garbage collector is going to remove that memory location after few seconds.
[03:50] Now I just wanted to give a very quick introduction, or I just wanted to give some hints how the immutability
[03:57] of the String is going to work.
[03:58] I hope you are clear with this.
[04:00] Now let's create a Java program and try to invoke these methods.
[04:04] Here I'm going to create a new Java class, and the Java class name is going to be ChangeCaseDemo.
[04:12] Inside this class
[04:13] as usual, the very first drill that we need to do is, to create the public static void main().
[04:18] First I'm going to create an String with the variable name as original String.
[04:25] And inside this I'm going to store the data Java where j is capital and remaining
[04:31] all letters are in small letter.
[04:33] Now using these original String, I can invoke that to toUppercase() and toLowercase().
[04:38] Before I try to invoke those methods, let me try to create an String object with the name upperCaseString
[04:45] .
[04:46] And to this object I'm going to assign the output that we are going to get from the toUpperCase() method.
[04:52] So how to invoke the toUpperCase() method?
[04:55] We can invoke the toUpperCase() method with the help of String object
[04:58] The String object that we
[05:00] can use.
[05:00] Here is original String.
[05:02] On top of this String object I can invoke toUpperCase().
[05:06] Very similarly, I can try to invoke the toLowerCase() as well.
[05:11] Let me invoke this and let me change the variable name toLowerCaseString.
[05:17] If I try to execute this program by keeping a breakpoint here, we should be able to see the output
[05:23] like upperCaseString object has a content with a complete capital letters, whereas lowerCaseString
[05:30] object has a content with a completely small letters.
[05:33] Let me release this breakpoint as a next step
[05:35] I want to do some tricky input to my toUpperCase() and toLowerCase() method.
[05:41] So what I can do is I can copy these three lines of code.
[05:44] This time I'm going to give some numeric values and special character values as well, along with few
[05:52] characters like Java best.
[05:55] But between Java and best, I have mentioned some numeric values and special symbol.
[06:01] Let me change this variable name to specialString.
[06:05] The same string object I can use in the next few lines to invoke that toUpperCase() and toLowerCase().
[06:12] And here I need to change the variable names because we already have these variable names used in the
[06:17] top
[06:18] that's why I'm getting the compilation error.
[06:20] Let me change this variable name to specialUpperCaseString.
[06:25] And here also I'm going to mention specialLowerCaseString.
[06:30] If I try to execute this program you can see all the numeric values and the special symbols
[06:36] they are not going to be affected any way because there is no uppercase and lowercase for special symbols
[06:43] and numeric values, only the alpha values like j a, v, b, e, s, t those are getting converted to the
[06:51] uppercase value, and similarly you can see specialLowerCaseString has content with all lowercase
[06:58] values.
[06:58] I hope you are clear with these special input that we have given.
[07:01] Let me release this breakpoint.
[07:03] Now before I try to close this lecture, I want to share one more important update about the toUpperCase
[07:09] and toLowerCase() method for the same
[07:12] let me open these toUpperCase()method which is available inside the String.java.
[07:16] Here I'm going to look for the method which is starting with toUpperCase().
[07:22] And you can see we have two methods.
[07:25] We thought there is only one method which we can invoke always.
[07:28] As of now, we invoke the first method which is not accepting any input parameter.
[07:33] But there is another method with the same name, but it is accepting the Locale as an input parameter.
[07:40] So let's try to understand what is the purpose of this method.
[07:43] For the same I'm opening this method.
[07:45] We can read the documentation here
[07:48] what they're saying is sometimes you may be storing other language data, not only the English alphabets.
[07:55] Maybe you might be storing some data with the help of Turkish characters or German or French or Spanish.
[08:02] So regardless of whatever language that you are trying to use, you need to let the JVM know what is
[08:09] the language that you are trying to use, so that the JVM is going to consider all the rules and regulations
[08:15] that it needs to follow.
[08:17] Whenever it is trying to convert a lowercase letter to the uppercase letter or uppercase to lowercase
[08:22] letter.
[08:23] Here you can see they have given an example.
[08:26] This is a word which has all complete lowercase letters.
[08:29] If you try to convert this to all capital letters, this is how it is going to look like.
[08:34] I'm not sure what language it is, but you can see you have some two dots on the top.
[08:39] If you try to use the default toUpperCase() and toLowerCase() method, your JVM will not know which
[08:45] which language characters you are trying to convert.
[08:48] So to let the JVM know about which language you are trying to use, we need to pass such information
[08:54] with the help of this Locale.
[08:56] Let me open this Locale.
[08:57] Inside this Locale you can see we have so many constants like English, French, German, Italian, Japanese,
[09:04] Korean.
[09:04] So based upon your language, whenever you are trying to invoke the toUpperCase() method, you need
[09:10] to pass these constants.
[09:11] For example, I can also show you a demo here.
[09:14] Think like I want to send the German as an local.
[09:18] So first I need to mention Locale.
[09:20] After the Locale I need to invoke the static variable which is German.
[09:26] With this now my JVM know that it has to follow the standards of German language whenever it is trying
[09:32] to convert the lowercase letter to the uppercase letter.
[09:35] Very similarly, we can also pass local information for the toLowerCase() as well.
[09:41] But in most of the scenarios, you don't have to pass this local because 90% of the projects they are
[09:47] going to store the English characters inside the database.
[09:51] But for some reason, if you're working on a project where you have to store that data using a specific
[09:57] language, then you can obviously use these local.
[10:00] Locale is a concept inside programming languages, which represents the language and the region that
[10:06] we are trying to consider when we try to execute the program.
[10:10] I'm assuming you are clear with these explanation.
[10:12] Let me roll back to the previous normal methods like toUpperCase() and toLowerCase().
[10:18] But I just wanted to share this extra information so that this can be useful for the interviews, where
[10:23] people may try to ask you some tricky questions around this.
[10:27] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
