# 23.17 — [JAVA 8] Demo of Instant and Duration in java.time Date and Time API

> Section 23: Date and Time in Java

[00:00] Inside this lecture.
[00:01] Let's see the demo on how to use instant and duration classes to show you the demo, I'm going to create
[00:08] a new Java class with the name Instant Demo.
[00:13] Inside this class.
[00:13] First I'm going to create a main method and inside this main method let me type instant class name which
[00:21] is instant itself.
[00:23] Post that I'm going to give the variable name as i1, followed by.
[00:28] I'm going to mention the class name of instant, and after this we can try to invoke one of the method
[00:35] which is of epoch second.
[00:37] So using this half epoch second, we can pass a number of seconds as an input.
[00:42] So if I try to pass 1000 as an input to this method, it is going to give me the time after thousand
[00:50] seconds from the Unix epoch time.
[00:52] That's why if I try to print out this i1, we're going to get the output as 1970 John one.
[01:00] But the time you can see it is 16 minutes 40s.
[01:06] So always use this method of epoch.
[01:08] Second, whenever you want to get a instant from the Unix epoch time by passing the number of seconds
[01:15] as an input.
[01:16] But if you are looking to get the current instant value, you can simply use the now method like we
[01:23] used in the case of Localdate Localdatetime and the zone datetime classes.
[01:28] So after this.
[01:29] Now let me type semicolon and on the left hand side I'll try to catch the output with the help of a
[01:34] variable i2.
[01:36] So if I try to print out these i2, you'll be able to see the current date and time value.
[01:43] So this is the current date and time value this object.
[01:46] It is going to store the date and time with the help of nanoseconds from the epoch time.
[01:52] But when we try to print out this, it is going to display the date and time value in an easily understandable
[01:58] format.
[01:59] So how this is achieved?
[02:00] This is achieved with the help of two string method available inside the instant class.
[02:06] So this two string method is.
[02:07] Overridden.
[02:08] So you can see this two string method which is inherited from the object superclass.
[02:12] It is overrided with a logic where they are trying to format the date and time with the help of this
[02:18] format, which is ISO instant.
[02:20] As a next step, I'm going to create the local DateTime object with a variable name as local date,
[02:27] time and post that I'm going to invoke the now method.
[02:31] So what I'm going to do is I'll keep a breakpoint here, and I'll try to execute this program.
[02:36] And in the debug window you'll be able to see the objects related to the local date, time and the instant.
[02:42] If you try to visualize how these instance is trying to store the date information, you'll be able
[02:48] to see it is storing the seconds and nanoseconds.
[02:52] Similarly, inside this i2.
[02:53] Also, you'll be able to see how many seconds it is passed Unix epoch time and what is a nanosecond
[03:00] when this object is created.
[03:02] But if you try to look into the local DateTime object.
[03:06] You can see it is represented with the help of year, month, day and inside the time we have hour,
[03:12] minute, second and nanosecond.
[03:14] So with this, I'm assuming you are clear about how these instant objects and local datetime objects
[03:20] they are going to store date and time values internally.
[03:23] So let me release this breakpoint.
[03:25] As of now, when we are trying to print out these I to object.
[03:28] We are getting that date and time values in an easily understandable format.
[03:33] But if you are looking to understand the number of seconds passed from the epoch time based upon a given
[03:39] I to instance object, you can simply invoke the method which is get epoch.
[03:45] Second, this get epoch second method, it is going to give you the number of seconds using this long
[03:50] data type.
[03:51] That's why on the left hand side let me type long followed by seconds.
[03:56] So these seconds I can try to print out with the help of System.out.println.
[04:01] Similarly, if you are interested about the nanoseconds in a particular instant object, you can easily
[04:08] get that nanoseconds information with the help of get nano method.
[04:12] So if you open this get Nano method, you'll be able to see the documentation which says get the number
[04:18] of nanoseconds.
[04:19] Don't be under the assumption that it is going to give you the number of nanoseconds from the Unix epoch
[04:26] time, it is not going to give that nanoseconds.
[04:28] Instead, when you are instance object, it is going to be created with the help of now method.
[04:33] In that particular second, your object might have created under a particular nanosecond time frame,
[04:40] so that nanosecond values you can get with the help of these get nano method the same.
[04:45] I can catch on the left hand side with the variable name as nano seconds.
[04:51] I can try to print out these nanoseconds with the help of the System.out.println.
[04:56] If I try to execute this program, you'll be able to see inside the console that these are the number
[05:01] of nanoseconds, and this is the number of seconds happened from the Unix epoch time.
[05:07] If you see these nanoseconds, it is same as this value, because from this instant object only, we
[05:13] are trying to derive the what is the number of nanoseconds inside a specific second.
[05:19] So your instant object, it is created in between 51 and 52 second and in between.
[05:25] The time is getting calculated with the help of these nanoseconds.
[05:29] If your business logic needs to consider up to nanosecond precision level, you can always use these
[05:35] get Nano method to get the nanosecond details.
[05:38] As a next step, we can try to understand about the duration class.
[05:42] Before I try to create the object of duration, let me delete this code related to the local date time.
[05:48] Now I'm going to type duration class and import the same from the package Java dot time.
[05:54] Using this class I can invoke many of the off method.
[05:58] For example, I can try to invoke the off days method and to this off days method I can provide an input
[06:05] which is five days.
[06:06] Post that on the left hand side, I can try to catch the output with the variable name as d1 of data
[06:12] type duration.
[06:13] In the similar lines, let me try to invoke the off minutes method to this minutes method.
[06:18] I'm going to pass the input as ten minutes.
[06:21] So with this I'm trying to create a duration of ten minutes.
[06:24] I'll explain you what I'm going to do with these duration objects in few minutes.
[06:29] As a next step, I'm also going to create next duration object with the help of off seconds method.
[06:35] To these off seconds method, I'm trying to pass the input as 30s, and here I want to highlight that
[06:41] using the positive numbers is not mandatory.
[06:43] You can also pass the negative numbers, for example to this default duration object.
[06:49] I'm trying to pass the negative seconds by mentioning the value as -13 if needed.
[06:55] You can also perform addition and subtraction of two different durations.
[06:59] For example, with the help of D3 object, I'm going to invoke the plus method to this plus method.
[07:05] I can either pass other duration object as an input.
[07:09] Ah, I can also invoke this plus this plus hours plus minutes plus nanos plus seconds method to add
[07:16] a respect to unit of value.
[07:17] For now, let me try to invoke this plus method to this plus method.
[07:21] I'm going to pass the input as default.
[07:23] So the output from this plus method I'm going to catch with the variable name as D5.
[07:28] So just like how we are trying to perform, plus we can also perform minus as well.
[07:33] So these are the minus related methods.
[07:35] So let me revert back to the plus.
[07:37] Now I'm going to run this method in a debug mode.
[07:40] And I'll show you what is present inside this d1, d2, d3, d4, d5 objects.
[07:45] So let me execute this program.
[07:46] And inside the debug window you'll be able to see there are five different duration objects.
[07:52] So the D1 which I have created by passing five days as an input.
[07:57] You can see all my days are converted into hours like one 20 hours.
[08:02] So there is a thumb rule.
[08:03] Anytime you are trying to create a duration object, it is always going to represent the duration with
[08:08] the help of hours, minutes, seconds and nanoseconds.
[08:12] You can also observe there is a prefix for all these duration values, which is PT.
[08:17] PT indicates period of time for the d2 object.
[08:21] You can see we have ten minutes.
[08:23] Similarly for D3 it is 30s.
[08:25] For D4 it is -13 seconds.
[08:28] But coming to the D5, which is an plus of d3 and d4, we are getting the output as 17 seconds.
[08:34] This way you can always create the duration objects, but the next question you may have here is what
[08:40] is the purpose of duration objects?
[08:41] Why should I create object with a particular duration?
[08:44] It's a great question.
[08:45] Let's try to understand the same the duration objects we can create to add a duration for a given instant
[08:52] object.
[08:52] For example, here we have created two different instant objects like i1 and i2.
[08:58] So here what I'm going to do is using the i1 object.
[09:02] I'm going to add that duration with the help of plus.
[09:06] And you can see to this plus method I can pass a Duration here.
[09:11] I'm trying to pass D1 as an duration, and the output I'm going to catch with a new variable with the
[09:18] name as A3.
[09:19] Similarly, just like how we're trying to perform addition, we can also perform subtraction with the
[09:24] help of minus method.
[09:26] So let me duplicate this line of code was that I'm going to rename this to i4.
[09:31] This time I'm going to use the i2 object.
[09:34] And using this i2 object I'm going to invoke the minus to this minus method.
[09:39] I'm going to pass the d2 as an duration input.
[09:42] So if you try to print out these i3 and i4, you will be able to see that the given duration time might
[09:49] have added or subtracted based upon whether we have invoked the plus or minus methods.
[09:54] So let me try to print out i4 as well.
[09:57] So I'm trying to execute this program and release this breakpoint.
[10:00] And this is my I1.
[10:02] To this i1 we have added five days duration.
[10:06] That's why the date is right now zero six.
[10:08] And to this next to i2 object we have subtracted ten minutes duration.
[10:13] That's why here you can see 1345.
[10:15] Whereas here we are able to see the time as 1355.
[10:18] I hope you are seeing the power of duration and instant.
[10:21] Apart from the methods that we have discussed so far, instant class, it also has methods to identify
[10:27] whether a particular instant is before or after the another instant object.
[10:32] Let me show you a demo to identify whether a given instant is before or after a another instant.
[10:39] Here I'm trying to use i3 as an instant object.
[10:43] Suppose that we can invoke.
[10:45] The method is after.
[10:47] To this we can pass other instant object as an input.
[10:50] So here I'm going to pass i4.
[10:53] So the output we're going to get in a boolean value.
[10:56] That's why I'm trying to catch the output with the help of is after variable.
[11:01] Similarly there is also a is before method which is going to help you to identify whether a given instant
[11:08] object is before the other instant object.
[11:11] So let me rename this variable name to ease before we know it belongs to 1970 year, whereas i4 belongs
[11:19] to current date and time.
[11:21] So for this definitely we should get the output as false, whereas for the ease before we should get
[11:27] the output as true.
[11:28] Let me execute this program and confirm whether we have false and true.
[11:32] Here you can see ease after has false and ease before has true.
[11:36] So this is working like we expect.
[11:38] Before I try to close this lecture, I want to show you a demo of important scenario.
[11:42] Whenever you are trying to deal with the instances, think like you have two instant objects and you
[11:48] want to identify what is the duration between those two instant objects.
[11:53] In real projects you will have these kind of scenarios.
[11:56] Maybe you want to understand how much time a particular task has been taken to complete.
[12:02] So at the starting of the task, you are going to create a current instant, and at the end of the task,
[12:08] you are going to calculate another current instant.
[12:11] You will try to identify the duration between them to identify how much time it has taken to complete
[12:17] the task, so the duration between two instances we can identify with the help of a between method available
[12:25] inside that duration class.
[12:26] To this method I can pass two different instances.
[12:30] For example, I can pass i1 as an first object, followed by i3 as a second object.
[12:38] We know i3.
[12:39] We derived by adding five days duration.
[12:41] That's why when we try to calculate the duration between these two instance objects, we should get
[12:46] the same five days as an output.
[12:48] So on the left hand side, let me catch the output with the help of duration object and the same I can
[12:54] try to print out onto the console.
[12:57] So if I try to execute this program, you can see we are getting the output 120 hours, which indicates
[13:02] five days.
[13:03] I hope you're clear.
[13:04] All the methods that we have discussed inside this lecture, I have mentioned them inside this slide
[13:09] as code snippets.
[13:10] Please refer the same for any questions.
[13:12] Thank you and I'll catch you in the next lecture by.

----------------------------------------
