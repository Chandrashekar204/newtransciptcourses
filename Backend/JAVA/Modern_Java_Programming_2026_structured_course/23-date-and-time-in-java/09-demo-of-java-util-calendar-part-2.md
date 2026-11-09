# 23.9 — Demo of java.util.Calendar - Part 2

> Section 23: Date and Time in Java

[00:00] Let's try to understand how to perform the formatting of the Date
[00:04] whenever we are trying to use a Calendar, the process is going to be very similar to the java.util.Date
[00:11] approach.
[00:12] First, you need to create the GregorianCalendar object.
[00:15] Since we already have a GregorianCalendar object, I will directly go and create SimpleDateFormat
[00:21] object, or I can try to copy the same from DateFormattingDemo class.
[00:26] Here we have an Object of DateFormat.
[00:29] Let me copy these two lines and paste it inside the CalendarDemo class.
[00:33] At the end you can see I have a DateFormat object, and to this DateFormat object, what I can do
[00:40] is I can send the time details using my GregorianCalendar.
[00:44] So when I invoke the getTime() method using my GregorianCalendar object behind the scenes, it is going
[00:50] to give the Date object as an return type, and the same is going to be used to perform the formatting
[00:57] and the output.
[00:57] I am going to get in a String format.
[00:59] I can try to print out the same with the help of the System.out.println() by passing these formatted date
[01:05] as an input.
[01:06] So if I execute this program at the end, you will be able to see the date value in the format that
[01:12] we have built.
[01:13] With the help of this SimpleDateFormat.
[01:16] There is no change here compared to the date, because eventually we are converting these
[01:21] GregorianCalendar object into a Date object with the help of these getTime() method.
[01:26] Just like how we have these get and set related methods inside the Calendar, we also have add and subtract
[01:33] related methods, which is going to help us to add months or days or years or time to your Date object
[01:41] value.
[01:41] Let me show you a demo around that for the same
[01:43] what I am going to do is,using these GregorianCalendar object.
[01:47] I'm going to invoke the add() method to this add() method
[01:51] first, I'll try to mention what I'm trying to add,
[01:54] I will try to add hours.
[01:56] That's why I am going to invoke the constant Calendar.HOUR and post that I'm going to mention two,
[02:02] which means I want to add two hours to the time and date present inside these GregorianCalendar.
[02:09] We can validate if these two hours are added or not by simply copying these code and pasting here.
[02:17] This time I'll try to use the same variable name by just removing the String, which means we are trying
[02:22] to overwrite the value here at the line number 39.
[02:25] So if I execute this program, you can see the last line has a date with the two hours more compared
[02:33] to the previous date.
[02:34] This is because we have added two hours compared to the previous date and time value.
[02:40] Similarly, we can also use the subtract and to the subtract method()
[02:43] also, we can pass any kind of constant indicating year, month, date, hour, and after the constant.
[02:50] We can also mention a numerical value to perform the subtraction.
[02:53] Just like add, we can also perform the subtraction.
[02:56] But for the subtraction we don't have any other method with the name subtract
[03:00] Instead for the same add method, if you send a negative number that is going to perform the
[03:05] subtraction behind the scenes. Let me show you a demo as well.
[03:09] What I can do is I can try to copy this line of code.
[03:12] This time I'm going to use the constant month and I will mention the value here as minus three.
[03:20] So with that, I want to subtract three months from the Date present inside these GregorianCalendar
[03:27] object.
[03:27] So if I execute this program, you'll be able to see the output clearly.
[03:32] So first we have February.
[03:34] Later on you can see in the next date the date is moved back three months
[03:38] and the year also adjusted.
[03:40] So here we are not able to see the year properly.
[03:43] What we can do is in the SimpleDateFormat, we can mention four wise so that we'll be able to see
[03:48] the date values correctly.
[03:50] So first we used to have the year 2101.
[03:53] Later on it is reduced to 2100 because we tried to subtract three months
[03:58] and that's why it went to the November in the previous year.
[04:01] So this add() method is going to be super useful in the scenarios
[04:05] whenever you want to write a business logic, by adding or subtracting dates months or year or even
[04:12] minutes, hours, seconds as well.
[04:14] I can also give some example.
[04:16] Think like you have a business requirement to fetch the records from the database which are created
[04:21] from the last two weeks.
[04:23] So what are you going to do?
[04:24] First, you are going to create a Calendar object with the default constructor, which is going to give
[04:29] you the current date and time value.
[04:31] On top of that, you're going to invoke the add() method to subtract the 14 days from it.
[04:37] And with that, you're going to have two different objects using which you can try to fetch the records
[04:41] from the database.
[04:43] There is also an interesting method inside the Calendar classes to identify whether a given year is
[04:49] a leap year or not.
[04:51] Let me show you the same.
[04:52] To invoke the leap year related method, first, we need to mention the object of GregorianCalendar
[04:58] using the same we can
[04:59] invoke the isLeapYear() method, so isLeapYear() method is a instance method to which we can pass the.
[05:06] What is the year we want to perform to check whether a given year is a leap year or not, and accordingly,
[05:12] we are going to get the output as boolean. To this method
[05:14] let me pass a leap year as an input, which is 2048.
[05:19] We know 2048 is a leap year.
[05:21] Let's see what output we are going to get by invoking this code.
[05:25] So if I try to print out these isLeapYear onto the console, we should have a true as an output.
[05:32] Hurray!
[05:33] Next, I'll try to change this value to 2049, and this time we should get the output as false, which
[05:39] is obvious.
[05:40] Yes, it is working perfect.
[05:42] So this kind of utility methods, they are lot available inside the Calendar and the GregorianCalendar.
[05:48] You can check the list of methods available inside these classes by using IntelliJ and based upon your
[05:54] requirements, you can use any of these methods.
[05:57] I hope this makes sense to you.
[05:59] As a next step, I want to show you how to create that date and time based upon a specific time zone,
[06:06] with the help of java.util.Date and the calendar related classes.
[06:11] So let's try to understand the same in the next lecture.
[06:14] Thank you,
[06:15] bye.

----------------------------------------
