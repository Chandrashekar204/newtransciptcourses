# 23.4 — Demo of java.util.Date - Part 1

> Section 23: Date and Time in Java

[00:01] Based upon our previous lecture discussion
[00:03] by this time, it should be pretty clear for you that new date time API is a lot better than Legacy
[00:09] date time API.
[00:10] And with that, you may have a question which is should I learn legacy date time API as well?
[00:15] If we already have a new and better date time API?
[00:20] It's a great question.
[00:20] Let me try to answer the same.
[00:22] The answer is of course, yes.
[00:24] You should learn the legacy date time API as well.
[00:27] The reason is legacy date time API has been around for more than 15 years, and when the new date time
[00:34] API released in Java 8, Java team, they did not remove the legacy date time API completely.
[00:40] Instead, they give an option to the developers.
[00:43] You can either use the Legacy Date-Time API or you can use a new Date-Time API.
[00:48] Even today, there are good amount of projects.
[00:51] They are still using the Legacy Date-Time API just because they started the development long back.
[00:56] And even when the new Date-Time is introduced, they are not bothered to upgrade themselves.
[01:02] The reason is very simple.
[01:03] The old Date-Time API is working for them.
[01:05] They got used to that.
[01:07] That's why they might be continuing the old Date-Time API
[01:11] even today.
[01:12] If you end up working in this kind of projects, obviously you should know how old Date-Time API works
[01:18] along with the new Date-Time API.
[01:20] When Java team introduced the new Date-Time API, they make sure that the legacy Date-Time classes have
[01:26] been retrofitted to work seamlessly by introducing new methods and classes.
[01:31] The thumb rule is very simple.
[01:33] If you are writing a new code from scratch, you can always give preference to the new Date-Time API
[01:39] classes.
[01:40] Whereas if you are going to work on a project where they are already using the Legacy Date-Time API,
[01:46] either you can continue to use them, or if you are looking to use a new features of new Date-Time API,
[01:52] what you can do is you can convert the legacy objects into the new Date-Time objects and post that you
[01:59] can happily use the new Date-Time API.
[02:01] I'll be showing you in the coming lectures how to convert your legacy objects into the new Date-Time
[02:07] API as well.
[02:08] I hope you are convinced with my inputs that you should also learn legacy Date-Time API.
[02:13] With that assumption, let's try to understand the very first important class that we have inside the
[02:20] Legacy Date-Time API, which is java.util.Date.
[02:24] Inside my IntelliJ, I'm going to create a new Java class with the name JavaUtilDate.
[02:32] So this is the class name inside this class.
[02:34] First, let me make sure to create the main() method post that I'm going to create a object of Date.
[02:41] You can see I'm trying to import the class present inside the java.util package, so please make sure
[02:46] you are importing the same.
[02:48] After this I can try to create a object variable with the name currentDate, followed by
[02:53] I'll just mention new Date().
[02:55] With this we know what is going to happen.
[02:57] We are going to get the current date.
[02:59] So let me mention in the comments as well currentDate and time value.
[03:04] So if I try to print out this as well, I'm going to get the output which is current date and time value.
[03:10] You'll be able to see the current date and time.
[03:13] Now let's try to understand what is happening behind the scenes when we try to create an object of this
[03:19] Date class.
[03:20] Here, I'm going to open these default constructor of Date class.
[03:24] Inside this default constructor, you can see first they are trying to invoke the current time in milliseconds
[03:30] which is available inside the System class.
[03:33] So inside System class we have a static method.
[03:36] And this static method is implemented with the native language.
[03:40] We don't have to worry about the logic written inside this, but what this method is going to do is
[03:45] it is going to return the time in milliseconds by considering the January 1st, 1970 UTC as the epoch
[03:54] time.
[03:55] So what is an epoch inside computer language?
[03:57] I can mention the same here inside the comments.
[04:00] In computing an epoch is a fixed date and time used as a reference from which a computer measures the
[04:08] system time.
[04:09] So this data class it is going to consider 1970 January 1st UTC as the first epoch time.
[04:18] So whenever you try to create an object of this class behind the scenes, it is going to calculate the
[04:24] number of milliseconds happened.
[04:26] From this reference point.
[04:28] We can also see how many milliseconds happened from the epoch time by invoking a method using your current
[04:34] date object.
[04:35] The method is getTime(), so get time is going to give you the time in milliseconds that are passed from
[04:43] the epoch time.
[04:44] So on the left hand side I can catch the output with the variable name time in milliseconds.
[04:50] So if I try to print out these time in milliseconds, we'll be able to see how many milliseconds completed
[04:57] from the epoch time, which is Jan first, 1970
[05:00] UTC.
[05:01] You can see this many milliseconds completed from the epoch time.
[05:06] If you are not passing any value to the default constructor, it is going to give you the current date
[05:10] and time.
[05:11] But sometimes you may want to create a date object with the specific date values.
[05:15] In such scenarios, you can always try to pass your day, year, month, and time values.
[05:23] For example, if I am trying to create a future date, I should be able to achieve that by passing values
[05:29] to the date constructor.
[05:31] So here I am going to mention 200 as the year followed by I am going to mention eight as the month,
[05:38] and at last I am going to mention 26.
[05:40] So if I try to print out this future date, I will be able to see the time and date stored inside this
[05:46] future date.
[05:47] So let me execute this.
[05:49] You can see the future date I am trying to create is from 2100.
[05:53] I can also copy the same and mention inside the comments.
[05:57] Now we can try to understand what is happening here.
[05:59] The year value we have mentioned as 200.
[06:02] Like we discussed previously, always the years start in 1900, in the legacy date time API.
[06:08] So to that 1900 we are trying to append 200.
[06:11] That's why we are getting the output as 2100.
[06:14] And since the month is always going to start at zero index for eight months, we are going to get September
[06:20] and the date we are trying to pass 26, the same we are seeing on the output as well.
[06:24] But coming to the time, since we have not mentioned any time value, we are getting the default midnight
[06:30] time with all zeros.
[06:31] So if I try to open this constructor, you will be able to see this constructor is deprecated.
[06:36] It is no more recommended.
[06:38] Instead, we should try to use the Calendar and the GregorianCalendar objects, which we are going
[06:44] to discuss in the coming lectures.
[06:46] Apart from these constructor, there are other constructors also inside this date class which are going
[06:51] to accept time in hours minutes as well.
[06:54] If you want to send even seconds as well, there is one more constructor, but all these constructors,
[06:59] they are deprecated in the favor of calendar related classes.
[07:03] So let me show you how to pass that time as well.
[07:05] So what I'm going to do is I'll mention time as eight, followed by 15 minutes, followed by 39 seconds.
[07:14] This time
[07:14] if I try to print out these date time value, you can see I'm getting the output based upon the date
[07:21] and time that I have provided.
[07:22] This way, you can always use these Date class to create the current date or future date or past date,
[07:29] but in order to create those objects, you need to know about all the rules that we have discussed.
[07:34] What kind of numbers you need to pass.
[07:36] I hope this makes sense to you.
[07:37] We need to discuss more about this date class.
[07:39] Let's continue this discussion in the next lecture as well.
[07:43] Thank you,
[07:43] bye.

----------------------------------------
