# 13.11 — Introduction to Scanner & Demo - Part 2

> Section 13: Accept input using BufferedReader and Scanner

[00:00] In the previous lecture
[00:01] we built these basic Java classes with the help of for your class, and because of this program is able
[00:08] to accept the named as person and the age of a person.
[00:11] And at the end we are adding the name element of the person.
[00:15] Now let me share
[00:16] you an
[00:17] important and interesting concept about the next method. To demo make the same,
[00:22] I'm going to run this program. This time I'm going to give my name in two words like Madan space
[00:29] Reddy.
[00:31] As I press enter we are you can see to getting an InputMismatchException.
[00:37] The reason going to getting this exception is,
[00:39] whenever we using the next() method it is going to read the very first word and
[00:45] second word which is seperated by a space it will be treated as
[00:49] a next token and the input stream.
[00:52] That's why it is not trying to waiting for me to input after
[00:56] this statement which is enter your age instead it is going with the second word as my age details
[01:04] and since the alphabets is an invalid to read with the help I'm nextInt() we are getting an
[01:11] runtime exception.
[01:12] Okay, so to resolve this kind exception
[01:14] you need to make sure you are using the nextLine() method.
[01:19] So the difference between next() and nextLine() method is, next() is only capable of reading a single word,
[01:26] whereas with the nextLine() method it is going to read the entire data inside a line until you press
[01:32] the enter button.
[01:33] So let me show you the demo of the same.
[01:35] So this time again I'm trying to run this program.
[01:38] Here it is asking me my name.
[01:40] I'll try to provide my name in two words which are separated by space, and I'm pressing enter.
[01:46] And this time you can see it is asking me to provide my age details.
[01:51] I'm going to mention 25 and press enter.
[01:54] And with that we are getting our output successfully, which is Hello Madan Reddy
[01:59] you are 25 years old.
[02:01] It's very nice to hear this statement because I became anger with this statement.
[02:06] Right now I'm 25 years old only I'm just kidding
[02:09] let's move to the next topic.
[02:11] What I'm going to do right now is I'm going to rebuild the logic of PrimeNumberChecker with the help
[02:17] of Scanner class.
[02:19] So for the same, I'm going to copy this class and paste it inside the same package, the class name
[02:24] I'll give it as PrimeNumberCheckerScanner because we are going to use a Scanner class here.
[02:30] So now inside this program we can make the changes very easily.
[02:35] But before that I want you to pause the video and try updating this logic and see if it is working everything
[02:41] properly for you.
[02:42] Otherwise, don't worry, there is nothing wrong facing issues
[02:46] when you try to execute a Java program, it's not going to end the world.
[02:50] You're going to get lot of chances to improve your coding skills.
[02:54] So now first I'm going to create the object of Scanner.
[02:57] For the same
[02:58] I'm going to copy the code from the ScannerDemo class.
[03:02] So this is the code that I can copy and paste it inside my PrimeNumberCheckerScanner class.
[03:08] And with that we don't have to handle these IOException I can simply remove these throws statement followed
[03:14] by I can keep these System.out.println() without making any changes.
[03:19] Next, using the when Scanner objects and I'm going to invoke a nextInt() method because
[03:26] I know my of end user is to enter a numeric value.
[03:30] That's why code and to invoke this nextInt() method and the same
[03:34] I need to accept on the left hand side with the variable name as num and try to that we don't need this all on
[03:40] parsing related code.
[03:42] I can data remove it these three num variable we are going to
[03:45] send as an input to is isPrime()
[03:49] and towards the end instead bf, I can say sc.close(). So with this year should be good
[03:55] let me just execute
[03:56] this program is going to run and that numerical value which is 101
[04:01] and I'm getting an desired output which is, Given number is a Prime number.
[04:06] I hope you're clear about the advantage that we are getting with the Scanner class.
[04:10] All the details that we have discussed, I have mentioned in this slide, and apart from that, I also
[04:16] highlighted about the important methods available inside the Scanner class.
[04:20] So you can use next()
[04:22] nextInt(), nextBoolean().
[04:23] nextFloat(), nextDouble(),
[04:25] nextLine().
[04:26] nextLong().
[04:26] nextShort(), nextByte().
[04:28] So these are the most commonly used other than that
[04:30] we also have other type of next methods which you can use based upon input data
[04:37] entered by the end user.
[04:39] And please note that there is a difference between next() and nextLine().
[04:42] Whenever you are using next() method, it is only capable of reading a single word from the end user input
[04:49] data, whereas nextLine() it is capable to read an entire String value from the end user until a enter
[04:57] button is pressed by the end user.
[04:59] Just like how we have next related methods, we also have has related methods inside the Scanner class.
[05:06] So these methods are hasNext(), hasNextInt(), hasNextFloat(), hasNextDouble(), hasNextLine(), hasNextLong(),
[05:15] hasNextShot(), hasNextByte().
[05:17] So these methods we can invoke to understand if there is any token available inside the stream before
[05:25] we try to fetch the data with the help of next methods.
[05:29] So whenever we invoke these has related methods, we are going to get a boolean value, whether the
[05:34] next token or the next data is available inside the stream data.
[05:38] If yes, we can invoke these next related methods to actually read the data from the StreamInputStream.
[05:45] So these has related methods
[05:47] they are more useful in the scenarios of looping logic that you are trying to build.
[05:52] With the help of Scanner object, I'll show you a demo about these has related methods in the next
[05:58] lecture.
[05:59] For now, I'm assuming you are clear about the next related methods.
[06:03] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
