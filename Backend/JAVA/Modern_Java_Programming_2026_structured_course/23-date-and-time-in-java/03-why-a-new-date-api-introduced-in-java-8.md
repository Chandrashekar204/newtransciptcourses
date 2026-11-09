# 23.3 — Why a new Date API introduced in Java 8

> Section 23: Date and Time in Java

[00:00] Based upon our previous lectures discussion, you may have $1 million question, which is why a new
[00:06] date API introduced in java 8, when we already have enough classes and interfaces to store date
[00:13] and time values before Java 8.
[00:15] So let's try to answer the same inside this lecture.
[00:17] Like I said before, the new DateTime API was introduced in Java 8 to address lot many drawbacks,
[00:25] limitations and design flaws of old date time API.
[00:29] The very first drawback is the legacy date API are the old date API
[00:34] it has some design flaws.
[00:35] This design flaws including ambiguity in representing date and time value.
[00:40] For example, if I try to create an object of date with the help of this code, like you can see with
[00:47] the help of these date constructor and new operator, I'm simply trying to create an object of date
[00:53] once this object is created.
[00:55] If I try to understand what value present inside this date object, it is going to have both the date
[01:01] and the time value.
[01:02] So these are very first confusion that developers may have.
[01:05] I'm trying to create an object of date which is supposed to store only date values, but why the hell
[01:11] it is also storing the time value?
[01:14] Not in all the scenarios
[01:15] you may need to store time.
[01:17] In some scenarios, you may want to ignore the time and simply store that date.
[01:21] But with the legacy Date API, we don't have any such option.
[01:25] We can't store date and time as a two separate objects.
[01:28] We should always create the date object, which is going to have both the date and time values.
[01:33] Let me show you a demo around this very quickly inside IntelliJ
[01:37] since we are into the new section, I have created a Java project with the name section_23.
[01:43] Inside this project, I'm going to create a new package with the name com.eazybytes.legacy.
[01:50] So inside this I'm going to create all legacy date API related examples and demos inside this package.
[01:57] Let me try to create a new Java class with the name LegacyDateAPIDemo.
[02:05] Here inside this class
[02:06] first let me try to create a main() method followed by
[02:09] I'm simply going to create a date object like you can see here
[02:12] I'm trying to leverage the default constructor of date along with the new operator.
[02:17] Here, my compiler has a confusion to which date it has to import.
[02:22] So there are two types of dates.
[02:24] One is from the java.util package, the other one is from the java.sql package.
[02:29] In this demo I want to use a java.util.date at later point of time, I'm going to explain you what is
[02:36] the difference between these two dates.
[02:37] For now, let's focus on date class present inside the java.util package.
[02:42] So if I try to print out these date object, you'll be able to see the date and time value based upon
[02:48] when these object is created.
[02:50] So if I try to execute this program, you'll be able to see the date as
[02:54] Friday, February 9th, 11:45 a.m. 36 seconds IST means Indian Standard Time and the year is 2024.
[03:03] So based upon when I'm trying to create this object, the current date and time value it is going to
[03:09] store inside it.
[03:10] Do you see here I don't have any intentions to store time, I just wanted to store only date, but I'm
[03:16] forced to store that time value as well.
[03:19] So these are one of the design flaw that these date class has.
[03:23] Let's try to understand what more design flaws we have under the Legacy Date API.
[03:27] With the Legacy Date API, the year always going to start from 1900, whereas the months they are going
[03:35] to start at index zero.
[03:36] Suppose if you want to represent a date of 26th September 2100, you need to create an instance of date
[03:44] using the code below like you can see here to the Date constructor we need to pass what is the year?
[03:51] So here I'm trying to send 200.
[03:54] Because if I want 2100 year as an year inside my Date object, I need to add 200 value to these 1900
[04:02] because inside the legacy date time API, like we discussed, the date is always going to start from
[04:07] 1900.
[04:08] So that's why I'm trying to mention 200 here.
[04:10] And since we are trying to represent September, we should mention here eight but not nine.
[04:16] The reason is the month is going to start at index zero in this legacy date API.
[04:21] And coming to the date you can mention 26.
[04:23] As usual, once this object is created, you will be able to see the output inside this Date object.
[04:30] It is going to look like this.
[04:31] You can see right now the time is being represented with all zero values.
[04:36] That means whenever we are not trying to pass the time values to the constructor of the Date class,
[04:41] they are going to be considered as a midnight time are with the zero values like you can see here.
[04:47] This is representing September 26th midnight time
[04:51] here also, I'm getting forced to store the time value even though I'm not interested.
[04:55] So let's see the demo of this code as well.
[04:57] This time what I'm going to do is, I'm going to create a
[05:00] object with the name date1, and on the right hand side, I'll try to use the constructor of Date,
[05:07] and to this constructor I'm going to mention 200, followed by 26 post that I can try to print out the
[05:14] same date one like you can see here
[05:16] this time I'm going to get the output, which is Sunday, September 26th, midnight time IST 2100.
[05:24] Since right now I'm executing this program from an Indian standard time and getting this default output
[05:30] based upon from which time zone you are trying to execute accordingly, you're going to get your time
[05:36] zone in the output.
[05:37] So this is the second design flaw that we have with the Legacy Date API.
[05:41] With all these design flaws inside the date class of java.util package Java team, they try to address
[05:47] few of them by introducing new classes, new methods, and deprecating some older ones.
[05:53] In fact, they also introduce another class with the name java.util.Calendar.
[05:59] They tried to overcome all the design flaws of date with the help of Calendar class, but this Calendar
[06:06] also has its own design flaws.
[06:08] In fact, these introduce more problems because the developers they are getting confused a lot whether
[06:14] they should use the date or whether they should use a Calendar.
[06:17] What's the difference between them?
[06:18] So instead of solving the problem, it created more confusion to the developers.
[06:23] Apart from these design flaws, there are good amount of drawbacks with the legacy date time API.
[06:28] The very first one is around the immutability and the thread safety.
[06:32] So whatever date related object that you are going to create with the help of legacy date APIs like
[06:38] java.util.Date or Calendar classes, they are all going to be mutable objects, which means their content
[06:45] or their state can be changed after creation.
[06:48] This mutability nature could lead to synchronization issues, especially when you are trying to execute
[06:54] your program in a multithreading environment.
[06:57] Whereas the new date time API under the package java.time.
[07:01] So all the classes under these new date time API, they are immutable, making them thread safe by design.
[07:09] You can happily use the new date time APIs inside the multithreading environment without worrying about
[07:16] the synchronization issues.
[07:18] We are ready to discuss about what are threads and multithreading as of now
[07:21] don't worry, this is going to make sense to you once we start discussing around the multithreading
[07:26] in the coming sections.
[07:27] The next drawback is around the limited date and time precision.
[07:31] With the Legacy Date API, we can only represent a time up to milliseconds, but there will be few industries
[07:38] where they expect the time precision up to nanoseconds.
[07:42] So these nanosecond precision is not supported by the legacy date API.
[07:47] Whereas inside the new date API there is a class with the name instance under the package java.time.
[07:53] It is going to support the nanosecond precision.
[07:56] We are going to see the demo about these instance in the coming lectures.
[08:00] The next drawback is around the inadequate time zone handling.
[08:04] We know we are all living in different different countries across the world.
[08:08] Every country will have their own time zone.
[08:10] For example, in India we follow the time zone with the name East Indian Standard Time.
[08:15] Similarly, USA has lot many time zones like EST, CST.
[08:21] So based upon the country where you are going to live, the time may vary
[08:25] not all of us is going to have the morning at the same time.
[08:29] So all these time zones, they are not handled properly in the legacy date API.
[08:35] On top of time zones, we also have a concept of daylight saving time.
[08:39] Few countries like USA, Canada, UK they're all going to follow daylight saving time.
[08:45] So what they are going to do as part of this daylight saving time is they are going to adjust their
[08:50] clocks by advancing it by one hour during summer time or winter time, based upon their requirements.
[08:57] These daylight saving time concept also is not handled properly inside the Legacy Date API.
[09:04] So all these challenges around the time zone and daylight saving they are addressed well inside the
[09:10] new date API, we are going to discuss about time zones and Daylight saving time support by new date
[09:16] API in the coming lectures.
[09:17] More details to follow.
[09:19] And at last the drawback is around the formatting and parsing dates and times different countries.
[09:24] They are going to follow different date formats and the time format.
[09:29] Few countries they follow 24 hour clock, whereas few countries they are going to follow 12 hour clock
[09:34] with the Am and PM, and few countries they are going to follow the date in an
[09:40] MMDDYY.
[09:41] Whereas few other countries are going to follow the date format in DDMMYY?
[09:47] With these kind of scenarios existing in the real world, sometimes you may want to convert your date
[09:52] into some other format, or you may want to pass your date which is present inside the String value
[09:59] as
[09:59] as an Date object.
[10:01] So to perform all these conversions, the legacy date time API, though it supports this formatting
[10:07] and parsing with the help of simple Date format class, but it is more of error prone or verbose or
[10:14] complex to understand.
[10:15] This problem also addressed well with the help of a class DateTime formatter.
[10:20] We are going to discuss about this in the coming lectures.
[10:23] In summary, we can say the Java Date time package in Java 8 was introduced to address the shortcomings
[10:30] or drawbacks of the older date and time classes.
[10:34] I hope you are clear on why a new date API introduced in Java 8.
[10:38] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
