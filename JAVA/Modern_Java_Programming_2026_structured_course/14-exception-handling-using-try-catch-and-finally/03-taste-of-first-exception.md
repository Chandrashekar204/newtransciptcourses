# 14.3 — Taste of first Exception

> Section 14: Exception handling using try, catch and finally

[00:00] Inside this lecture, I can show you some Java programs where you might be thinking there is no problem
[00:06] and you may never face any issues with those programs, but at run time they are going to throw some
[00:12] exceptions due to some invalid data provided to them.
[00:16] Once we are clear about what is an exception and how they will be throwed at runtime, then we can focus
[00:22] on learning on how to make our Java programs to handle exceptions gracefully in any kind of situations.
[00:30] Since we are into the section14, I have created a Java project with the name section_14.
[00:36] Inside this Java project only, I am going to develop all the examples that we are going to discuss
[00:41] throughout this section.
[00:42] You can find the same inside the GitHub repo as well.
[00:46] As of now you can see the source folder is an empty folder.
[00:50] First I'm going to create an package which is com.eazybytes.exception.
[00:57] So this is the package name.
[00:58] And inside this package I'm going to create a Java class which is ExceptionDemo inside this class
[01:06] first as usual we need to create the main() method inside this main() method using the Scanner object.
[01:13] I'm going to ask my end user to enter a number so that I can display the same onto the console.
[01:20] So to the Scanner constructor we need to mention System.in.
[01:25] Since we are asking the end user to enter his input using the keyboard was that I am going to mention
[01:32] the System.out.println(), which is enter a number I know
[01:36] previously I said not to use System.out.println() inside your Java programs, but since right
[01:42] now we are trying to learn the Java programs, this should be fine.
[01:46] But in real projects always please make sure you are using the logger statements.
[01:51] So wherever possible I'm going to use the logger statement.
[01:54] But sometimes if we are in a rush or if you want to quickly see a demo of a topic, there is no harm
[01:59] using the System.out.println().
[02:02] After this statement, I'm going to write the code which is int number is equal to Scanner.nextInt()
[02:10] .
[02:10] Since I'm asking an number as an input data from an end user, I'm using this next int method available
[02:18] inside the Scanner object.
[02:20] The same I'm going to print with the help of System.out.println().
[02:25] And at last I need to make sure I'm closing the Scanner with the help of close() method.
[02:30] So now let me execute this program.
[02:33] You can see it is going to ask me to enter a number.
[02:36] I am a good person, which you already know.
[02:39] So here I'm going to enter a good data.
[02:43] So I'll just type three and press enter
[02:46] and you can see we are getting the same as an output
[02:49] and with this our program is working perfectly
[02:52] there is no issue inside the program.
[02:54] You might be under the assumption that there are no issues in our program, and it is working without
[02:59] any issues.
[03:00] So this always applicable for a happy scenario.
[03:03] We as a good humans, we always think about good things.
[03:06] We never think about bad things or bad people, but sometimes we never know where our program is going
[03:13] to be executed.
[03:15] It might be executed by a bad person as well.
[03:18] In such scenarios, let's see how our program is going to behave.
[03:21] So I'm going to execute the program one more time, but this time I'm going to act as a bad person.
[03:27] I'm highlighting here, I'm going to act as a bad person.
[03:30] I'm not a bad person.
[03:31] In reality, I'm very, very good person.
[03:34] So jokes apart.
[03:35] So now I'll try to be as a bad person and I'm trying to enter the number by using its spelling.
[03:42] So I'm trying to enter three with the help of english word here.
[03:46] I may be a bad person, or I may be a confused person as well.
[03:50] I may not have enough clarity to enter a valid numerical value.
[03:54] I might be under the assumption three still is a valid input.
[03:58] So in this kind of scenarios, as soon as I press enter, you are going to get the RuntimeException.
[04:04] Inside Java
[04:05] anything that is going to fail your program to end abruptly.
[04:10] So such things we can call them as exceptions inside Java.
[04:14] So what is the exception that I'm getting here.
[04:16] So the exception name is InputMismatchException.
[04:20] So our program right now it is throwing this exception because while it is trying to convert these three
[04:26] inputs into a numerical value, obviously the libraries that we have used behind the scenes like Scanner.nextInt()
[04:32] they throw this exception.
[04:35] So this is our first official taste of RuntimeException inside Java.
[04:41] You will not be able to see these exceptions while you are trying to compile your program, or while
[04:46] you are trying to develop your program.
[04:48] Because as a developer, you may think everything is looking fine.
[04:52] There are no issues.
[04:53] But like I said, at runtime anything may happen due to some invalid data are due to some unexpected
[04:59] behavior.
[05:00] Let me show you one more example as well, so that it is going to be super clear for you.
[05:04] This time I'm going to create a one more Java class, and the class name I'm going to mention as
[05:12] ArrayIndexOutOfBoundsExceptionDemo.
[05:17] So I'm going to show you what is going to happen whenever we try to access an index inside an array,
[05:23] which is not available at runtime for the same, first I'm going to create a main() method.
[05:28] Inside the main() method, I'm going to create an int array with the name numbers, and inside these numbers
[05:35] array I'm going to store some numbers.
[05:38] Maybe I'll store five numbers like 1, 2, 3, 4, 5.
[05:43] With this, we know the total size or length of this array is going to be five, and the first number
[05:48] is going to be available at the index zero followed by 1, 2, 3, 4.
[05:53] So the max index number that we can use to access an element inside this array is four.
[05:59] But let's see what is going to happen if we try to access an index which is not present inside this
[06:05] array.
[06:05] So I'll simply write System.out.println() numbers.
[06:09] And after this numbers array variable I'm going to mention the square brackets.
[06:13] And inside this I'm going to mention an index number which is not available inside my array input data.
[06:20] So during the development or during the compilation, my Java is not going to look into the details
[06:26] about the data that I store inside my array.
[06:29] So it is not going to give any warning to me, because all these data will be stored inside an array
[06:36] object during the runtime only.
[06:38] So that's why during the compilation we're not going to get any error, but at runtime we will get some
[06:44] surprises which we are going to see in few seconds.
[06:47] So now I'm going to execute this program and you can see I am getting an exception which is
[06:55] ArrayOutOfBoundsException because I'm trying to access an index file which is out of bounds for the length
[07:03] of five.
[07:03] So if the length of the array itself is five, then how can I access the index file?
[07:08] We all know the max index value that we can access inside an array is length -1.
[07:15] So five minus one which is four.
[07:17] So the max index for this array is four.
[07:19] But we are trying to be dumb here or
[07:21] we are trying to be a bad person here.
[07:24] That's why we are trying to access index five due to which the program is throwing RuntimeException.
[07:30] Hey buddy, you asked me to access the index five element inside the array, but I don't see any element
[07:36] at index five, so that's why I'm throwing an runtime exception.
[07:40] Each exception has its own name, like here we have a name which is ArrayIndexOutOfBoundsException.
[07:47] Whereas the other exception that we have seen in the exception demo program, the exception name is
[07:53] going to be like you can see InputMismatchException.
[07:57] So based upon the scenario the exception name also may change in some scenarios.
[08:03] But behind the scenes all these exceptions they have a same parent class.
[08:08] We are going to discuss more about exceptional inheritance hierarchy in the coming lectures.
[08:13] But for now I'm assuming you are clear about what is an exception.
[08:17] The immediate $1 million question that you may have here is I understand what are the exceptions.
[08:23] I understand under which scenarios the exception may happen, but I'm clueless how to handle these,
[08:29] or how to make my program to gracefully shut down whenever these kind of exceptions are happening.
[08:36] So right now, what is happening inside our program is whenever an exception happens at this line of
[08:41] code, the next lines of code, they are not going to be executed.
[08:44] The same applicable here.
[08:46] If you try to write some other program after this line number seven, they are not going to be executed.
[08:52] This means your program right now it is getting shut down all of a sudden without worrying about the
[08:59] next set of lines.
[09:01] So we have to overcome these kind of situations.
[09:04] So let's try to understand how to implement exception handling inside Java from the next lecture.
[09:10] Thank you
[09:10] bye.

----------------------------------------
