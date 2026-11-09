# 23.27 — [JAVA 8] Parsing Dates and Times using DateTimeFormatter

> Section 23: Date and Time in Java

[00:00] After formatting
[00:01] the next common requirement that you may face on your day to day work is around the parsing.
[00:06] So what is a parsing?
[00:08] Parsing is a process of converting String representation of date and time values into the objects of
[00:14] date and time.
[00:14] So let's try to understand how to perform the parsing with the new Date-Time API.
[00:20] Even for the parsing, we need to create the object of DateTimeFormatter.
[00:24] What I can do is I can try to create a new Java class with the name ParsingDemo.
[00:30] Inside this class I'm going to create the main() method followed by
[00:35] I'm going to create the object of DateTimeFormatter with the variable as DateTimeFormatter is equal to
[00:43] DateTimeFormatter of pattern and to this off pattern method, let me mention the format in a String
[00:50] format, which is yyyy-MM-dd.
[00:56] Similarly, let me try to create other DateTimeFormatter objects with the variable name as timeFormatter
[01:03] and dateTimeFormatter.
[01:05] To this time formatter, I'm going to mention that time format as HH:mm:ss.
[01:14] Now coming to these DateTimeFormatter, I'm going to mention the format as dd/MM/yyyy
[01:23] followed by HH:mm:ss.
[01:29] You can see I have created three different date time format objects that I can use to perform the parsing
[01:36] operation.
[01:36] First, let me try to create a variable with the name dateString, and to this dateString I'm going
[01:43] to assign that date in a String format.
[01:45] So let me type .
[01:50] 2015-03-18.
[01:51] So based upon how the date is stored inside your String representation, the same format you need to
[01:57] mention while you are trying to create the object of DateTimeFormatter, I make sure I'm following
[02:02] the same pattern in both inside the String representation and while creating these DateFormatter object.
[02:09] Very similarly, let me try to create the another object with the name time String, and inside this
[02:16] I'm going to store that time as 15, followed by 30, followed by zero zero.
[02:21] So I'm trying to use the same format.
[02:23] Next I'm going to create one more String variable with the name dateTimeString.
[02:28] Inside this variable we need to type first day which is 18/ followed by zero three, followed by
[02:36] 2015, followed by space.
[02:38] After the space I need to mention 15:30:00.
[02:42] So I'm making sure I'm following the same pattern that I have defined here.
[02:46] Now let's try to understand how to convert these String date representation to the corresponding date
[02:52] and time objects.
[02:53] So these are date value.
[02:54] So that's why I need to invoke the LocalDate class.
[02:59] Inside this LocalDate class I have a parse() method.
[03:02] To this parse() method I can pass what is the dateString followed by what is a formatter object that
[03:10] I need to use.
[03:11] So I want to use the DateFormatter object.
[03:13] That's why I'm trying to mention that DateFormatter as an input.
[03:17] So the outcome from these parse() method is going to be an object of LocalDate.
[03:22] So that's why I'm trying to catch on the left hand side with the variable name as LocalDate.
[03:28] Very similarly, let me try to perform the parsing by using these time String variable for the same
[03:34] instead of LocalDate
[03:35] I need to invoke LocalTime since we are trying to parse only time, and to this parse() method, we need
[03:41] to parse this time String as an input and the formatter.
[03:44] This timeFormatter we need to pass as an input, and on the left hand side, we need to catch the output
[03:50] with the help of LocalTime and with the variable name as localTime.
[03:54] In the similar lines, we can also use LocalDateTime to invoke the parse() method, and to this parse()
[04:01] method, we need to pass these dateTime String followed by these DateTimeFormatter.
[04:06] On the left hand side, we need to catch the output with the help of LocalDateTime and this variable
[04:12] we can change to LocalDateTime.
[04:14] So if I try to keep a breakpoint here and execute this program, you'll be able to see that LocalDate
[04:20] right now has the same date which I have mentioned inside the String.
[04:23] But this time the date values are stored in the form of LocalDate object.
[04:28] Similarly, the LocalTime also has time and LocalDateTime has both date and time.
[04:34] So this is how you need to perform the parsing.
[04:36] You just have to invoke the parse() static methods available inside these classes.
[04:41] To this parse() method, you need to pass your string representation of your date and time values along
[04:46] with the formatter object.
[04:48] If you try to use a different format inside these DateTimeFormatter object compared to the format
[04:54] mentioned inside your String value, then you're going to get a runtime exception.
[04:58] Think like here
[04:59] I am trying to mention hyphen instead of slash.
[05:03] With that, you're going to get a runtime exception saying that DateTimeParseException.
[05:09] So that's why always make sure you are mentioning the same format like you have inside your String representation.
[05:16] I hope this is clear.
[05:18] All the examples that we have discussed inside this lecture I have mentioned in this slide for your
[05:23] reference.
[05:24] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
