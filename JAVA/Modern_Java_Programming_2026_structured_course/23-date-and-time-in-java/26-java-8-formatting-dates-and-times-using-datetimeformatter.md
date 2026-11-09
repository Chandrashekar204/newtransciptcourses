# 23.26 — [JAVA 8] Formatting Dates and Times using DateTimeFormatter

> Section 23: Date and Time in Java

[00:00] I showed that demo on how to format a given Date object into another format with the help of
[00:08] SimpleDateFormat class.
[00:09] Now, inside this lecture, let's try to understand how to perform the same formatting with the new
[00:15] Date-Time API.
[00:16] We can't use a SimpleDateFormat class because that belongs to the old API.
[00:21] Instead, we have a class with the name DateTimeFormat inside the java.time.format package,
[00:30] so the class name is DateTimeFormatter.
[00:33] Let's try to understand how to perform the formatting of the date and time values. For the same,
[00:40] I'm going to create a new class inside the new API package with the name DateTimeFormatterDemo.
[00:49] Inside this class, as usual, I'm going to create the main() method followed by
[00:54] first, I'll try to create the objects of LocalDate, LocalTime and LocalDateTime, and I'll also
[01:00] show you how the date and time values are being displayed on the right hand side.
[01:04] Let me use the LocalDate.of() method to this of() method, I'm trying to pass the year as 2015 month
[01:12] as March, followed by day as 18.
[01:14] Similarly, I'll also want to create the object of LocalTime with the variable name as localTime,
[01:21] followed by LocalTime.of() the time I'm going to mention as 15:30, 0 seconds.
[01:28] So 15 indicates 15 hours, 30 indicates minutes, zero indicates seconds.
[01:33] Post that I'm also going to create the LocalDateTime object with the variable name as localDateTime
[01:38] and this I'll try to create with the help of() method.
[01:43] To this of() method I can pass 2015, 3, 18 followed by hour as 15 minutes as 30s as zero.
[01:53] So here I have mentioned capital O
[01:54] that's why I'm getting compilation error.
[01:56] Let me mention small o.
[01:57] So now I have three different objects ready.
[02:01] If I try to print out, all of them will be able to see what is the default format followed by the new
[02:08] Date-Time API.
[02:09] So let me copy paste this LocalDateTime here and execute this program.
[02:14] You can see this is the default format being used by the new Date-Time API.
[02:19] For a second, think like I want to replace this hyphen with the slash inside this LocalDate object.
[02:26] So how to achieve that?
[02:27] We can achieve that with the help of DateTimeFormatter class.
[02:31] With the help of DateTimeFormatter class, I need to invoke the method ofPattern() to this ofPattern().
[02:39] I need to pass the format pattern that I want to consider for my LocalDate.
[02:44] So I'll just mention small YYYY/MM/dd.
[02:51] So the output of this ofPattern() method is going to be an object of DateTimeFormatter.
[02:58] So let me create the object with the name DateTimeFormat here.
[03:02] Post that using these DateTimeFormatter I can invoke the format() method, and to this format() method
[03:09] I can pass my LocalDate object, which is local date itself, and the output from this format() method
[03:16] is going to be in a String format.
[03:18] That's why I'm trying to catch the output on the left hand side, with the variable name as formatDate,
[03:23] by defining the data type as String.
[03:25] Maybe I can try to change this variable name to formattedDate.
[03:29] Now I can try to print out the same unto the console so that we can see the difference.
[03:34] So if you see this time my date is displayed in a different format because I'm trying to use a
[03:41] DateTimeFormat object to format my given date.
[03:45] Similarly, this time let's think that right now my time is being represented with the 24 hour cycle.
[03:51] If I want to display in a 12h format by using Am and PM, I should be easily achieved that with
[03:58] the help of DateTimeFormatter class.
[04:01] So what I'm going to do is I'm going to copy this entire three lines of code into the next line.
[04:08] This time I'll try to mention this class name as TimeFormatter.
[04:13] Here also, I'll change this name to dateFormatter because we are only doing the date formatting, so I'll
[04:18] try to use the same here.
[04:20] Now the timeFormatter object, I'll use it here and to this format() method I'm going to pass the
[04:26] localTime as an input.
[04:27] And this variable name I'll just mention as formattedTime.
[04:31] But now question is what format we need to mention here.
[04:35] The format that we need to mention here is first you need to mention small h followed by mm indicates
[04:41] minutes followed by space followed by small a.
[04:44] So with this small a I'm trying to ask please display AM or PM inside my time details.
[04:51] So if I try to print out this formatted time into the output, you'll be able to see the output in a
[04:58] 12h format.
[04:59] Like 15:30
[05:01] we can represent as 3:30 p.m. as well.
[05:04] I hope you're seeing the power of formatting.
[05:07] Sometimes we may have requirements inside the real projects to convert a given date value into some
[05:12] other format, so that we can show that new format values onto the UI or onto the mobile application.
[05:18] The requirement can be anything in all these kind of scenarios, you can happily use the DateFormater
[05:24] object.
[05:25] This time, let me try to create one more DateTimeFormater object using which I'm going to format() these
[05:32] LocalDateTime.
[05:33] So let me send these localDateTime as an input to this format() method.
[05:38] Post that I'm going to change this variable name to dateTimeFormatter, because we are going to perform
[05:44] both date and time formatting.
[05:46] So let me replace this here and the variable name here I'll try to mention formattedDateTime.
[05:53] But now we need to mention a correct pattern as an input to these ofPattern() method.
[06:00] Let me mention the format as dd/MM/yyyy h:mm a.
[06:12] So let's see how the date and time is going to display with this pattern.
[06:16] You can see we are displaying first date followed by month followed by year.
[06:21] And at last we are displaying the time in a 12 hour format.
[06:25] I hope you are clear inside this approach.
[06:27] We are trying to perform the formatting by passing the hour, date and time objects as an input to the
[06:34] method of format(), which we can invoke with the object of DateTimeFormatter.
[06:39] Instead, we can directly use these LocalDate, LocalTime or LocalDate Time objects as well to invoke
[06:45] the format() method.
[06:47] So there is a format instance method also available inside these classes.
[06:51] So let me try to invoke the same.
[06:54] So using the LocalDate object I'm going to invoke the format() method. To this format() method we can pass
[07:02] an object of DateTimeFormater like here
[07:05] I'll try to pass these dateTimeFormatter as an input, and on the left hand side we can try to catch
[07:12] the output with the variable name as formattedDate1.
[07:17] With this line of code
[07:18] also we are going to get the same output.
[07:20] I can try to confirm the same by printing these formattedDate1 variable.
[07:25] So if I execute this program, you'll be able to see that I'm getting the same formatted date.
[07:31] So to this format() method we can pass the DateFormat object
[07:35] or we can also pass few of the predefined constants available inside the DateTimeFormatter class.
[07:42] So there are some constants like basic ISO date.
[07:46] So this is a format that you can use.
[07:48] So if you can open you'll be able to see the format.
[07:52] So whenever you are using these formats your date is going to be displayed like this.
[07:57] There won't be any special characters.
[07:58] Only the numerical values is going to be present.
[08:01] So if I execute this program this time, you'll be able to see the formatted date one is represented
[08:07] like this.
[08:08] Similarly, we have other constants as well which is ISO_LOCAL.
[08:14] So there are many constants which you can explore.
[08:16] But for now I'm trying to use ISO_LOCAL_DATE.
[08:19] If you want to understand how the format is going to look like, you just have to open the constant
[08:23] and look the documentation.
[08:26] So this is how the ISO local date format is going to look like.
[08:30] So if I execute this program this time, you'll be able to see that my date is being displayed in the
[08:36] format that we have provided.
[08:38] So these are the two approaches that we have discussed so far.
[08:41] With these two approaches
[08:42] we're only trying to format the date from one format to other format, but there is also advanced formatting
[08:49] support available with the help of DateTimeFormatter.
[08:52] Think like you are working for a German company and you want to display a date using the German language.
[08:59] So these kind of local language formatting support is also available with the help of DateTimeFormatter.
[09:07] Let me show you how to do that.
[09:08] What I'm going to do is, I'm going to create an object of DateTimeFormatter by copying this line of
[09:14] code and pasting at the end.
[09:16] So this variable I'm going to mention as germanFormatter.
[09:20] So whenever you want to use a format which is specific to a region, you need to provide that information
[09:27] to the ofPattern() method.
[09:28] So there are two overloaded ofPattern() methods.
[09:31] So if you try to invoke ofPattern() method.
[09:33] So there is one ofPattern() method which is going to simply accept the String as an pattern.
[09:39] The other method, it is going to accept a pattern along with the local details.
[09:45] I'll try to invoke the second method.
[09:47] First
[09:47] I'll mention a pattern that is going to match with the Germany date.
[09:52] So the pattern is, d. MMMM four m's
[09:59] I'm trying to
[10:00] which are capital letters, followed by I'm going to mention yyyy four times, and at last I'm
[10:06] going to type Locally.GERMAN.
[10:09] So there is a constant available inside the Locally class with the country name as GERMANY.
[10:13] Similarly, it has so many other countries as well.
[10:16] For example, you'll have US, you will have CHINA.
[10:19] So it's up to you which one you want to use.
[10:22] As of now, I'm trying to use GERMAN.
[10:24] Now, using this germanFormatter object, I can try to invoke the format() method, to this format() method
[10:31] I'm going to pass localDate object as an input, and on the left hand side I can try to catch the output
[10:39] with the variable name as formattedDateGermany.
[10:43] So the same
[10:44] I'll try to print out onto the console with the help of this variable, which is formattedDateGermany.
[10:50] So let me execute this program.
[10:52] At the end
[10:53] you can see I'm able to see the date in a German format.
[10:57] I'm not sure if this is correct or not, but someone from Germany, I'm assuming it is making sense
[11:02] to them.
[11:02] So this way you can always use the DateTimeFormatter even for the advanced formatting, like where
[11:09] you want to format your date to a specific local country or a local region.
[11:15] I hope you're clear about everything that we have discussed around the formatting of the date.
[11:19] With the help of DateTimeFormatter class, all the code examples that we have discussed inside this
[11:25] lecture I have mentioned in this slide for your reference.
[11:28] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
