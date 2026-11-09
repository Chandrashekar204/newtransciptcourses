# 23.20 — [JAVA 8] The truncatedTo() method

> Section 23: Date and Time in Java

[00:00] Inside this lecture, we're going to discuss about the truncatedTo() method that we can use on top of
[00:07] a Duration object.
[00:09] To show you the demo, let me create a new Java class with the name TruncatedToMethodDemo.
[00:18] Inside this class
[00:19] first, let me create a main() method post that I'm going to create a Duration object with some random
[00:27] duration, so I'll just type Duration.ofDays().
[00:32] So to this I'm trying to pass 28 days, followed by I'm going to add hours to the days with the help
[00:39] of plusHours(), to this plusHours() method
[00:41] I'm trying to pass 6 post that
[00:44] I'm going to also add minutes with the help of plusMinutes(), to this plusMinutes(), I'm going to send
[00:51] the 56 minutes as an input, followed by
[00:53] I'm also going to invoke plusSeconds() method.
[00:57] And to this method I'm providing 19 seconds.
[00:59] So with this I'm trying to create a duration of total 28 days, six hours, 56 minutes, 19 seconds.
[01:07] But we know behind the scenes duration is never going to store that duration in a form of days.
[01:13] It is always going to store with the units of hours, minutes and seconds.
[01:18] That's why if I try to see the content of this Duration object at runtime, you'll be able to see the
[01:23] duration as six 78 hours, 56 minutes, 19 seconds.
[01:29] I can copy this value the same
[01:31] I'll try to mention for your reference here.
[01:34] Just after this line
[01:35] inside the comments, I'm trying to mention the duration value.
[01:38] So how these two 78 hours came.
[01:40] So behind the scenes it is going to multiply 24 hours to these 28 days.
[01:45] And we are going to get the output as 672, to the same 672 hours
[01:50] it is also trying to add six hours.
[01:52] So that's why we are getting 678 hours followed by 56 minutes 19 seconds.
[01:57] Now think like I want to truncate these duration to the number of days, which means I don't want to
[02:04] carry the number of hours and seconds which are beyond the exact number of days.
[02:10] So in all such scenarios, I can happily use that truncatedTo() method.
[02:15] So with the help of Duration object, I'm trying to invoke the truncatedTo() method. To this truncatedTo()
[02:21] method, we need to pass the TemporalUnit as an input.
[02:25] So what is this TemporalUnit?
[02:27] It is an interface inside the new Date-Time API which represents a unit of date and time.
[02:33] So there is an implementation enum for these interface with the name ChronoUnit.
[02:39] So you can see inside this ChronoUnit we have so many enum constants like NANOS, MICROS, MILLIS, SECONDS,
[02:45] MINUTES, HOURS, HALF_DAYS, DAYS, WEEKS, MONTHS, YEARS, DECADES, CENTURIES, MILLENIA, ERAS, FOREVER.
[02:53] So these are all the enum constants that we have inside this class.
[02:56] So we need to pass days as an input.
[03:00] Whenever you are trying to truncate your duration to days.
[03:04] So that's why here to this method I'm going to pass the enum constant of ChronoUnit, which is DAYS.
[03:11] With that, all the extra hours, minutes and seconds they are going to be truncated.
[03:16] So let me catch the output inside the variable which is daysTruncated.
[03:21] If I try to see what is present inside these daysTruncated at runtime, you can see I have 672 hours,
[03:29] so the extra 6 hours and 56 minutes 19 seconds
[03:33] they are truncated because these 672 hours will result into the exact number of days, which is 28
[03:41] days.
[03:41] So all the extra hours, minutes and seconds beyond a given number of days they are going to be truncated.
[03:48] So here I'm going to get the output as PT672H.
[03:54] We can also truncate hours and minutes as well.
[03:56] So here instead of days if I try to mention hours, then all the minutes and seconds they are going
[04:03] to be truncated.
[04:04] With that we are going to get the output as 678H.
[04:07] So this minutes like 56M 19 seconds, they are going to be truncated, followed by if we pass
[04:13] the constant as minutes, we are going to get the output as 678H56M.
[04:21] So the seconds they are going to be truncated.
[04:23] So let me change this variable names to hours truncated.
[04:27] Later on I'll mention minutes truncated, if I try to observe these values at runtime
[04:33] you can see we have 678 hours under the hours truncated variable and 678 hours 56 minutes as an
[04:40] value inside these minutes truncated.
[04:43] So based upon your constant that you are trying to pass, the duration is going to be truncated.
[04:48] So especially these truncated methods, they are going to be useful when you want to ignore some duration
[04:55] especially seconds minutes, hours.
[04:58] One important point that
[04:59] you need to be aware whenever you are using this truncatedTo().
[05:02] Please make sure you are only using the variables like day, hours, minutes, seconds, and below constants
[05:10] only.
[05:11] Don't try to be smart and use constants like weeks, because we know duration is never going to store
[05:16] the week's information.
[05:18] So if you try to use invalid constants, we are going to get a runtime exception saying that unit is
[05:25] too large to be used for truncation.
[05:27] So that's why always use a constants like days, hours, minutes, seconds are any smaller constants.
[05:34] These truncatedTo() method is not available inside Period, because we know with the help of Period
[05:40] we represent the differences between dates, and there is no meaning to truncate such a larger values.
[05:46] So that's why truncated is not supported inside the Period.
[05:49] But you should be able to identify similar truncated methods inside the LocalTime class.
[05:56] So inside this class, if you type for truncatedTo(), you have the same kind of method.
[06:01] Similarly, inside the Instant class
[06:04] also you have this method with with the name truncatedTo(), so please feel free to use them based upon
[06:11] your requirements.
[06:12] Everything that we discussed around the truncatedTo() I have mentioned in this slide.
[06:16] I hope you are also realizing the beauty of the new Date-Time API.
[06:20] It is providing lots and lots of functionality which you can use to develop any kind of business logic.
[06:27] I'm just trying to discuss most commonly used methods.
[06:30] If I start discussing all the methods and all the features supported by the new Date-Time API, it will
[06:36] easily take months and months of time.
[06:38] That's why my humble request is to practice more and more around these new Date-Time API.
[06:44] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
