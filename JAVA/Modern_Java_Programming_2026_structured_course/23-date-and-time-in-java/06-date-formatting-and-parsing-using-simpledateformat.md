# 23.6 — Date formatting and parsing using SimpleDateFormat

> Section 23: Date and Time in Java

[00:00] The next common requirement that you may face whenever you are dealing with the Date objects is formatting
[00:06] them.
[00:07] As of now, if you see this is our default format that is being followed for all the Date objects,
[00:13] but sometimes we may want to store or display the Date objects in a specified format.
[00:19] So let's try to understand how to do the same.
[00:21] For the same,
[00:22] I'm going to create a new Java class with the name DateFormattingDemo.
[00:28] Inside this class I'm going to first create the main() method, followed by
[00:33] I'm going to first create a Date object with the variable name as currentDate.
[00:39] And on the right hand side I'm going to mention new Date.
[00:43] We know this Date is going to hold the current date and time, and it is going to display in a default
[00:48] format.
[00:49] So let's try to understand the same how it is going to display.
[00:52] So this is the format that it is following.
[00:54] Let me mention the same inside the comments as well.
[00:57] But sometimes we may want to display in a specified format.
[01:02] In those scenarios, what you have to do is you have to create the object of simple Date format, which
[01:08] is available inside the java.text package.
[01:11] So this also belongs to the Legacy Date API.
[01:14] I'm just giving the variable name as date format, followed by on the right hand side.
[01:19] Using the constructor of the SimpleDateFormat(), I'm trying to create the object to this constructor
[01:24] of the SimpleDateFormat.
[01:25] I'm trying to pass a format using which I want to format my date.
[01:30] So inside the String I'm going to type y four times.
[01:33] So y indicates year, followed by capital M two times, always capital M it is going to indicate month
[01:40] and small D indicates the date followed by HH:MM:SS.
[01:46] Here the capital H indicates.
[01:48] However, m indicates minutes and s indicates seconds.
[01:53] So please note that for months the M should be in capital, whereas for the minutes the m value should
[01:58] be in the lowercase value.
[02:00] So now using these DateFormat object, I can invoke the format() method, and to this format() method I
[02:06] can pass the CurrentDate object.
[02:09] If you see this format() method, it is going to give the output in a String format.
[02:13] So that's why on the left hand side, I need to catch the output with the help of String data variable.
[02:19] So I'll just mention the variable name as formatted date.
[02:23] Post that I'm going to print these formatted date.
[02:26] If I execute this program this time, you can see the date is displayed properly in the format that
[02:32] I have given.
[02:33] Like I have given four y's, which means I want to display my year in a complete four letters for month.
[02:40] It is zero two followed by nine, which is for date followed by time in hour, minutes and seconds.
[02:46] If you are looking to display the year only two digits, you can mention double Y, and with that,
[02:53] your year is going to be displayed in a two digits.
[02:56] Like instead of 2024, you're going to have the output as 24.
[03:00] Similarly, if you try to add one more M here, you will be getting the month details in a short form
[03:07] like February.
[03:08] But if you are looking for a full name of the month, you can mention four M's
[03:12] and with that you'll be able to see the complete month name.
[03:15] Let me show you one more demo around this formatting.
[03:19] This time I'm going to create the same objects.
[03:23] That's why I'm trying to copy the same code, but variable name I'm going to mention as date format
[03:27] one, formatted date one and the same I'm going to display.
[03:30] So here this time I'll try to get only that date information for the same
[03:35] I'm going to mention MM/DD/YYYY.
[03:42] So with this format you can expect the date in this format only.
[03:46] But before that let me try to update this date format to date format one.
[03:51] And if we execute this code you will be able to see the date in MMDDYY format.
[03:58] This way, based upon your requirements, you can always use these formats.
[04:03] With the help of the SimpleDateFormat.
[04:05] You'll be able to format your dates here.
[04:08] Whenever you are using capital H, it indicates you are looking for 24 hour format, whereas small H
[04:14] indicates you are looking for two hour format using these SimpleDateFormat.
[04:18] As of now, we are trying to format the given date into a specified format in the similar line.
[04:24] Sometimes you may want to perform the parsing as well.
[04:28] So what is a parsing?
[04:29] Parsing is a concept of converting a String value into an object.
[04:34] Think like you have received the date value in a String object.
[04:38] In this kind of scenarios, where you are receiving the date value in a String format, you may want
[04:43] to convert that into a Date object so that you can properly perform the validations, or you can store
[04:49] it.
[04:49] The requirement can be anything.
[04:51] But what I'm trying to say here is, parsing is another kind of common operation that you need to perform
[04:57] on your day to day activities.
[04:59] So
[04:59] let's try to understand how to perform the parsing.
[05:02] We can perform the parsing using the same SimpleDateFormat.
[05:05] So what we have to do is whenever we want to perform the parsing, first we need to decide the format
[05:11] of the date post that using the same date format object, we can invoke the parse() method, and to this
[05:18] parse() method we can send the String Date object.
[05:21] Let me show you a demo.
[05:22] First, I'm going to store the Date value using a Date string variable.
[05:27] On the right hand side
[05:28] I'm going to type 2100
[05:30] hyphen zero nine.
[05:31] Hyphen 26, followed by some time like 1430 zero zero.
[05:37] So this is a date value in a String format.
[05:40] Now what I'm going to do is since we can perform the parsing only with the help of SimpleDateFormat
[05:46] object, I'm going to copy these lines of code and paste it here.
[05:51] The very first thing that we need to take care is whenever we are trying to perform the parsing.
[05:56] With the help of SimpleDateFormat, you need to mention the format in the same format that your date
[06:03] is being stored inside the String object.
[06:05] So what is our format that we have here?
[06:07] We have four wise indicating the year followed by month in two digits.
[06:13] That means we need to mention MM in capital letters, followed by DD followed by space, followed by
[06:20] hHH indicating the hours and after the HH we need to mention colon followed by MM followed by SS.
[06:28] So I need to make sure I'm mentioning the same format like this
[06:33] value is being maintained, otherwise I'm going to get a runtime exception.
[06:37] I'll also show you the demo around this in few seconds, but before we try to see the demo, we need
[06:41] to fix some issues here.
[06:43] So here I'll change this variable name to dateFormat2 and the same dateFormat2
[06:48] I'm going to use it here.
[06:50] And with the help of this dateFormat2 object, I'm going to invoke the parse() method.
[06:55] To this parse() method we can pass the String representation of our date value.
[07:00] So this is the date String object that we can pass here.
[07:03] And with that you're going to get a compilation error which is around the exception handling.
[07:07] Whenever we are trying to perform the parsing, we need to make sure we are handling and checking exception
[07:13] with the name java.text.ParseException.
[07:16] Since I'm not trying to handle here this checked exception, I'm getting a compilation error for now.
[07:21] Let's not worry about handling these exception.
[07:23] Instead, I'm going to simply add the parse exception to the throws block with that, this compilation
[07:29] error here is all the return type from this parse() method is going to be a Date object.
[07:34] That's why on the left hand side we need to catch the output with that date, followed by I'll give
[07:41] a variable name which is past date the same.
[07:45] I'll try to print out with the help of System.out.println().
[07:48] If I try to execute this program, you'll be able to see that my String object is converted into the
[07:54] Date object.
[07:55] That's why I'm able to see these date value here.
[07:58] So this is a happy scenario.
[07:59] For a second, let's try to screw up these format by mentioning four MMMM.
[08:04] Whereas here the date is stored in a two digits.
[08:08] But we are trying to format into a proper month value.
[08:12] If I try to execute this program, you can see I'm going to get a runtime exception which is java.txet.ParseException
[08:17] java.txet.ParseException.
[08:19] So it is saying Unpassable date, because the format that we are trying to provide to parse the date
[08:25] is not matching with the content of the string object that we have provided.
[08:30] So that's why always make sure you are mentioning a proper same format when you're trying to create
[08:35] the SimpleDateFormat object.
[08:37] I hope you are clear on how to format and parse with the help of SimpleDateFormat class.
[08:43] Everything that we discussed around the java.util.Date, along with the SimpleDateFormat I have
[08:50] mentioned in these two slides for your reference.
[08:52] So please refer these examples whenever you are trying to quickly brush up your knowledge around the
[08:57] Legacy Date API.
[08:59] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
