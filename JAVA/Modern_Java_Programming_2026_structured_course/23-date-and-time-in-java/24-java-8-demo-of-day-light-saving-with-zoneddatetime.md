# 23.24 — [JAVA 8] Demo of Day Light Saving with ZonedDateTime

> Section 23: Date and Time in Java

[00:00] Inside this lecture, I want to show you a demo on how ZonedDateTime object is going to handle the complexities
[00:08] around the daylight saving time.
[00:11] Before I try to show you the demo around the daylight saving time, first let me explain you what is
[00:16] a daylight saving time?
[00:18] For the same, I'm going to search what is DST inside my chrome?
[00:24] DST means daylight saving time and with that you will have a Wikipedia link which you can open if you
[00:30] try to read this explanation, it is pretty clear.
[00:32] So Daylight Saving Time is a concept where few countries like United States, Canada and Australia,
[00:39] they are going to advance their clocks by one hour during the warmer months so that darkness falls at
[00:47] a later clock time.
[00:48] If you take United States as an example, what they are going to do is, they are going to advance their
[00:54] clock by one hour on every March 2nd Sunday at midnight, 2 a.m..
[01:00] So what is going to happen?
[01:02] Think like today is a March 2nd Sunday.
[01:04] So during the midnight at 2 a.m., all the clocks will be changed to 3 a.m. by advancing one hour.
[01:12] Similarly, when they are close to the winter, what they are going to do is, they're going to set clocks
[01:17] back to one hour in the fall.
[01:20] So when this is going to happen in us, it is going to happen during the November 1st Sunday.
[01:25] So during the November 1st Sunday after the midnight, they're going to make their clock one hour behind.
[01:32] So this is a quick introduction about that daylight saving time.
[01:35] If you want to understand more details around this, you can read this Wikipedia or there are enough
[01:40] videos in YouTube explaining about the daylight saving time.
[01:44] Now let's try to understand how that daylight saving time complexities it is going to be handled by
[01:49] the ZonedDateTime class.
[01:51] To show you the demo, I'm going to create the new class with the name
[01:57] ZonedDateTimesDstDemo, DST means daylight saving time. Inside this class,
[02:03] first, let me try to create the main() method post that I'm going to copy few lines of code, which we
[02:10] can discuss in detail.
[02:11] I'm trying to save some time here because you are already familiar with all these syntaxes.
[02:16] I'll make sure I'm explaining each line by line.
[02:18] If you want, you can get the same code from the GitHub repo.
[02:21] So what I'm doing here first, I'm trying to create an object of ZonedDateTime by providing some date
[02:28] values and time values with a zone ID as America Los Angels in US, we can also call these Los Angeles
[02:35] Time zone as pst, pst means Pacific Standard Time.
[02:41] Think like you are building a business logic for one of the airlines company.
[02:46] So these are the time that a flight is going to departure from PSG time zone.
[02:52] And this flight is going to take four hours to travel to New York from Los Angeles.
[02:58] So that's why what I'm doing is to this departure object.
[03:02] I'm trying to add four hours and post that
[03:05] I'm trying to convert that time into the equivalent to time by passing the zone ID as America/
[03:11] New York, New York time zone
[03:13] in short form, we can call it as s t Eastern Standard Time.
[03:18] So if you want to send these details to the person who booked the flight ticket, saying that your flight
[03:23] is going to start at so-and-so time and it is going to arrival at so-and-so time, definitely
[03:29] you need to be very careful because these two cities like Los Angeles and New York, they stay in a
[03:35] different time zone.
[03:36] So let's try to execute these example and try to understand the complexities around this and how zone
[03:42] date time is going to handle it seamlessly.
[03:44] So first what I'm going to do is I'll try to create the date as 2024 February 2nd at night, 9 p.m.
[03:52] it is going to departure, so 21 indicates 9 p.m..
[03:56] And with that, let's try to understand at what time the flight is going to arrive in the new York.
[04:02] So the values inside this Departure object and Arrival object I'm trying to print out with these System.out.println().
[04:09] So if I execute this program, you can see the flight is going to departure at February 2nd at 9 p.m..
[04:17] So the Los Angeles time zone is going to be present inside the UTC offset which is -8.
[04:24] Now coming to the EST time, it is going to arrive the next day, which is February 3rd at early morning 4.
[04:32] Technically, if you simply add four hours to these 21, so the time should be 22, 23, 24, and
[04:40] 1.
[04:40] So it should be 1 a.m..
[04:42] But here we have 4 a.m. because behind the scenes, the ZonedDateTime is trying to convert the
[04:48] date between the two time zones efficiently.
[04:51] That's why to the customer we are going to send the details like that
[04:54] the flight is going to arrive the next day, which is February 3rd at
[04:59] 4 a.m. EST time. So this is a normal day.
[05:02] But like I said before, every March 2nd Sunday, the daylight saving is going to happen.
[05:09] During the same time, all the clocks will be advanced to by one hour.
[05:14] Please remember, as of now we have these offsets as -8 and minus five.
[05:18] What I'm going to do is I'll go to the Google
[05:21] inside Google, I'll search DST in 2024.
[05:26] It is going to tell me that DST is going to start on March 10th, 2024.
[05:32] So this is the second Sunday inside March.
[05:35] So what I'm going to do is, I'll set that date of departure as March 9th night and the time as 9 p.m.
[05:44] and with that, by the time the flight land onto the arrival, the DST might have activated during the
[05:51] midnight during 2 a.m..
[05:53] So let's see how this is going to work in these kind of scenarios.
[05:57] But before that, I'll try to copy these values for comparison and mention the same here at the end
[06:04] of the class.
[06:05] Now I'll try to execute this program.
[06:07] And this time you can see these are the values.
[06:10] So let me copy these values and paste it here.
[06:14] I'll just mention comments before these values.
[06:17] So if you see here there is no change in terms of PSG.
[06:21] It is the same offset which is -8 and the time also 21.
[06:26] And the date is 39 here.
[06:28] But by the time the flight is going to land we are entering into the next day, which is 310 and this
[06:35] time instead of 4 a.m., it is showing 5 a.m. on top of that, it also adjusted the offset, which is
[06:42] -4.
[06:43] So what happened behind the scenes?
[06:45] Behind the scenes
[06:46] as soon as the March 10th started at midnight to 2 a.m., all the clocks will be advanced by one hour.
[06:53] So that's why instead of -5 offset here we have -4 offset and similarly the arrival
[06:59] time instead of 4 a.m. we have 5 a.m..
[07:02] So are you seeing the beauty here of that
[07:04] ZonedDateTime the legacy Date-Time API
[07:07] achieving all this is hell lot of work.
[07:10] But with the help of new Date-Time API it is just a cakewalk.
[07:13] I just have to use the classes and methods available.
[07:17] All the complexities are on the time zone and daylight saving
[07:21] they are going to be handled by the date API.
[07:24] Behind the scenes
[07:25] this is the feeling that you're going to get when you are
[07:28] program and business logic is working seamlessly during the daylight saving time changes as well.
[07:35] Believe me, if your work is working without any issues on daylight saving, it is a big achievement.
[07:41] You need to be proud of yourself.
[07:43] That's why inside real projects always try to understand the corner scenarios around the daylight saving
[07:48] as well and make sure you are handling them.
[07:51] Otherwise, on the March 10th midnight you're going to get an S.O.S. call from your manager.
[07:57] I hope you are clear with this program.
[07:59] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
