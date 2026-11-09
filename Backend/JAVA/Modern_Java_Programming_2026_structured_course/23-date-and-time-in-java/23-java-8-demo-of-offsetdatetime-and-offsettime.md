# 23.23 — [JAVA 8] Demo of OffsetDateTime and OffsetTime

> Section 23: Date and Time in Java

[00:00] Inside this lecture, let's talk about another class available inside the new Date-Time API which is
[00:06] OffsetDateTime.
[00:08] This is going to work very similar to the ZonedDateTime, but there is a clear difference between
[00:14] ZonedDateTime and the OffsetDateTime.
[00:16] You need to use ZonedDateTime whenever your business logic needs to handle all the time zone rules,
[00:24] daylight saving time changes, or geographical regions.
[00:27] In all such scenarios, you need to use the ZonedDateTime.
[00:31] But if you are simply looking for an option which is going to help you to build the date and time based
[00:36] upon the offset, ignoring all the daylight saving rules and geographical locations in such scenarios,
[00:42] you can happily use OffsetDateTime.
[00:45] Whenever you want to create the object of OffsetDateTime.
[00:48] You can only pass the ZoneOffset object, but not the ZoneId objects. You can see here
[00:54] at the end, I have an example where I'm trying to pass this offset object as an input to the now() method
[01:01] of OffsetDateTime.
[01:02] With that, I'm going to have a OffsetDateTime object, which is going to store the current time based
[01:08] upon the offset plus two.
[01:10] If you want to know what is the equivalent offset time by providing another ZoneOffset object, I can
[01:16] use the same OffsetDateTime object, and with the same I can invoke the withOffsetSameInstant()
[01:22] method, just like how we have withZoneSameInstant() method, we also have
[01:28] withOffsetSameInstant() method inside the OffsetDateTime.
[01:31] So to this method, if you pass the DestinationOffset as an input, you're going to get the equivalent
[01:36] offset time based upon the provided offset value.
[01:40] Let's see the demo of this offset date time inside IntelliJ.
[01:44] To show you the demo
[01:45] first, I'm going to create the new Java class with the name OffsetDateTimeDemo.
[01:52] Inside this class
[01:53] first I'm going to create the main() method, followed by
[01:56] I'm going to create the two objects of ZoneOffset.
[01:59] So let me open this ZonedDateTimeDemo.
[02:02] And here you can see I have these objects.
[02:04] So let me copy them and paste it inside the OffsetDateTimeDemo class.
[02:09] Now using these zoneOffset objects I should be able to create the objects of OffsetDateTime class.
[02:16] So how to create them?
[02:17] It's very simple.
[02:18] First you need to type OffsetDateTime followed by variable name as offsetDateTime and on the right
[02:24] hand side
[02:25] using the OffsetDateTime class.
[02:27] I need to invoke the now() method to this now() method, we can pass the ZoneOffset object.
[02:33] So this now() method it is going to accept the ZoneId object, but still we are able to pass the
[02:39] ZoneOffset object because behind the scenes if you see this ZoneOffset is a subclass of ZoneId.
[02:45] That's why we are able to pass the object of ZoneOffset to this now() method.
[02:50] Now using this object name, which is offsetDateTime, I invoke the withOffsetSameInstant() method.
[02:58] And to this method I'm going to pass DestinationOffset object as an input, and on the left hand
[03:05] side I am going to catch the output with the help of a variable which is destOffsetDateTime.
[03:13] For that
[03:13] I'll try to print out both these objects, which is OffsetDateTime followed by
[03:18] I'm also going to print this DestinationOffsetDateTime.
[03:22] If I execute this program, we'll be able to see the date and time values.
[03:26] So these are date and time value.
[03:28] You can see it has only offset details but not the time zone details.
[03:32] Similarly, in the next line you will be able to see the equivalent time based upon the offset that
[03:38] we have provided, which is UTC -8.
[03:41] I hope you're clear on how to create the objects of OffsetDateTime.
[03:45] Please use this class inside your business logic.
[03:48] If you are not worrying about the daylight saving rules and the time zone details. I can also show
[03:53] you a formula which conveys the relationship between the ZoneId and zoneOffset.
[03:58] Like you can see here, we can say ZoneId is equal to zone offset plus zone rules.
[04:04] So every time zone or every zone ID will have its own rules like daylight saving rules.
[04:10] Not every time zone is going to have daylight saving.
[04:13] Only few countries or few time zones only they are going to have daylight saving rules.
[04:18] So if you try to apply all those rules on top of the ZoneOffset, you are going to get the zone ID.
[04:24] I hope this makes sense to you, and the last class I want to discuss around the offset is offset time.
[04:30] So with the help of OffsetDateTime, we are able to represent a date and time values based upon a
[04:36] given offset.
[04:37] But if you have a requirement to simply represent a specific time of a day with a fixed offset from
[04:43] the UTC, then you can use the Offset class and try to create the objects of same.
[04:48] Here I have an example code on how to create the object of OffsetTime.
[04:53] So first I'm trying to create the OffsetTime object with the help of off method, and I'm trying
[04:59] to pass.
[04:59] number of hours,
[05:01] number of minutes.
[05:01] Number of seconds and number of nanoseconds after the nanosecond, you can pass the object of ZoneOffset.
[05:09] So here I'm trying to create the object of ZoneOffset directly within the parenthesis.
[05:14] So based upon these details that you have provided a OffsetTime object is going to be created with
[05:20] the UTC offset as zero two.
[05:23] Using this OffsetTimeObject we should be able to invoke many other methods like getHour(), getMinute(),
[05:29] getSecond(), and getOffset().
[05:31] If you are looking for a specific information like offset details, hour details, minute details,
[05:36] hour second details.
[05:37] We also have plus related methods which we can invoke with the help of these OffsetTime object.
[05:42] And similarly, we also have isBefore() method to identify whether a given offset time is before the
[05:49] other offset time.
[05:50] So let's try to see the demo of this class very quickly.
[05:53] I'm going to create a new class inside my project with the name OffsetTimeDemo.
[06:00] Inside this class,
[06:01] first, let me create the main() method post that I'm going to create the object of OffsetTime with the
[06:08] variable name as OffsetTime, and on the right hand side
[06:11] with the help of of() method, I'm going to pass what is the hour minute, second nanoseconds and the
[06:18] object of ZoneOffset or
[06:21] you also have an option where you can pass the object of LocalTime and along with the LocalTime object,
[06:27] you can pass a ZoneOffset object.
[06:29] With that you are going to get the object of OffsetTime.
[06:33] For now, let me invoke the second of() method and to this I'm going to send the input as 15, 30,
[06:40] 0, 0.
[06:43] And at last I'm going to pass the ZoneOffset object by invoking ZoneOffset class.
[06:48] And with this class I'm going to invoke the ofHours() method to this method I'm going to pass the input
[06:55] as two.
[06:55] Let's try to understand what is a content available inside this OffsetTime object.
[07:01] To understand the same, I'm going to print out these objects.
[07:04] If you see inside the console we have the time 15:30.
[07:08] Along with the time we also have offset details which is plus two.
[07:13] So whenever you have a requirement where you want to represent offset details also inside your time,
[07:19] you can use the OffsetTime object.
[07:22] Otherwise you can simply use LocalTime object where it is going to simply show you the time details
[07:28] but not the offset details.
[07:30] Now using these OffsetTime object, we should be able to invoke many methods like
[07:35] we should be able to invoke getHour() method to get number of hours that we have inside this Offset object.
[07:42] Similarly, we can invoke getMinute() method to understand how many minutes we have inside this object
[07:49] and after getMinute(), we should be able to invoke the getSecond() or getNano() method.
[07:56] But in our scenario, since we only define seconds, let's try to invoke only getSecond() and try to
[08:02] see what seconds we have inside these Offset object.
[08:05] So I'll try to create the variable which is second.
[08:07] This time I'll try to invoke the important method which is getOffset().
[08:13] So this is going to give you an object of ZoneOffset which will have the details of the offset that
[08:20] a particular offset time object holds.
[08:23] So I can try to mention the variable name as offset.
[08:26] So if you try to debug this program line by line, we should be able to see all the details like hour
[08:32] we have 15 minutes we have 30 and second we have zero.
[08:36] But coming to the offset we can see we have the offset value as +02:00.
[08:42] Similarly, there are many other methods that we can invoke with the help of the OffsetTime object.
[08:48] For example, if you want to add hours to this OffsetTime object, you can use this plus hours, plus
[08:55] minutes, plus nano and plus seconds.
[08:57] For now, let me invoke this plusHours() method, to this plusHours() method
[09:01] I'm going to pass our input as two, which means I want to add two hours to this offset time.
[09:08] So the output from these plusHours() method I'm going to catch with the help of a variable, which is
[09:14] later time.
[09:15] So just like how we have plusHours(), we also have minus related methods as well, which is going to
[09:21] help us to subtract a specified unit.
[09:24] For now, let's revert back to the plusHours() method.
[09:27] You can see as of now I have two objects of offset like offset time and this laterTime if I want to
[09:34] compare both of them to understand whether a given offset object is before or after, I should be able
[09:40] to invoke isBefore() method or isAfter() method, or isEqual() method.
[09:46] For now I'm going to invoke isBefore() method and to
[09:48] this isBefore() method.
[09:50] I'm trying to pass other offset time object, and the output from this method is going to be in boolean
[09:56] form.
[09:56] So let me define the variable which is isBefore.
[09:59] If I execute this program under the
[10:01] isBefore you can see we have true.
[10:03] Which means this offsetTime is before the laterTime, which is obvious.
[10:10] I hope you are clear on the purpose of offset time.
[10:13] I know there is a chance that you may get confused by looking at these all class names, but don't worry
[10:19] as and when you are trying to do more practice, you will get used to these class names and the scenarios
[10:24] around them anytime.
[10:26] If you have any questions, try to quickly revise all the slides that we have discussed so far.
[10:30] With that, you're going to get more clarity.
[10:33] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
