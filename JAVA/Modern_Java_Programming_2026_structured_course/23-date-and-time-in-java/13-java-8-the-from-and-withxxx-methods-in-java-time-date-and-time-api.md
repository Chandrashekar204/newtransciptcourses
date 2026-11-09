# 23.13 — [JAVA 8] The from() & withXxx() methods in java.time Date and Time API

> Section 23: Date and Time in Java

[00:00] Just like how we have of() related methods, we also have from and with related methods as well inside
[00:07] the new Date-Time API.
[00:09] Let's try to understand the purpose of these methods and how to use them.
[00:13] I'm going to create a new Java class inside the newapi package.
[00:18] The class name I'm going to mention as FromAndWithMethodsDemo inside this class.
[00:25] First we need to create the main() method, followed by
[00:29] first I'm going to create the object of LocalDateTime and to this of() method I'm going to pass the
[00:35] year as 2015, followed by month as March.
[00:39] I'm going to pass after the month, I'm going to pass the day as 18 followed by hours
[00:45] I'll pass as 22, followed by minutes
[00:47] I'm going to pass as 30.
[00:49] So with this we have successfully created the object of LocalDateTime with the given values.
[00:55] So if I try to print out these objects, we'll be able to see the date and time details that we have
[01:01] provided.
[01:02] You can see the same details are present inside the console.
[01:05] Now let me show you the purpose of from() method.
[01:08] Whenever you have a requirement to extract only the date values from these LocalDateTime, or if you
[01:14] want to extract only the time component from this LocalDateTime object, you can use the from() method.
[01:21] For example, think like
[01:22] I'm looking to extract only the date information from this LocalDateTime object.
[01:27] In this kind of scenarios
[01:28] first I need to type the class name LocalDate which represents only the date component.
[01:34] Using this method, I need to invoke the static method from() to this
[01:38] from() method I need to pass the object which is DateTime object which I have created above.
[01:43] Post that on the left hand side
[01:45] I'm going to accept the output with the LocalDate as an data type, and the variable name I'll mention
[01:51] as derived date.
[01:52] Similarly, we can also extract only that time component as well, but to extract that time component,
[01:59] we need to use the LocalTime class to invoke the from() method and to this from() method, we can pass
[02:05] the DateTime object.
[02:06] The output from this code will be an object of LocalTime.
[02:09] That's why on the left hand side, I need to type LocalTime with the variable name as derivedTime.
[02:16] So if I try to print out these information onto the console, I'll be able to see the date and time
[02:23] values separately since we extracted into the separate object components.
[02:28] So let me execute this program.
[02:30] You can see I'm getting the output.
[02:32] But the second statement it is printing that time value.
[02:36] Let me see what's a problem.
[02:38] Here I have used the invalid variable name.
[02:40] It should be derivedDate.
[02:42] So with this we should be good.
[02:43] Let me execute the program.
[02:45] You can see first we have only date information followed by only time information.
[02:49] So whenever you have a requirement to partially extract the data from an DateTime object or from a
[02:55] ZonedDateTime object, in all those scenarios, you can happily use this from() method available inside
[03:01] various classes of new Date-Time API.
[03:03] Now let me show you the purpose of with methods.
[03:07] We know by default all the objects that we are going to create with the help of new Date-Time API.
[03:12] They are going to be immutable by nature.
[03:15] We cannot change the content of these objects once the object is created, but many times we will have
[03:21] requirement to create the new objects from an existing object by partially changing some data.
[03:28] Off course, we cannot change the same object because these objects are immutable in nature, but there
[03:33] will be a common requirement inside your projects which which is change some content inside the existing
[03:39] objects and create a new object from the new content.
[03:43] So this can be a common requirement for all these kind of requirements
[03:47] you can use the with related methods. If there is some confusion
[03:51] don't worry
[03:51] when I show you the demo it is going to be super clear for you.
[03:54] So what I'm going to do is we already have this DateTime object inside the method using which we are
[04:00] trying to store this Date and Time information.
[04:02] Think like I want to create a new LocalDateTime object by just changing this year.
[04:08] So in those kind of scenarios you can use the with related methods.
[04:12] For example using these DateTime object I'm going to type with
[04:17] and with that you can see there are so many with related methods.
[04:20] For example, if I want to change the year, I need to select the with the year and I'm going to type
[04:26] the new year, which is 2030.
[04:29] With that, I'm going to get a new LocalDateTime object with the new updated content.
[04:35] So this object name I'm going to mention as dateTime1.
[04:39] So if you see here, with the help of this withYear() method, we are not changing the original object,
[04:44] which is dateTime.
[04:45] And of course we cannot change it as well since it is a immutable.
[04:48] Instead, we are leveraging the same data present inside the original object.
[04:51] On top of that, with the help of this withYear() method, we are trying to manipulate the year data
[04:57] and post that we are trying to create a new
[04:59] object.
[05:00] Similarly, you can try to change any of the content like month, minutes, seconds if needed
[05:05] you can change multiple content as well, like year end date.
[05:09] It's up to you what you want to change.
[05:11] I can also show you a demo around that.
[05:13] This time what I'm going to do is along with the year, I'm also going to change the month.
[05:18] So to change the month, I just have to type withMonth() and to this month I can pass the value as ten,
[05:27] so ten indicates October.
[05:28] So with this code, I'm going to get a new object of LocalDateTime with the variable name as
[05:34] dateTime2.
[05:35] So if I try to print out these two objects, which is dateTime1 and dateTime2, you'll be able
[05:41] to see the updated date and time.
[05:44] Here you can see 2030 March 18th.
[05:47] Whereas in the last statement we have 2030 October 18th which has updated year and month.
[05:54] So this way you can change any kind of content by invoking these with related methods.
[06:00] So this with related methods are available in all type of classes.
[06:04] As of now, I'm trying to show you the demo only with the object of LocalDateTime.
[06:09] But if you open this LocalDate here inside this class also, you should be able to find with related
[06:16] methods.
[06:17] The same applies for LocalTime as well.
[06:20] Any class you can open inside the new Date-Time API.
[06:24] You will be able to find some with related methods.
[06:27] So using these with related methods, we can create new objects from the existing objects.
[06:34] And these with methods are very useful because we know the objects that we are going to create with
[06:39] the classes of new Date-Time API, they are going to be immutable whenever you want to copy the data,
[06:45] with a few modifications from the existing objects, you can happily use these with the related methods,
[06:51] and they are going to provide you the new objects with the updated date and time values.
[06:56] I hope you are clear with the from and with related methods.
[07:00] Whatever we have discussed inside this lecture I have mentioned in this slide for your reference.
[07:05] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
