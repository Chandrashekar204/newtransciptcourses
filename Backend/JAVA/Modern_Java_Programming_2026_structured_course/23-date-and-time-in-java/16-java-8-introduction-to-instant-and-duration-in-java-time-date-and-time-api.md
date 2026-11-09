# 23.16 — [JAVA 8] Introduction to Instant and Duration in java.time Date and Time API

> Section 23: Date and Time in Java

[00:00] As of now, when we're trying to store that date and time details, we are trying to create the objects
[00:06] of LocalDateTime and ZonedDateTime.
[00:09] But apart from these classes, we also have other class with the name Instant.
[00:14] Using these Instant also, we should be able to create the objects that are capable of storing date
[00:20] and time value.
[00:21] Inside this lecture, let's try to understand more details about this Instance class and under which
[00:26] scenarios we need to use them and how it is different compared to the other classes that we have discussed
[00:32] so far.
[00:32] We as humans, we use date and time values, but for machines, the time is calculated based upon number
[00:40] of seconds passed from the Unix epoch time.
[00:44] What is the epoch time?
[00:45] The epoch time inside computer is represented by the time which is midnight of January 1st, 1970 UTC.
[00:52] If you try to look at these representation, this zero represents the epoch time, which is the midnight
[00:59] of January first, 1970 UTC.
[01:02] After this epoch time, we have various numbers like 1, 2, 3, 4.
[01:06] For each of these numbers, they represent the number of nanoseconds passed from the epoch time.
[01:12] So if you try to travel on to the right hand side, all the nanosecond numbers will be positive.
[01:17] Whereas if you try to travel on to the left hand side, which is before the epoch time, all the numbers,
[01:22] they are going to be represented with the help of negative numbers like you can see here. Each of these
[01:27] numbers inside the timeline, they are representing an instant time from the epoch time.
[01:33] If you take these eight, this is an instant time which represents that eight nanoseconds completed
[01:39] from these epoch time.
[01:41] Inside Java
[01:42] whenever we want to create an object representing these instant time, we can use the Instant class
[01:49] available inside the new Date-Time API.
[01:52] And apart from Instant, we also have Duration class.
[01:55] So what is a Duration?
[01:56] Duration is used to identify the duration of time between two instances.
[02:02] For example between these 3 and 11
[02:05] if I try to identify the duration, it is going to be 8 nanoseconds.
[02:10] So whenever we want to represent the duration between two time instance or between two dates, or between
[02:17] two times, in all such scenarios, we can use the Duration object. Inside this Duration object, the
[02:23] difference between two time instances
[02:25] they are going to be stored in terms of hours, minutes, seconds, and nanoseconds.
[02:31] When we see the demo about these Instant and Duration, it is going to make more sense to you.
[02:35] For now, let's try to understand more details about these classes.
[02:38] This Instant class
[02:40] it is often used for low level operations where precise timestamps are required, such as logging or
[02:48] measuring elapsed time.
[02:49] For example, think like you're trying to calculate the duration between two different events occurred
[02:55] inside your application.
[02:57] In all these kind of scenarios, you are going to create two different instant object representing the
[03:02] start of the event and the end of the event, and the duration between them can be calculated with the
[03:09] help of Duration class.
[03:11] Here at the end of the slide, I also highlighted all the points that we have discussed.
[03:15] I tried to explain about this timeline and how it is work with the help of these two points here.
[03:20] With this
[03:21] now you may have a question running behind the scenes, which is what is the difference between instant
[03:26] and the LocalDateTime or ZonedDateTime.
[03:30] So let's try to understand the same.
[03:31] We know both Instant, LocalDateTime and ZoneDateTime.
[03:35] They all can be used to represent date and time values inside Java, but they have a fundamental differences
[03:41] in how they work internally.
[03:43] Here I'm trying to compare between Instant and LocalDateTime.
[03:46] So the same comparison is also applicable for Instant and ZoneDateTime as well.
[03:51] So the very first difference is whenever you are trying to represent a time with the help of Instant,
[03:57] it is going to represent a specific moment in time from the epoch time.
[04:01] Whereas if you try to represent a date and time with the help of LocalDate time behind the scenes,
[04:06] the date and time values are going to be stored without the time zone details.
[04:10] Whereas if we use ZoneDateTime, even the time zone details are also going to be stored.
[04:15] Coming to the internal representation internally, all the Instant objects, they are going to be represented
[04:21] with the help of seconds and nanoseconds since Unix epoch time, whereas inside the LocalDateTime
[04:26] or ZoneDateTime, all the date and time details are represented with the help of year, month, day,
[04:32] hour, minute and second.
[04:34] And the third difference is instant is independent of time zone.
[04:38] Instant is not going to worry about time zone.
[04:41] It is only going to worry how many nanoseconds or seconds passed from the Unix epoch time, whereas
[04:47] the LocalDateTime, though it is not going to contain any time zone information.
[04:51] But behind the scenes it is going to consider your local time zone to create that date and time value.
[04:57] If I try to invoke the now() method present inside
[05:00] the LocalDateTime, it is going to give me the current date and time based upon the time zone where
[05:05] I am executing the code. And at last we have use cases
[05:08] you should consider using the instant whenever you are very serious about representing your time with
[05:13] the help of Timestamps, Durations, TimeZone, IndependentTime.
[05:17] In all those scenarios, you can use the instant. Coming to the LocalDateTime and ZonedDateTime
[05:21] you can use them whenever you want to display the dates and time in an user friendly manner.
[05:27] I also provided more details when to use which class, so you can use Instance when you need to represent
[05:32] a specific point in time, regardless of location or time zone.
[05:36] So this is ideal for Timestamps, Durations and Calculations, whereas LocalDateTime you need to use
[05:43] when you display the dates and times to user in their local time zone or when the specific moment
[05:50] itself is not critical.
[05:51] I hope you are clear with this initial introduction around the Instant and Duration.
[05:55] In the next lecture, I am going to show you the demo of these classes so that it's going to be more
[06:00] clear for you.
[06:01] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
