# 23.18 — [JAVA 8] Period in java.time Date and Time API

> Section 23: Date and Time in Java

[00:00] With the help of Duration, we can identify the duration between two instances.
[00:07] Very similarly, if you are looking to identify the difference between two different dates, we can
[00:13] use the Period class.
[00:14] We have a Period class just like Duration.
[00:18] So this Period class is going to help us to identify the gap between multiple dates.
[00:24] I will try to show you the demo of this class by creating a new Java class with the name PeriodDemo.
[00:31] Inside this class,
[00:32] first let me try to create the main() method, followed by
[00:35] I'm going to create a couple of Date objects with the help of LocalDateClass.
[00:40] So this is my localDate1 object.
[00:44] And to this I'm going to assign the date with the year as 2015 and month as one and date as one.
[00:52] Very similarly, I'm also going to create one more object with the variable name as localDate2.
[00:57] But for this I'm going to mention the month as March, followed by date as 18.
[01:03] Now you can see we have two different localDate objects.
[01:07] If you want to identify the duration are the time difference between these two LocalDate objects,
[01:13] we can use the Period class, and using these Period class, we should be able to invoke the between()
[01:20] method.
[01:21] To this between() method, we can pass the objects of localDat1 and localDate2.
[01:27] On the left hand side, I can try to catch the output with the help of Period object.
[01:31] The same I can try to print out with the help of System.out.println().
[01:35] So if I execute this class, you will be able to see that this is the period.
[01:40] So here m indicates month D indicate day.
[01:43] Similarly, if the gap is very high it will also show you the year details.
[01:48] Let me show you the demo as well here instead of 2015
[01:51] let me mention 2013.
[01:53] With that, if you execute this program, you will be able to see that gap is two years, two months,
[01:59] 17 days each and every Period object that you are going to create inside your project, it is going
[02:04] to have a prefix p, whereas in the scenario of duration we are going to have the prefix as pe, because
[02:12] Duration is going to explain the difference using the hours, minutes, seconds and nanoseconds.
[02:18] But coming to the Period, it is going to show you the difference with the help of years, months,
[02:24] days.
[02:24] I hope you are getting the difference between Period and Duration.
[02:28] As a next step, let me show you that demo on how to create the objects of Period and the same Period
[02:33] objects we can use to add a date and time to the existing LocalDate objects.
[02:39] So there are multiple approaches to create the object of Period.
[02:42] The very first one is with the help of() method.
[02:45] To this of() method.
[02:47] You can see you can pass years, months and days to establish the Period.
[02:52] Similarly, you can use of days by providing the days of months by simply providing the months of weeks,
[02:58] by providing weeks and off years, by providing years.
[03:01] So first, let me try to show you how to create a Period object by invoking the of() method.
[03:07] So first I need to mention the number of years.
[03:10] So here I'm going to mention one followed by two followed by zero.
[03:15] So with this I'm trying to create a Period with the duration of one year two months.
[03:21] On the left hand side I can try to create a object of Period, which is one year with two months.
[03:29] So the same I'm trying to assign here.
[03:31] So if I try to print out these one year, two months onto the console, you will be able to see the
[03:37] output as one by two m.
[03:40] So y indicates year, m indicates month.
[03:42] In the similar lines, we can also use ofDays() method to create a Period object with a given number
[03:49] of days.
[03:50] So here I'm trying to give three by providing three as an input to these ofDays() method, I'm trying
[03:56] to create a Period object which is going to store the duration of three days.
[04:00] So on the left hand side, let me create the Period object with the name as three days.
[04:06] Now I have two different Period objects.
[04:08] Think like
[04:09] I want to add these periods to my LocalDate objects.
[04:12] So it is going to be very simple.
[04:14] Using your LocalDate object like localDate1, you can invoke the method which is plus.
[04:21] To this plus() method.
[04:22] You can pass a Period object like one year two months, and with that you're going to get a new
[04:28] LocalDate object, which I'm trying to store with the variable name as localDate3.
[04:33] So if I try to print out these localDate3, you'll be able to see that to this localDate1
[04:38] one year, two months is going to be added.
[04:41] So let me execute this program.
[04:43] You can see one year, two months are added to the initial localDate object which is going to store
[04:48] 2013 January 1st.
[04:50] The same kind of logic is also going to work for LocalDateTime as well and ZonedDateTime as well.
[04:57] So please feel free to use this plus() method whenever you
[05:00] want to add a period to a given object of LocalDateTime or LocalDate or ZonedDateTime.
[05:06] I'm assuming you're clear about the difference between the Period and Duration.
[05:10] You can use that duration whenever you're dealing with the instance, whereas you can use the periods
[05:16] whenever you are dealing with the LocalDate, LocalDateTime, ZonedDateTime, and other classes.
[05:23] Everything that we discussed around the Period class along with its difference from the Duration class
[05:29] I have mentioned in this slide.
[05:30] For your reference, I have also provided a code snippet with the code examples that we have discussed.
[05:36] I hope this is clear.
[05:37] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
