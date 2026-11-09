# 23.11 — [JAVA 8] Introduction to new Date & Time API from Java 8

> Section 23: Date and Time in Java

[00:00] I know you might have been scratching your head when this fellow is going to talk about the new Date-Time
[00:06] API.
[00:07] The waiting is finally over.
[00:09] From this lecture we are going to completely focus on new Date-Time API.
[00:14] Inside this lecture, let me give an high level overview and introduction to the new Date-Time API that
[00:21] is introduced as part of Java 8.
[00:24] With all the limitations that Legacy Date API used to have, most of the Java developers they started
[00:31] using lot many third party date and time libraries such as Joda time.
[00:36] So there is a third party API or library, which is developed by other open source developers with the
[00:42] name Joda Time.
[00:43] This Joda time library
[00:45] it has lot many features compared to the legacy date time API.
[00:49] To overcome all the challenges of legacy Date-Time API.
[00:52] Most of the developers they used to use these Joda time API, which is from third party.
[00:58] So with all these reasons, Java team finally decided to introduce a high quality date and time support
[01:05] within the Java library itself.
[01:07] As a result, as part of Java 8, a new date time API released under the package java.time inside
[01:15] java.time package and all its sub packages.
[01:19] There are many interfaces, classes, enums.
[01:22] We can't discuss all of them, but I'm going to discuss most commonly used or most important interfaces
[01:29] and classes and enums, which you may need on your day to day work.
[01:33] Like you can see here under that java.time package, we have these important classes with the name
[01:39] LocalDate,
[01:40] LocalDateTime,
[01:41] LocalTime,
[01:42] ZonedDateTime.
[01:42] OffsetDateTime.
[01:44] Instant,
[01:44] Duration, Period.
[01:46] Similarly, we also have enums with the name DayOfWeek and Month.
[01:50] We are going to discuss about all these classes.
[01:52] Then it is going to make sense to you. Under the java.time package
[01:56] we also have a sub package with the name temporal.
[01:59] Under this temporal package we have so many classes related to temporal with the name like Temporal,
[02:05] TemporalAccessor, TemporalAdjuster and TemporalQuery.
[02:09] And we also have enums like ChronoField and ChronoUnit coming to the formatting of date and time.
[02:15] In the legacy Date-Time API, we have a class with the name SimpleDateTimeFormat in the similar lines
[02:21] in the new Date Time API as well, we have a class with the name DateTimeFormatter, which is going
[02:27] to help us to format our Date and Time objects.
[02:30] This is present inside a sub package with the name java.time.format.
[02:34] So anytime if you see a class interface or enum under the package java.time or under its sub package,
[02:42] you can simply assume it belongs to the new Date-Time API.
[02:46] Let's start the discussion of new Date-Time API by trying to understand how to represent Date, Time
[02:53] and TimeZone details with the help of these new Date-Time API.
[02:57] Inside these new Date-Time API, we have a class with the name LocalDate, which is going to useful
[03:04] to strictly represent a Date.
[03:06] There won't be any time involved.
[03:08] If you are looking to store only date, you can simply use these LocalDate to create the Date object.
[03:15] After LocalDate, we have a LocalTime which is going to help us to represent only a time without a
[03:22] date value.
[03:23] Sometimes you may have a business requirement just to store time of a day without worrying about the
[03:29] dates.
[03:29] In all those kind of scenarios, you can create the object of LocalTime, but if you want a combination
[03:35] of both date and time, you have a class with the name LocalDateTime which is capable of storing the
[03:42] date time details but not the time zone.
[03:45] If you are worrying about the time zone as well, then you have an option in the form of
[03:51] ZonedDateTime.
[03:52] So with the help of ZonedDateTime class, we can create objects that are capable of storing Date, Time
[03:58] along with the TimeZone.
[03:59] So did you see the beauty here of the new date time API?
[04:02] You have a complete flexibility to choose from what you want.
[04:06] You are simply looking to store only time.
[04:08] Go for the LocalTime if you are looking for the date and time along with the time zone, go for the
[04:13] ZonedDateTime.
[04:14] And the naming convention of these classes also is selected very cleverly.
[04:19] So whenever someone is talking about LocalDate, LocalTime, LocalDateTime, they're trying to refer
[04:24] what is the time in your local area.
[04:26] But if someone is looking for the Date and Time based upon a zone or based upon a TimeZone, then they
[04:32] can safely use these ZonedDateTime.
[04:34] It also has the word zoned to convey the purpose of it.
[04:38] So if you try to visualize these four classes, this is how it is going to look like.
[04:42] We know each date and time.
[04:44] It is going to have three different parameters.
[04:47] What is the date, what is the time and what is the zone.
[04:50] So if you are only looking for the date, so go for the LocalDate or
[04:54] if you are looking only for the time, go for LocalTime.
[04:57] If you are looking for the combination of date and
[04:59] time, you can go for the LocalDateTime.
[05:02] Otherwise, if you are looking for the combination of date, time and zone, you need to use the
[05:08] ZonedDateTime, which is a combination of date time and ZoneId.
[05:12] I hope this is making sense to you with this clarity.
[05:15] You might be super happy, but you may have a question which is how to create the object of these classes.
[05:21] It's very easy.
[05:22] All these classes, they have a common method with the name now().
[05:25] So now() is a static method.
[05:27] Invoke this now() method.
[05:29] Using these classes you're going to get the current date or current time, or current date and time
[05:35] based upon what type of object you are trying to use.
[05:38] Again, this method naming convention also is very good
[05:42] usually now indicates what is a current time even for the developers to remember
[05:47] this method is very easy because it is very close to the functionality that it provides.
[05:52] I hope you are clear with these code snippets.
[05:54] Let's see the demo on how to create these objects by going into the IntelliJ. Inside my Intellige,
[06:00] let me close all the current opened classes.
[06:04] Now I'm going to create a new Java package with the name com.eazybytes.newapi.
[06:14] Inside this new API package, I'm going to create all the examples related to the new date time API
[06:20] that is introduced in Java 8.
[06:22] Under this package, let me create a very first class which is NewDateTimeApiDemo inside this class
[06:31] as usual
[06:32] first I'm going to create the main() method post that I'll show you how to create the objects of various
[06:38] classes that we have discussed so far.
[06:39] So first I'm going to create an object of LocalDate.
[06:43] This is present inside the package java.time.
[06:46] To this I'm going to mention the variable name as Date only and post that using the same class
[06:52] I need to invoke the static method.
[06:54] Now after this LocalDate.
[06:57] This time I'm going to create the object of LocalTime, which is going to have only time details.
[07:04] That's why I'm giving the variable name as time only.
[07:07] On the right hand side
[07:08] we need to invoke the LocalTime class followed by now() static method.
[07:12] After LocalTime, I'm going to invoke the LocalDateTime class with the variable name as dateTime,
[07:20] and on the right hand side I'll invoke the LocalDateTime class along with the static method now.
[07:26] And at last we can try to create the object of ZonedDateTime with the variable name as
[07:32] DtaeTimeWithZone() on the right hand side
[07:35] let me invoke the now() method with the help of
[07:38] ZonedDateTime.
[07:39] Do you see the consistency here,
[07:41] all the classes
[07:42] they have a same method now().
[07:43] As a next step, I'll try to print out all the objects like date only.
[07:49] I'll try to print out followed by
[07:51] I'll try to print out time only, followed by I'll try to print out dateTime.
[07:58] And at last I'll try to print out object with the name, dateTimeWithZone.
[08:04] So if I execute this program, you'll be able to see the currentDate.
[08:08] What is the current time?
[08:09] What is the current date and time?
[08:11] What is the current date and time along with the ZoneId?
[08:15] So as of now, this ZonedDateTime object, it is trying to create that time zone based upon the where
[08:21] the program is running.
[08:22] Since I'm running from India, it is considering my time zone.
[08:25] Later on in the coming lectures, I'll show you how to feed a different time zone to the object of
[08:31] ZonedDateTime class.
[08:32] So these are very first advantage provided by the new date time API compared to the legacy date time
[08:38] API.
[08:39] The advantage is you have various options to choose from based upon your requirements.
[08:45] If you are looking to store only time, use LocalTime or if you are looking only for date use
[08:51] LocalDate.
[08:51] If you are looking for date and time without worrying about the time zone, you can use LocalDateTime.
[08:57] Otherwise, if you are looking for date and time along with the time zone, go for the ZonedDateTime.
[09:02] I hope you're happy with this initial demo of the new Date-Time API, but this is just a tip of the
[09:08] iceberg.
[09:09] There are more and more features available inside the new Date-Time API.
[09:12] As we explore more and more about these in the coming lectures, you're going to fall in love with it.
[09:17] I'm not joking
[09:18] it's a serious statement.
[09:19] You're going to like it 100%.
[09:21] Thank you,
[09:22] and I'll catch you in the next lecture, bye.

----------------------------------------
