# 23.25 — [JAVA 8] Non-ISO Calendars in java.time Date and Time API

> Section 23: Date and Time in Java

[00:00] The beauty of new Date-Time API is it covered all the possible scenarios around the Date and Time.
[00:07] We know most of the countries in the world they follow the GregorianCalendar.
[00:12] In other words, we can call this GregorianCalendar as ISO calendar or English calendar, but apart
[00:19] from ISO or GregorianCalendar, we have other types of non ISO calendars as well exist in few countries.
[00:27] Such calendars are Thai Buddhist calendar, which is going to be followed inside Thailand.
[00:33] Hijra calendar which is going to be followed by the Islamic countries.
[00:37] Minguo calendar, which is followed inside the China and Japanese calendar, which is followed inside
[00:43] the Japan.
[00:44] Please pardon me if I pronounce these calendar names incorrectly.
[00:49] The point that I'm trying to highlight here is, the new date Time API that introduced in Java 8.
[00:54] It also supports other types of calendars, which are used only in specific regions.
[01:01] All these kind of calendars we can call as non ISO calendars.
[01:05] For example, think like you are working for an organization which operates inside Japan.
[01:10] Obviously, if they want to localize their content to the Japan people, sometimes they may have to
[01:17] display that date based upon that Japan calendar.
[01:20] With the legacy Date-Time API, we don't have any option to identify what is the equivalent date for
[01:27] the Japan calendar based upon a given English calendar date, but with the new date time API, it is
[01:33] going to be super fun and easy.
[01:35] Here you can see I'm trying to use a class with the name JapaneseDate. Using this class,
[01:41] if I invoke the now() method, it is going to give me that today's date based upon the Japan calendar.
[01:48] Whereas if we use our LocalDate.now() it is going to give that today's date based upon the GregorianCalendar
[01:53] or based upon the English calendar.
[01:56] Apart from simply creating the non ISO calendar objects, we can also convert a non ISO date to ISO
[02:04] date and vice versa.
[02:05] Here you can see with this from() method which is available inside the JapaneseDate.
[02:10] I'm trying to convert my ISO date or English date to an equivalent JapaneseDate.
[02:16] So these ISO now object I'm trying to pass as an input here.
[02:20] Similarly inside the LocalDate class
[02:23] also we have a from() method to this
[02:25] you can pass any calendar object like JapaneseDate class object.
[02:29] If you pass this as an input, it is going to give you the equivalent to date as per the GregorianCalendar
[02:36] or as per the English calendar. For each of the non ISO calendar systems available inside the new date
[02:43] time API.
[02:44] Usually there will be two pair of classes.
[02:46] So these classes they are going to present inside the package java.time.chrono one class
[02:52] it is going to have a suffix which is chronology.
[02:55] For example, if you take the Hijra calendar, there is a class with the name
[03:01] HijraChronology.
[03:02] So all these chronology classes, they are going to have the set of rules and characteristics belongs
[03:08] to the particular calendar.
[03:09] Whereas using the other class we can represent the date object which belongs to a particular calendar.
[03:16] Such classes are HijraDate, JapaneseDate.
[03:19] So you're going to have a prefix, which is the calendar name followed by date.
[03:23] I hope you are clear with this quick introduction.
[03:26] Let's see the demo of Japanese calendar so that it is going to be make more sense to you.
[03:31] Inside my package, I'm going to create a new Java class with the name JapaneseCalendarDemo.
[03:39] Inside this class
[03:40] first I'm going to create the main() method post that using that JapaneseDate, I'm going to create a
[03:48] object with the variable name as japaneseDate.
[03:50] Post that using the same class name, I'm going to invoke the now() method.
[03:55] So this is going to give me that today's date based upon the Japanese calendar.
[04:01] Similarly, if I try to use the LocalDate, I'm going to get the current date and time based upon the
[04:08] ISO calendar or the GregorianCalendar.
[04:11] So if I try to put a breakpoint here, you'll be able to see in local date today date is February 11th,
[04:19] 2024.
[04:20] But if you see inside the Japanese day today's date, here is some 602-11.
[04:26] I'm assuming someone who is from Japan
[04:28] it is making more sense to them.
[04:30] So this way you can always create current date and time for any calendar system that is supported by
[04:37] the new Date-Time API.
[04:38] And like we discussed, if needed, we can also convert one calendar date into the other calendar date.
[04:45] So here, with the help of JapaneseDate class, I'm trying to invoke the from() method and to this from()
[04:51] method, I am passing the object of LocalDate, and with that we're going to get the object of JapaneseDate
[04:57] as an output, which I
[05:00] I'm going to catch with the variable name as japaneseDate1.
[05:03] Similarly, using the LocalDate class as well, we can invoke the from() method and to this from() method
[05:10] we can pass the object of JapaneseDate, and on the left hand side we can catch the output with the
[05:16] help of LocalDate object with the variable name as localDate1.
[05:21] So if I execute this program, you will be able to see and a localDate1.
[05:25] The date is 2024 February 11th, whereas under the japaneseDate1 this is the value that it holds.
[05:32] So this kind of conversion from one calendar to other calendar is also possible.
[05:37] So if you can open these JapaneseDate class, it is available inside the Java.time.chrono package.
[05:45] Similarly we have other kind of calendars like HijrahDate.
[05:48] So here we have a class with the name type.
[05:51] With this date and MinguoDate also is available, which is going to be used inside China.
[05:56] So please refer to these classes whenever you have a requirement to build the date and time based upon
[06:02] a specific non-iso calendar system.
[06:06] I hope this makes sense to you.
[06:07] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
