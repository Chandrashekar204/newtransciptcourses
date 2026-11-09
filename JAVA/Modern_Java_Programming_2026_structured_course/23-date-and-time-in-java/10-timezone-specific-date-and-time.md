# 23.10 — TimeZone specific Date and Time

> Section 23: Date and Time in Java

[00:01] As of now, in the examples that we have discussed so far around the date and time, the value of date
[00:06] and time is getting created based upon the default time zone where I am trying to execute my Java program.
[00:13] Since I am trying to execute my Java program from India, the time zone of India is getting considered
[00:19] in the date and time values that are getting created.
[00:22] But in real projects, we will have specific requirements to create the date and time based upon a different
[00:29] time zone.
[00:30] To handle those kind of scenarios, you need to understand how to create date and time based upon a
[00:35] given time zone.
[00:37] So what is a time zone throughout the world
[00:39] all the countries they are going to have different, different times.
[00:43] Not every country is going to have morning at the same time and night at the same time.
[00:48] So based upon how the earth is rotating, the time is going to vary from country to country to make
[00:54] our lives easy long back
[00:55] these time zones are introduced in order to use these time zones.
[00:59] First you need to understand what are the time zones supported by these legacy date API.
[01:04] In order to show you the list of time zones supported by the Legacy Date API, I am going to write a
[01:10] small program with the Java class name as TimeZoneIDsList.
[01:16] So these are class name.
[01:18] Inside this class, I need to create the main() method post that using the class which is time zone.
[01:26] This class is present inside the java.util package.
[01:29] Inside this class we have a static method which is get available IDs.
[01:35] So I'm trying to invoke the same.
[01:36] So this is going to give all the available time zones in a String array format.
[01:41] That's why on the left hand side I need to catch the output with the help of String array and the variable
[01:47] name as timeZoneIds.
[01:50] Now this array content I'm going to display with the help of our age.
[01:55] So let me first create a temporary variable name which is String timeZoneId.
[02:01] And after the colon I'm going to mention timeZoneIds which is my array variable.
[02:06] Inside this for each loop, I'm going to print out each timeZoneId during each iteration.
[02:13] So if I execute this program, you'll be able to see there are lot many timeZones that are supported
[02:19] by Legacy Date API.
[02:21] So if you are looking for the time right now in the US eastern, you can use this time zone.
[02:28] Similarly US specific UTC Turkey time.
[02:32] So there are so many time zones available which you can use based upon the country that you are interested
[02:38] to get the time.
[02:39] I hope you are clear with this logic that I have written now
[02:42] using these time zone values, we can try to create a date and time by providing that time zone details.
[02:48] So first I'm going to show you how to create a time zone specific date and time with the help of java.util.Date.
[02:55] So let me create a class with the name TimeZoneDatesDemo.
[03:01] Inside this class I'm going to first create a main() method followed by
[03:04] first I need to create the object of SimpleDateFormat.
[03:08] What I can do is, instead of typing, I can copy some code from the CalendarDemo class.
[03:13] So let me copy these code and paste it inside the TimeZoneDatesDemo.
[03:19] So here you can see I just created an Object of DateFormat by providing a format detail post that using
[03:26] the same DateFormat object, I need to invoke the method setTimeZone().
[03:30] To this setTimeZone() method, we need to pass the object of TimeZone.
[03:34] So to create that TimeZone object, first we need to invoke that TimeZone class followed by
[03:40] we need to invoke the getTimeZone() method.
[03:42] And to this method I'm trying to pass a timeZone value, which is America/New_York.
[03:47] So these time zone is already available inside my list that I have printed here.
[03:52] You can see using this, I can try to get the what is a current date and time in the new year.
[03:59] Please make sure you are passing one of these values only to the getTimeZone() method.
[04:04] Otherwise things won't work like you expect.
[04:06] Now I have said that TimeZone details to my DateFormat object.
[04:10] Now using the same DateFormat object, I need to invoke the format() method, and to this format() method
[04:17] I need to pass the object of Date.
[04:20] So if I invoke new date here, it means I'm trying to pass the currentDate and time as an input to
[04:27] this format() method.
[04:28] So on the left hand side I can try to catch the output with the help of String variable with the name
[04:34] formattedDate.
[04:35] So let me try to print out these value present inside the formattedDate.
[04:40] So if I execute this program, I'll be able to see what is the time right now in New York.
[04:47] So right now the time is 7:39:35 seconds Am.
[04:51] I can also show you by mentioning some other TimeZone details here.
[04:56] So let me execute this program and pick randomly
[05:00] one of the time zone.
[05:01] Maybe this time I'll try to take some country
[05:05] maybe I'll take these Europe/Vatican.
[05:09] So let me mention the same here
[05:11] or maybe instead of replacing, what I can do is I'll try to copy this code one more time and paste
[05:18] it here and copy this Europe, Vatican in the place of America, New York.
[05:24] And with that I can remove this String.
[05:27] And that content of the formatted date is going to be overwritten.
[05:31] And now I'm trying to print formatted date again.
[05:35] So if I execute this program you'll be able to see right now in New York this is the time which is 7:45
[05:42] a.m., whereas in Vatican it is afternoon 13:41:06 seconds.
[05:48] So this way you can always get the date and time based upon a given time zone.
[05:54] So the process to get that time zone specific date and time with the help of Date object is very complex.
[06:01] First, you need to create the SimpleDateFormat object post that you need to set the time zone followed
[06:07] by
[06:07] you need to invoke the format() method by passing the current date time value.
[06:12] So these are very length approach.
[06:13] But if you try to use the GregorianCalendar approach, it is going to be super simple.
[06:19] You just have to first create the object of GregorianCalendar as usual with the help of default constructor.
[06:26] Once you have written this code to the constructor of GregorianCalendar, you can pass the time zone
[06:32] details by invoking the getTimeZone() method, and to these geTimeZone() method.
[06:38] You can pass the time zone details like you can see here.
[06:41] I'm trying to pass America/New_York, so whenever you have a requirement to create an object of
[06:47] TimeZone, you need to invoke the static method available inside the TimeZone class.
[06:51] To this getTimeZone(), you need to mention what is the time zone for which you are trying to get the
[06:56] Date and Time.
[06:56] So now, inside this GregorianCalendar, the current date and time of New York is going to be present.
[07:03] Did you see how simple it is to create that time zone specific date and time using GregorianCalendar?
[07:09] Now let me show you the demo on the date and time details created with the help of these GregorianCalendar.
[07:15] For the same, I'm going to open this CalendarDemo and copy all these lines of code and paste it inside
[07:21] these TimeZoneDatesDemo.
[07:23] So here I'm going to copy all this code.
[07:25] So using this object I'm trying to get the year month date, hour of the day, minute second and milliseconds
[07:32] and the same
[07:32] I'm trying to print out with the help of this printf() method.
[07:35] So if I execute this program you'll be able to see that right now in New York the time is 7:44:54 seconds
[07:44] and this is the milliseconds as well.
[07:46] So this is how you can get the time zone specific details with the help of GregorianCalendar.
[07:52] You may have a question here
[07:53] why did you read that data individually?
[07:56] By using these Get methods, why can't you directly use the getTime() method and use the same to print
[08:03] onto the console?
[08:04] Let's see the same as well.
[08:05] In the same process, I will also show you an issue around this.
[08:09] Think like I'm trying to get the Date object with the help of getTime() method available inside the
[08:16] GregorianCalendar.
[08:16] If I try to print out the same onto the console, surprisingly you will not see the New York time.
[08:22] You will see the highest time.
[08:24] That's because whenever this getTime() method is invoked behind the scenes, a new Date object is going
[08:30] to be created.
[08:31] And when this object is getting created, it is going to construct the default time zone where the program
[08:37] is running.
[08:38] In my scenario, it is highest if you want to get the same time zone like in the GregorianCalendar,
[08:44] then you need to follow all these steps like.
[08:46] First you need to create the SimpleDateFormat object pose that you need to set the time zone using
[08:50] the same DateFormat object.
[08:51] You need to invoke the format() method to the same
[08:54] you need to send you a Date object.
[08:56] Then only your Date object is going to have your desired time zone details.
[09:00] Otherwise it is going to carry the default time zone details.
[09:04] Whereas if you try to read the data individually, with the help of this get() method, you will be able
[09:10] to get the time based upon the time zone that you have provided to this GregorianCalendar() constructor.
[09:16] If you see on a high level with the introduction of Calendar related classes, certain limitations of
[09:22] date are resolved.
[09:23] Like we can directly pass the year, we can use the month constants.
[09:27] There are lot many utility methods and useful methods inside the Calendar, so to some extent the Java
[09:33] team, they try to resolve the issues with the java.util.Date class.
[09:37] But still, even with the Calendar
[09:39] also there are some design flaws like there is no way for us to store the date and time separately.
[09:45] On top of that, dealing with the time zones is also complex with the help of Date and Calendar.
[09:51] And in fact, this Calendar created more confusion to few developers.
[09:56] That's why many of the developers still they are using java.util.Date.
[10:00] So no worries
[10:01] we have new Date-Time API to our rescue.
[10:04] When we discuss about the new Date-Time API, you're going to see the beauty of the new API, how it
[10:11] is solving all these limitations and complexities.
[10:14] I hope you are clear with all the discussion that we have done around the Calendar so far.
[10:18] Whatever we discussed around the GregorianCalendar, I have mentioned in these two slides along with
[10:24] the example code.
[10:25] Please refer the same for any questions.
[10:27] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
