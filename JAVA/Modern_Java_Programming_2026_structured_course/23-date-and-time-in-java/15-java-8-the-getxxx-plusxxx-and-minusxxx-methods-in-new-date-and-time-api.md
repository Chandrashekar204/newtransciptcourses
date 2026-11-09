# 23.15 — [JAVA 8} The getXxx(), plusXxx() and minusXxx() methods in new Date & Time API

> Section 23: Date and Time in Java

[00:00] Inside this lecture I'm going to show you the demo of get related methods plus and minus related methods.
[00:07] To show you the demo
[00:08] first, let me try to create a new Java class with the name GetPlusMinusMethodsDemo.
[00:17] So this is the class name. Inside this class
[00:19] as usual, we need to create the main() method followed by
[00:22] I'm going to create a object of LocalDate with the help of of() method.
[00:28] So let me type LocalDate.of() and to this I'm going to pass the year as 2015 month as March, followed
[00:37] by day as 18.
[00:39] Now think like you have a specific requirement to read only the year detail or day detail or month detail.
[00:46] For these kind of scenarios, we have get related methods which you can invoke with the help of
[00:52] LocalDate object that we have created.
[00:53] So using the variable of localDate, if I try to type get, you'll be able to see that there are good
[01:00] amount of methods like getDayOfMonth(), getDayOfWeek ()and getDayOfYear(), getMonth(),
[01:07] getMonthValue(), getYear().
[01:08] So first let me try to invoke getYear() method on the left hand side and can catch the output with an
[01:15] int variable which is going to have the value of year, which is 2015.
[01:20] So we're going to get the output as 2015.
[01:22] Similarly, I'll be able to invoke month related methods with the help of getMonth().
[01:28] And there is also a getMonthValue() method.
[01:31] So if you invoke the getMonthValue() method, you're going to get the output in an into format,
[01:36] which is three.
[01:37] Whereas if you invoke the getMonth() method, you're going to get the output in an enum format.
[01:44] We know there is a enum with the name month.
[01:46] We are going to get the month name in the form of enum data type.
[01:51] So what is our output that we are going to get?
[01:53] We are going to get the march as the output.
[01:55] Similarly, if you are looking to fetch only that day, then you can invoke the getDayOfMonth().
[02:03] And with that you will get the output in an int format, which I can catch with the variable as day.
[02:09] Next I'm going to invoke the getDayOfWeek(), which will tell me whether a given day is a Monday,
[02:16] Tuesday, Wednesday or Thursday, Friday, Saturday, Sunday. So I can get to know those details.
[02:21] So if you open this method, you can see we're going to get the output in an enum format.
[02:26] So day of week is an enum.
[02:28] It is going to have constants like Monday, Tuesday Wednesday Thursday Friday Saturday.
[02:33] So let me catch the output on the left hand side.
[02:36] With the help of dayOfWeek() and with the variable name as dayOfWeek.
[02:41] So if I execute this program by keeping a breakpoint at line number 14, you'll be able to see all the
[02:47] constants like year has 2015, month has March and day has 18.
[02:53] And if I move my breakpoint to the next line, you'll be able to see the day of the week as well, which
[02:58] is Wednesday.
[02:59] Let me show you how to invoke these
[03:01] get related methods using LocalDateTime as well.
[03:04] Regardless of which class you are using, all these classes they support get related methods.
[03:09] For example here
[03:11] this time I'll try to create the object of LocalDateTime with the variable name as LocalDateTime,
[03:16] and I'm going to get the current date and time in my time zone by invoking the now() method.
[03:23] So using these object of LocalDateTime I can invoke get related methods.
[03:28] And you can see I have so many methods.
[03:31] For example, if I'm trying to get what is the current hour, I can simply invoke these, getOur() method
[03:38] and on the left hand side I can catch the output with the help of this variable r.
[03:43] So if I try to run this program and debug the program at the end, you'll be able to see that right
[03:50] now the hour is 15.
[03:52] So this is the purpose of Get related methods.
[03:54] You can always use them to extract a specific information that you are interested.
[04:00] Maybe you may have a requirement inside your real project that a particular logic should not be executed
[04:06] on a weekend like Saturday and Sunday.
[04:08] In those kind of scenarios, you can always use these getDayOfWeek to identify which day the
[04:14] program is running
[04:15] accordingly, you can execute your business logic.
[04:18] Let me show you the plus and minus related methods, which is going to help us to perform addition and
[04:25] subtraction on top of that date and time values.
[04:28] To invoke the plus and minus related methods, I'm going to use the same object of LocalDate that we
[04:33] have created.
[04:33] So at the end I'm going to first type LocalDate, followed by I'm going to type a plus.
[04:40] So with the help of plus you can see we can add the days, months, weeks and years to the current
[04:47] LocalDate object.
[04:47] For example, if I want to add six days, I can simply pass six as an input to the plusDays() method,
[04:54] and on the left hand side I can type LocalDate with the variable name ld1.
[04:59] So
[05:00] now these ld1 variable will have the date as six days to the future of this date that we
[05:07] have created. Which means we are going to have the output as
[05:11] 2015 - 03 - 24
[05:12] .
[05:14] Similarly, we can also add months as well
[05:16] with the help of plusMonths().
[05:19] This code is going to add six months to this date.
[05:22] And with that we are going to get the output as 2015 September 18th.
[05:28] This time let me try to add weeks.
[05:31] So here I am going to invoke the method which is plusWeeks().
[05:35] And to this if I pass two I am going to get the output as 20 15th April zero one as an output.
[05:43] So let me rename this variable name to ld3.
[05:46] Just like how we are trying to perform the addition operation.
[05:49] With the help of this plus related methods, we can also perform the subtraction as well with with the
[05:54] help of minus methods.
[05:56] So let me invoke one of the minus method.
[05:59] So what I am going to do is I'm going to invoke the minusMonths() method to this minusMonths() method.
[06:04] I'm going to pass the input as nine.
[06:07] And with that we're going to get the output as
[06:11] 2014 - 06 - 08
[06:14] .
[06:15] Because whenever we use minus we are going to travel into the past on the left hand side
[06:20] let me try to catch the output with the help of LocalDate ld4.
[06:24] I can also subtract years as well with the help of minusYears() method to this minusYears() method
[06:32] I'm going to pass the input as seven.
[06:34] And with that we are going to get the output as 2008 March 18th as an output, which we are going to
[06:42] catch with the help of ld5 variable. I can try to print out all these LocalDateTime objects that
[06:49] I have created with the help of plus and minus methods.
[06:52] So let me first print out ld1, followed by I'm going to print out ld two, ld3 ld4 and ld5.
[07:01] So if I execute this program by removing this breakpoint, you'll be able to see the output.
[07:06] So based upon our discussion, the output is matching with the values that we are expecting.
[07:11] I hope you are clear.
[07:12] So always whenever you are trying to travel into the future, please use the plus method or
[07:18] if you want to go to your past and correct some mistakes, you can always use minus related methods.
[07:25] Unfortunately, we don't have these kind of options in real life.
[07:29] We can't travel to future and we can't travel back to the past.
[07:32] But at least we can do this inside the Java programming language with the help of plus and minus related
[07:38] methods.
[07:39] I hope you are clear about the methods that we have discussed inside this lecture.
[07:43] Please refer to this slide for any questions.
[07:45] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
