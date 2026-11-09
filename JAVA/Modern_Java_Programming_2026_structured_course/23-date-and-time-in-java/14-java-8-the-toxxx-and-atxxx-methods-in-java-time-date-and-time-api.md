# 23.14 — [JAVA 8] The toXxx() & atXxx() methods in java.time Date and Time API

> Section 23: Date and Time in Java

[00:00] Inside this lecture, let's try to understand other type of methods available inside the new Date-Time
[00:06] API.
[00:07] I'm going to create a new Java class with the name ToAndAtMethodsDemo.
[00:15] Inside this class I'm going to show you the demo of two related method and at related methods.
[00:20] First, let me try to create the main() method post that I'm going to create the object of LocalDateTime.
[00:27] What I can do is, I can try to copy this code and paste the same inside these
[00:33] ToAndAtDemo class.
[00:33] So here I'm trying to create an object of LocalDateTime.
[00:37] Previously when we were trying to extract a specific information like date and time, we use the from
[00:44] method by using the LocalDate class or LocalTime class.
[00:49] So whenever you are using the from() method, you need to make sure you are using the class name belong
[00:55] to the component that you are trying to extract.
[00:57] For example, from this DateTime object
[00:59] if you're trying to extract out only date information, then you need to make sure you are using the
[01:03] LocalDate class to invoke this from() method.
[01:06] Similarly, if you are trying to extract only the time related information, you need to make sure you
[01:11] are using the LocalTime class.
[01:13] So this is one approach to extract a specific component like date or time.
[01:17] The other approach is with the help of to() method.
[01:20] So whenever we are using the to() method, we can directly use this object like DateTime and using this
[01:27] object
[01:27] if you try to type to, we have various methods like toLocalDate() and toLocalTime().
[01:32] So toLocalDate() is going to help us to give the object of LocalDate. The same
[01:39] I'm trying to catch on the left hand side.
[01:41] Very similarly
[01:42] you can also invoke the toLocalTime() and on the left hand side we need to catch the output with the
[01:49] help of LocalTime and with the variable name as time.
[01:52] So here I'm getting a compilation error, because on the right hand side I need to invoke the method
[01:57] which is toLocalTime().
[01:59] So now if I try to print out these two objects like date and time, we should be able to see the same
[02:07] behavior like we saw in the previous lecture.
[02:09] So I'm trying to extract only date and only time.
[02:12] So this way you can always use that to related methods directly with the help of the object that you
[02:18] have in your hand.
[02:19] So this seems to be more simple to me.
[02:21] Whereas with the help of from() method, you need to make sure you are invoking these static methods with
[02:26] the specific class like LocalDate
[02:29] in the scenario where you are trying to extract the date and local time in the scenarios where you are
[02:33] trying to extract the time.
[02:35] I hope this makes sense to you.
[02:36] Now let me show you the demo of art related methods to show you the demo of the at related methods.
[02:43] First, let me create the object of LocalDate with the variable name as localDate and on the right
[02:50] hand side with the help of of() method, I'm going to pass the year as 2015, month as three and date
[02:58] as 18.
[02:59] Now using these objects, if I try to invoke at related methods, I have various options like the very
[03:05] first one is atStartOfDay().
[03:07] So if you try to invoke the atStartOfDay() using the LocalDate object, it is going to return
[03:13] me the object of LocalDateTime with the midnight time.
[03:17] Because this method, it is going to move your day to the starting of the day, which is midnight time.
[03:23] So that's what it is mentioned inside these documentation as well.
[03:26] So let me confirm the same by catching the output on the left hand side with the data type as
[03:33] LocalDateTime and the variable name as startOfDay.
[03:37] So if I try to print out these startOf Day variable, you'll be able to see that I have both the
[03:43] date and time information, but time information we will be having with the 0000 indicating the midnight
[03:51] of the day, which is March 18th.
[03:54] In the similar lines, you also have a method which is atTime() which is going to help you to add time
[04:00] to your Date object based upon that time details that you are trying to provide.
[04:05] So here I'll try to provide the hour details as 18 and minutes details as 20.
[04:10] On the right hand side, I can try to catch the output with the help of LocalDate time and the variable
[04:15] name as localDateTime.
[04:17] And if I try to print out these localDateTime object, this time you'll be able to see inside the
[04:23] output that these date is going to present and to this date.
[04:27] This time is also going to be added in the new object that you are trying to create.
[04:31] So we can't add the time to the same object, because once this object is created, it is immutable
[04:37] in nature.
[04:38] So let me execute this program and you can see we are getting the date and time and the time we have
[04:44] 1820.
[04:45] I hope you are clear.
[04:46] With the help of at related methods as well, we can create the new objects from the existing objects.
[04:53] With that you may have a question which is then what's the difference between with() method and at() method.
[04:58] Even with() method
[05:00] also giving you the new objects from the existing objects by allowing you to change some data like year,
[05:07] month, date and time.
[05:09] The difference is very clear.
[05:10] With the help of with related methods, you can only convert a local date time or a local date or a
[05:17] local time into the same type of object.
[05:21] So here I have a LocalDateTime object.
[05:23] If I use this with the methods, I'm going to get the output as only local date time only.
[05:28] The same applies if you try to invoke this with related methods with the LocalDate object.
[05:33] If you are using LocalDate object, then the output also is going to be LocalDate and the same rule
[05:38] applies for other data types as well.
[05:39] But coming to the at related methods, you're going to get other type of objects as well.
[05:45] So here with the help of LocalDate, I'm trying to invoke the at method.
[05:49] And from this at() method I'm getting an object of other data type which is LocalDateTime.
[05:54] So if you are trying to create an new object which belongs to the same data type, then you can happily
[06:01] use this with related method.
[06:02] Otherwise, if you are looking for a option to completely create a different data type objects, then
[06:08] you can happily use the at related methods.
[06:10] I hope you are clear with all the discussion that we have done.
[06:13] As usual, everything that we discussed inside this lecture I have mentioned in this slide for your
[06:18] reference.
[06:19] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
