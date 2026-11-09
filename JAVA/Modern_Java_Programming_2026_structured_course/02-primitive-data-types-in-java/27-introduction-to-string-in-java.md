# 2.27 — Introduction to String in Java

> Section 2: Primitive data types in Java

[00:00] As of now, we discussed all the primitive data types available inside the Java programming language
[00:06] around these primitive types
[00:07] we explore a lot many demos and examples.
[00:10] My humble request for you is to practice all the examples that I have provided.
[00:15] On top of that, you can try to do more practice, do mistakes and from the mistakes, please try to
[00:21] learn the concepts of Java programming language.
[00:24] Inside this lecture, I want you to introduce to a special data type and the name of this data type
[00:30] is String.
[00:30] With the primitive data types that we have discussed previously, we can store all kind of data except
[00:37] text data, anywhere
[00:38] did I show you how to store a text value or a word or a sentence?
[00:42] I have not showed you, because these primitive data types are not capable of storing a complete word
[00:48] or a complete sentence.
[00:49] Off course we have char, but char is capable of storing only a single character, but not a word or a
[00:56] sentence.
[00:56] So to store some text data, we need to use string data type.
[01:00] So let's try to understand
[01:01] the same. String is not a primitive data type
[01:04] inside a Java. I'm going to discuss why it is not a primitive data type in few seconds, but like I said
[01:10] previously, with the help of String, we can store a sequence of characters and the sequence of characters
[01:16] can be of any length.
[01:18] You can store a simple word, or you can store a sentence, or you can store entire data inside a book.
[01:24] The length can be anything, regardless of length of your data.
[01:27] String is capable of storing any amount of data.
[01:31] For example, if you want to store a word Java with the help of String, you can simply assign the Java
[01:36] word to the String variable,
[01:38] but please make sure we have to mention the words or text inside
[01:42] double quotes.
[01:43] Whenever you are trying to store data with the help of String data type, the only thumb rule that we
[01:48] need to follow is the data should be surrounded by the double quotes, whereas with the char primitive data
[01:53] type we use single quotes.
[01:55] I said String is not a primitive data type.
[01:58] Then what is this data type?
[01:59] String is an reference data type.
[02:02] When I gave introduction about primitive data type, I also told you that there are reference data types
[02:07] also available inside Java.
[02:09] Using these reference data types, we can store complex data and if needed, we can create our own custom
[02:16] reference data type.
[02:17] For example, if I want to store details of a person like his name, age, what is his date of birth,
[02:23] what is his address?
[02:24] So if I want to store all the data related to a person in a single place, then I can create my own
[02:31] person reference data type and using that person data type I can store the person related information.
[02:37] We are going to explore more about reference data types in the coming lectures, but for now, please
[02:42] note that String is not a primitive data type, it is an reference data type.
[02:46] The next question you may have is what is the syntax that we need to follow whenever we want to assign
[02:52] or whenever we want to store data with the help of String?
[02:55] The syntax is very similar, just like how we mentioned for primitive data types, even for String,
[03:00] also, we need to follow the same syntax like I can give String input is going to be the variable name
[03:06] and what is the text that I want to assign.
[03:08] So here you can see Hello World exclamatory (!) mark I'm trying to assign to the variable input. By default
[03:15] if you don't assign any value and if you are doing only the declaration but not the initialization,
[03:21] your string is going to hold null value, which is the default value for String.
[03:25] So what does null represents?
[03:27] null represents inside Java, there is no data inside that particular variable.
[03:32] But instead of simply declaring like String input, it is always recommended or a good practice to initialize
[03:39] it with a null.
[03:40] So whoever is trying to use your String input variable inside their methods or inside their classes,
[03:46] they'll have information that your variable may have null value, and they'll be very cautious while
[03:52] dealing with the null value.
[03:54] Because whenever we are trying to deal with null values, there is a chance that we may receive
[03:58] NullPointerException.
[04:00] We are going to discuss about what is an exception error, how to handle exceptions in the coming sections.
[04:05] But for now, I just wanted to let you know.
[04:07] Always please try to declare your string at least with a null value.
[04:12] Maybe after few lines of your Java code based upon your requirements, you can change the value inside
[04:18] your String with whatever text that you want.
[04:20] Now I want to answer your burning question, which is why String is not a primitive data type, why
[04:26] it is an reference data type.
[04:28] The reason is very simple.
[04:30] We never know what is the amount of data that a developer is going to store inside a String variable.
[04:36] So here I am trying to assign a Java or Hello world.
[04:39] Very similarly, a person can assign 1 million characters or 1 million words, or he can try to mention
[04:47] the data from an entire book.
[04:50] Since we cannot control what kind of data that developers are, people may save into the String
[04:56] we can't keep it as a primitive data type, because if you go with the
[05:00] primitive data type, it should always have a specific size specific range, whereas with the String,
[05:05] since this is not possible, this String is developed as a reference data type inside Java.
[05:10] So what is the beauty of reference data type?
[05:12] With the help of reference data type, we can store any amount of data.
[05:17] So based upon the volume of our data, the memory inside your computer is going to be assigned for that
[05:23] variable.
[05:24] If your String variable is going to have 100 words, then the memory for that is going to be assigned
[05:29] by your computer.
[05:30] Whereas the other developer who is trying to assign 1 million words, then the memory requirement for
[05:36] that developer is going to be different.
[05:38] So based upon the amount of data, the memory allocation will happen at runtime.
[05:43] So that's why String is marked as a reference data type inside Java.
[05:49] So there is lot of concept behind String.
[05:52] That's why I'm going to discuss more details about String in the coming sections,
[05:57] we are going to have very in detail discussion about String.
[06:00] But for now I just wanted to give a very quick introduction about what is String, how to store text
[06:06] with the help of String.
[06:07] Let's see the demo of String data type in the next lecture.
[06:11] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
