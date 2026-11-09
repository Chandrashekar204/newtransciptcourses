# 23.12 — [JAVA 8] The of() methods in java.time Date and Time API

> Section 23: Date and Time in Java

[00:00] As of now, we are trying to use the now() method, which are available inside the new Date-Time API to
[00:08] create the objects that are capable of holding current date and time values.
[00:13] But apart from creating the objects of current date and time, sometimes we may have requirements to
[00:19] create the date and time objects with a specific date and time values.
[00:23] So let's try to understand how to achieve the same
[00:26] with the help of new Date-Time API.
[00:29] I'm going to create a new Java class inside the new API package.
[00:34] The class name I'm going to mention as OfMethodsDemo, because with the help of OfMethods only,
[00:41] we are going to create the date and time objects with the specific values. Inside this class
[00:46] first, let me try to create the main() method post that
[00:50] first, I'm going to create a LocalDate object with the variable name as date, followed by
[00:55] I'm going to type LocalDate again here this time instead of now, I'm going to invoke the of() method.
[01:02] You can see there are two overloaded of() methods.
[01:05] Using these of() methods, we should be able to create a date object with a specific year, month and
[01:12] day of the month.
[01:13] For example, I'm going to pass the year as 2015, followed by month as March, followed by date as
[01:22] 18.
[01:22] So with this now my LocalDate object, it is going to hold the March 18 to 2, 2015 as the date.
[01:30] We also have other overloaded method here
[01:33] instead of passing the month in an int value, we can also pass the month using an enum.
[01:40] So this is the second overloaded method.
[01:42] You can see it is accepting a month with the help of a Month enum.
[01:46] So inside this we have various enum constants like January, February, March.
[01:51] So what I can do here is, instead of these three integer number, I can simply first invoke the month
[01:58] enum present inside the java.time package, followed by
[02:02] I can invoke the constant MARCH, so this also perfectly fine.
[02:05] I hope you are seeing the beauty of new Date-Time API.
[02:09] We don't have to worry about the drawbacks that we have with the java.util.Date.
[02:13] Like in the case of java.util.Date, we need to mention the year by performing the addition from the
[02:18] base year, which is 1900 and even for the months
[02:21] also, we need to subtract the month value by one because inside the legacy Date-Time API, the months
[02:27] they are going to start at the index zero.
[02:29] In the similar lines, let me try to create that Time object as well.
[02:33] So I'll try to give the variable name as time, and this time, with the help of LocalTime, I'm going
[02:40] to invoke the of() method.
[02:41] So while you're trying to create the LocalTime, you have an option to pass only hour and minute.
[02:47] Similarly, you also have an option to pass hour, minute, and second.
[02:51] If you are also interested to pass the nanoseconds as well, you can use the third of() overloaded method
[02:58] using which you can pass hour, minute second, and nano of second.
[03:03] One of the great advantages of new Date-Time APIs is they are going to support the time up to nanosecond,
[03:10] whereas the legacy Date-Time APIs, they are going to support time up to a millisecond only.
[03:15] For now, let me use the first of() method using which I can pass what is the hour and minute?
[03:22] So I'm just typing 14 followed by 30.
[03:25] So with this I'm trying to create the time with the 2:30 p.m..
[03:30] In the similar lines, we should be also able to create the object of LocalDateTime by using the of()
[03:36] method available inside this LocalDateTime class.
[03:39] So let me give the variable name as dateTime, followed by
[03:42] I'm going to invoke the class which is LocalDateTime.
[03:45] And after this I'm going to invoke the of() method.
[03:48] So there are good amount of of() methods which you can use based upon your requirements.
[03:52] If needed
[03:52] you can also use this very first of() method, which is going to accept the object of LocalDate and
[03:58] LocalTime.
[03:58] By combining both of them, it is going to give you a LocalDateTime object.
[04:03] For now, let me try to use the of() method which only accept year, month, day of the month, hour
[04:11] and minute.
[04:11] So to this method I'm going to mention the year as 2015, followed by three, which indicates march
[04:17] followed by 18, followed by 14 hour followed by 30 minutes.
[04:22] Next, let me show you how to create the object of ZonedDateTime with the help of of() method.
[04:29] So whenever you want to create that ZonedDateTime object, first you need to provide the information
[04:34] about the time zone which you want to consider for the same
[04:37] first I need to create the object of zoneId so this zoneId is present inside the package java.time
[04:43] time, followed by
[04:45] let me give the variable name as newYorkTimeZone.
[04:48] So this is the variable name on the right hand side I'm going to use the same class which is zoneId.
[04:54] Inside this ZoneId class we have a of() method which is going to accept that
[04:59] ZoneId in a String format.
[05:00] So let me mention the zone ID details in a String format.
[05:05] So here I'm going to type America/ New_York.
[05:10] So this is a zone ID.
[05:11] Later on by passing this zone ID object I should be able to create the ZoneDateTime object.
[05:17] So let me show you how to do that
[05:18] first let me type ZonedDateTime followed by
[05:22] let me give the variable name as ZonedDateTime, and on the right hand side I'm going to type
[05:27] ZonedDateTime again.
[05:28] And inside this class also we have of() methods which you can use based upon your requirements.
[05:33] If you want you can pass LocalDateTime, object and zone ID, or you can pass objects of LocalDate,
[05:39] LocalTime and zone ID or if you want to manually pass the values, you can use these third of() method.
[05:45] So let me use the same.
[05:46] So first I'm going to mention all these details like 2015 March 18th, 14, 30.
[05:53] As a time and at last I'm going to mention the New York Time Zone as an input.
[05:59] But since we are getting an error, let's see what why we are getting this error.
[06:04] So if you see the of() method which is present inside the ZonedDateTime, it is also expecting the minute
[06:11] and second and nanosecond.
[06:12] So what we can do is we can try to pass the seconds as zero followed by nanoseconds.
[06:19] Also I'm trying to mention zero.
[06:21] So with this now compilation is resolved and we are able to create the object of ZonedDateTime.
[06:26] So as a next step, let me try to print out all these objects with the help of System.out.println().
[06:32] First I'm trying to print out date, followed by
[06:35] I'm trying to print out the Time object, followed by I'm going to print DateTime object.
[06:41] And at last I'm going to print out ZonedDateTime object.
[06:45] So if I execute this program you will be able to see first this is the date, this is the time and this
[06:51] is the Date and Time.
[06:52] And this is the ZonedDateTime.
[06:54] You can see this also having the time zone information like this time is belongs to the so and so time
[07:01] zone.
[07:01] So what is the time zone that we have provided.
[07:03] We have provided America New York as a time zone.
[07:06] The same is being considered here.
[07:08] So apart from simple off() methods there are other of() related methods as well inside each of the class.
[07:15] For example, with the help of LocalDate.
[07:18] If I type off, you can see there are other methods like ofInstant(), ofEpochDay() and ofYearDay().
[07:25] So we can use these based upon our requirements.
[07:28] For example, if you try to open the ofEpochDay() documentation, you will be able to see the purpose
[07:34] of this.
[07:35] So if you try to read these, it says obtains an instance of LocalDate from the epoch date count.
[07:42] We know the very first epoch day inside Java is 1970 Jan first.
[07:48] So if you try to pass some days as an input to this method, it is going to add the number of days to
[07:55] this initial Epoch day.
[07:57] So let me show you a demo around this.
[07:58] So what I'm going to do is I'm going to pass 1000 as an input to this method.
[08:03] So this is going to give 1000 days from the initial epoch day which is 1970 /01/01.
[08:10] So on the left hand side, let me create the object of LocalDate to catch the output from the ofEpoch()
[08:17] method.
[08:18] Similarly, let me try to invoke other off related methods after typing LocalDate class name, I'm
[08:24] going to type off, and this time let's try to see what is the purpose of this ofYearDay().
[08:31] So I can open this method to read the documentation.
[08:33] It is saying obtains an instance of a LocalDate from a year and the day of a year.
[08:39] So it is going to return a LocalDate with a specified year and day of the year for the year.
[08:43] Otherwise an exception will be thrown.
[08:45] So the minimum value that we can pass to this method is one followed by the maximum value we can pass
[08:51] is 366 days.
[08:52] So what this documentation is conveying is using this method you can pass an year and the day of the
[08:58] year.
[08:58] If you pass the day of the year as 100, it is going to give you the hundredth day inside a specific
[09:06] year.
[09:06] So let's see the demo of this method.
[09:08] So what I'm going to do here is, I'm going to type the year as 2000, followed by day as 100.
[09:13] With this I'm trying to look for a 100th day inside the year 2000.
[09:18] So let's try to catch the output on the left hand side with the variable name as day in 2000.
[09:24] So with this, if you try to print out, these objects will be able to see the output and validate if
[09:31] they are working based upon our discussion or not.
[09:34] So let me execute this program, and you can see if I try to add 1000 days to the initial epoch day,
[09:40] I'm going to get this date.
[09:42] Similarly, inside the 2000 year, April 9th is the 100th day.
[09:47] So let's see what is going to happen if we give the year as 2001.
[09:51] Because 2001 is not a leap year in this scenario, you can see the April 10th became the 100th day.
[09:58] So behind the scenes
[09:59] it is also considering the leap year logic, how beautiful it is.
[10:02] A lot of complexities.
[10:04] They are taken away from the developer this way based upon your requirements, you can always look for
[10:10] the of() related methods to create the date and time objects based upon a given value.
[10:16] I can't explore all the methods because there are more than 100 of() related methods inside each of the
[10:22] classes, but with my teaching, I'm making you ready on how to read the method documentation and how
[10:29] to understand the need of a specific method.
[10:31] I hope you are clear about the discussion around the of() methods present inside the new date time API.
[10:37] Everything that we have discussed inside this lecture I have mentioned in this slide for your reference
[10:43] along with the code snippets.
[10:45] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
