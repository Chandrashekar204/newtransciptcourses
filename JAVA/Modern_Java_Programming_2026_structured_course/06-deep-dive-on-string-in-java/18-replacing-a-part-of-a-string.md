# 6.18 — Replacing a part of a String

> Section 6: Deep dive on String in Java

[00:00] Sometimes you may have a requirement to replace a specific content of your String with a new content.
[00:08] For all such scenarios, we have a replace() method available inside the String with the help of this
[00:14] non-static or instance method, which is available inside the String class, we can replace occurrences
[00:22] of a specific character or sequence of characters in a original String with another character or another
[00:29] String data.
[00:30] When I say replace() method, there are multiple overloaded methods available inside the String class.
[00:37] Let's try to understand what are those under which scenarios we have to use them.
[00:41] The very first type of replace() method, it is going to accept two char values.
[00:46] What is the old char and what is the new char?
[00:49] When you invoke this replace() method on top of a original String, whatever old char that are available
[00:56] inside your String, they are going to be replaced with the new char value that you have provided.
[01:01] For example, here I have the original String as Hello world!
[01:05] Using the object of this original string, I invoke the replace() method, and to this replace() method
[01:12] I have mentioned the old char as well and the new char as asterisk mark.
[01:17] With that, all the old characters available inside my original string, they are going to be replaced
[01:23] with the asterisk mark.
[01:24] And this is how the output is going to look like.
[01:27] Just like how we can provide the char values as an input to the replace() method.
[01:32] We can also provide a sequence of char values, which means we can provide the String data here.
[01:38] Inside this example, I'm trying to invoke the replace() method.
[01:42] And to this replace() method, first I'm trying to pass what is the existing word inside my original string.
[01:49] So I'm trying to pass the word which is already present inside my String and this world word
[01:55] I want to be replaced with a new String value, which is universe.
[01:59] That's why I'm going to get the output as Hello Universe.
[02:02] So both of these two replace() methods
[02:04] they are going to be case sensitive.
[02:07] So when you try to replace a String, please give the accurate case sensitive details.
[02:12] Otherwise you're not going to get the expected output.
[02:15] Let me show you one more example of this replace() method.
[02:19] Here you can see I have a original string where I have the string like abababab.
[02:25] If I invoke the replace() method and try to pass the old String value as ab and the new String value
[02:32] X, then all the sequence of characters which are like a b, they are going to be replaced with an
[02:38] X.
[02:39] That's why I'm going to get an output as XXXX, which means my x is going to be repeated four times
[02:47] wherever ab is present inside my original string.
[02:50] I hope you are clear with this example.
[02:52] Apart from the replace() method, we also have replaceAll() method.
[02:56] This replaceAll() method
[02:58] it is going to accept an regular expression or in short form we can call it as regex
[03:04] And the second parameter it is going to accept is what is the replacement or what is the new string
[03:08] that we want to replace.
[03:10] Here I have provided an example for replaceAll() method.
[03:13] I have an original string which is Java is fun!.
[03:19] On top of this String object I want to invoke replaceAll() method but the replaceAll() method
[03:25] first we need to pass what is our regular expression.
[03:28] So here I'm trying to pass a regular expression like a e i o u, which are separated by a pipe symbol.
[03:35] And the second input parameter that I am providing for the replaceAll() method is string representation
[03:41] of the asterisk symbol.
[03:43] With this
[03:43] what I'm trying to convey to the replaceAll() method is
[03:46] please check if there are any vowels inside my string like a e i o u which are in small letters.
[03:54] replaceAll() these vowel letters with the asterisk symbol.
[03:58] That's why inside the output you can see all my small case vowels
[04:02] letters are replaced with the asterisk mark.
[04:05] So what is the purpose of this pipe symbol inside the regular expression?
[04:08] It is a kind of or condition.
[04:10] So I'm telling any of these characters if they're present inside my original string, please replace
[04:16] all of them with the asterisk.
[04:18] Off course, our replace() method also is going to replace all the occurrences, but the only difference
[04:23] between replace() and replaceAll() method is the replaceAll() method is going to accept the regular expression
[04:30] as an input.
[04:31] So this is going to be handy for the complex replacement requirements.
[04:36] One such example that we saw here is replacing all small case vowel letters with the asterisk.
[04:42] And the next flavor of replace() method available is replaceFirst().
[04:47] This is very similar to replaceAll(), but this replaceFirst() method is going to replace only the first
[04:53] match found in the original string.
[04:55] Here you can see for the replaceFirst() method I'm passing the
[04:59] regular expression which is apple.
[05:02] So here my regular expression is not complex because I'm directly providing an string literal value,
[05:08] which is apple.
[05:09] That means my replaceFirst() is going to look for the apple word inside my original string, and the
[05:15] same is going to be replaced with the grape value.
[05:18] So this is the input, and this is how the output is going to be.
[05:22] Only the first apple word is replaced with the grape, whereas the second apple word and third apple
[05:28] words, they are not replaced in the original string because we are using the replaceFirst() method.
[05:34] Let's see the demo of all these replace methods inside intelliJ.
[05:38] To show the demo of replace related methods, I have created a class with the name StringReplaceDemo,
[05:44] and inside this class there is a main() method I have created, and inside the main() method I have created
[05:50] an String object which is holding the value,
[05:53] Hello, World !.
[05:56] Here
[05:57] first I'm going to create a string object with the name replaced string and post that
[06:03] using the original string object
[06:06] I'm going to invoke the replace() method and you can see we have various flavors of replace methods.
[06:12] But now I want to invoke the first replace() method, which is going to accept the old char and the new
[06:18] char. To this method
[06:20] first I'm going to mention what is the old char that I want to replace.
[06:24] I'll give the small o, and this small o, I want to replace with asterisk mark.
[06:29] That's why I'm trying to give the asterisk mark.
[06:31] So whenever we want to provide char values we need to use a single quotes.
[06:35] That's why I'm trying to use the same here.
[06:37] Next I want to show you the other flavor of replace() method for the same
[06:42] let me change this variable name to replacedString1 and post that
[06:46] this time I'm going to invoke the replace() method, which is going to accept the char sequence.
[06:53] When I say char sequence, what are those,
[06:55] it is a String.
[06:56] Inside String we have a sequence of characters.
[06:59] So whenever someone is telling char sequence, it is nothing but a String.
[07:02] So let me try to pass the first string, which is World, and the next string I'm going to mention as
[07:10] Universe.
[07:11] With this, the world world is going to be replaced with the universe world as a next step.
[07:17] Let me show you a negative scenario as well.
[07:19] Maybe I'll try to create one more string object with the name replacedString2.
[07:25] Here this time I'll try to give a small case of w letter, and with this my replace() method cannot identify
[07:32] a word with a small w inside my original string, and with that they will not be any replacement happen.
[07:38] We can also confirm the same in few seconds.
[07:41] Now let me create one more string for the same
[07:44] let me copy the first line and I'm going to change this name to originalString1.
[07:49] And for this string I'm going to pass the data as abababab.
[07:55] So I'm trying to repeat the ab 4 times.
[07:58] Now as a next step, let me try to invoke the replace() method on top of this originalString1.
[08:04] Before that, let me rename this to the
[08:07] replacedString3 to avoid the compilation error.
[08:10] For this replace() method, I want to pass ab as a old string value, and the new value that I want to
[08:16] replace here is X.
[08:18] So with this line of code, all the ab occurrences inside your original String, they are going to
[08:24] be replaced with the X value.
[08:26] Now let me show you how to invoke the replaceAll() method for the same
[08:31] first, let me create a string object with the name originalString2, and inside this originalString2 variable,
[08:37] I'm going to store a string data, which is Java is fun!.
[08:46] Now using this originalString2 I want to invoke the replaceAll() method for the same
[08:53] first, let me create a String object with the name replacedString4 and post that with the help
[09:00] of originalString2
[09:01] Object.
[09:02] I'm going to invoke the replaceAll() method.
[09:05] You can see there is only one replaceAll() method, which is going to accept the regular expression as
[09:11] a first parameter and the second parameter,
[09:13] what is the replacement string?
[09:15] And the return type from this method is going to be the new string with the replaced values.
[09:21] So let me invoke this and to this method I'm going to pass a regular expression which
[09:29] a | e | i | o | u.
[09:33] And you with this regular expression, I'm trying to replace all the lowercase vowel letters inside
[09:41] my string value with a new String data, which is asterisk.
[09:45] We can see the demo as well in few seconds.
[09:47] Before that, let me try to show you how to invoke the replaceFirst() method to show the demo of
[09:54] replaceFirst() method.
[09:55] First, let me copy these two lines and paste it at the end of the main() method.
[09:59] So
[09:59] I'm going to create a new String object with the name orginalString3.
[10:04] And inside this string I'm going to store some fruits names which are separated by a space value like
[10:11] apple space orange
[10:13] space.
[10:14] apple
[10:15] space
[10:16] banana
[10:17] space
[10:17] apple
[10:18] Now, using this originalString3 object, I want to invoke the replaceFirst() method.
[10:25] So this replaceFirst() method is also going to accept the regular expression
[10:30] and what is the replacement string.
[10:31] So here my requirement is very simple to replace the first occurrence of the apple word.
[10:38] That's why I'm going to do the regular expression as apple itself.
[10:42] So this is also one type of regular expression where my regular expression is going to look for exact
[10:49] word apple inside my String.
[10:51] Whenever it is identifies, it is going to replace with the new string, which is grape, but the replacement
[10:58] operation is going to happen only once because we are trying to use our replaceFirst() method.
[11:04] Now, let me put a breakpoint on the top and post that we can try to execute the program and see how
[11:09] this replace methods are working at runtime.
[11:12] So let me run my program using debug option.
[11:15] You can see the breakpoint stopped at the line number four.
[11:19] So we can use this step over button to move our Java execution line by line.
[11:25] Otherwise we can also use the F8 shortcut.
[11:28] So let me use the F8 shortcut here.
[11:31] So I'm pressing F8.
[11:32] You can see right now the execution moved into the next line.
[11:36] But the execution at the line number two is not completed.
[11:39] That's why I'm not able to see the what is the value inside the replaced string variable.
[11:45] If I move the execution to the next line, then the previous line execution is going to complete and
[11:50] you can see the replacedString as a value Hell*, W*rld
[12:00] and ! mark
[12:00] Let's see the output from the remaining replace() method statements as well.
[12:04] So I'm pressing F8 here
[12:06] also, we got the expected output.
[12:08] The world is replaced with universe from the next line execution
[12:12] the replaced string should have the same original value, which is hello world.
[12:16] The reason is here we use the lowercase w value and with that the replace operation is not going to
[12:24] find any word matching the same case sensitive values inside my original string.
[12:29] That's why even my replacedString2 value is holding the original value that we stored inside the
[12:36] original string object.
[12:37] Now, let me try to move on to the next lines and the replacedString3 object
[12:43] you will be able to see the output as XXXX, because we are trying to replace every occurrence of
[12:49] a b with a single X, let me move the execution to the next lines by pressing F8, and here you can
[12:56] see my replacedString4 have asterisk symbol in all the places where I have the lowercase vowel
[13:04] values.
[13:05] So this is the power of replaceAll() method, because it is going to accept the regular expression as
[13:12] an input.
[13:12] Now I can execute the last two lines by pressing F8 and you can see the value inside the originalString5
[13:20] has grape, orange,
[13:22] apple,
[13:23] banana,
[13:24] apple.
[13:24] That means only the first occurrence of apple is replaced with the grape value.
[13:30] I hope you are clear with all these discussions.
[13:32] Please try with various combinations of input data and see the behavior of all the flavors of replace
[13:38] methods that we have discussed inside this lecture.
[13:41] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
