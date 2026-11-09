# 23.8 — Demo of java.util.Calendar - Part 1

> Section 23: Date and Time in Java

[00:00] To overcome the few of the drawbacks of java.util.Date Java team, they introduced a new set of classes
[00:08] with the name Calendar.
[00:10] If you can try to search for calendar, there is a abstract class in the java.util package.
[00:15] So this is an abstract class like you can see here.
[00:18] And this class is implemented by another concrete class which is GregorianCalendar.
[00:23] So let me open the same.
[00:25] And this GregorianCalendar also present inside the java.util package.
[00:30] Let's try to read the documentation of this class, so that you will know why this name is chosen for
[00:35] this class name.
[00:36] So what is a Gregorian?
[00:37] So that can be your question if you try to read the second paragraph they highlighted.
[00:41] GregorianCalendar is a hybrid calendar that supports by the Julian and GregorianCalendar systems.
[00:49] Throughout the world
[00:49] there are many calendars available.
[00:51] Few Arab based countries
[00:53] they follow the Islam calendar, and similarly Japan follows their own calendar,
[00:57] korean people
[00:58] they also follow their own calendar, but majority of the countries they follow the GregorianCalendar,
[01:04] which is a regular calendar.
[01:05] That's why Java team implemented a class with the name GregorianCalendar representing the most commonly
[01:13] used calendar.
[01:14] And with that you may have question which is how about the other type of calendars?
[01:17] Maybe I might be working for a Japan based company, or I might be working for a Arab based company.
[01:23] So for all these kind of situations, you might be scratching your head how to implement those country
[01:29] specific calendars.
[01:30] For now, don't worry, when we are discussing about the new Date-Time API, I'm going to show you how
[01:35] the new Date-Time API supports various kinds of calendars available throughout the world.
[01:40] For now, let's focus on these GregorianCalendar and try to understand how to create Date objects
[01:46] with the help of this calendar, let me open the Calendar.java class and there is a good amount
[01:51] of documentation around this class
[01:54] like you can see here.
[01:55] Whenever you want to create an Calendar object representing the current time.
[01:59] Since we can't create an abstract class object, we can leverage these get instance method to create
[02:05] the current time.
[02:06] We can also try this in the demo for the same
[02:09] what I'm going to do is, I'm going to create a new Java class with the name CalendarDemo.
[02:15] Inside this class
[02:17] first I'm going to create the main() method, and inside this main() method I'm going to type Calendar with
[02:23] the name as currentDate is equal to Calendar and post that I need to invoke the getInstance() method.
[02:31] So if I try to invoke this getInstance() method behind the scenes, it is going to create a Calendar
[02:37] object for me based upon the default time zone. Based upon from which country I'm trying to run this
[02:43] Java program
[02:44] accordingly, the time zone is going to be selected by my program.
[02:48] That's why if I try to print out these Calendar object, I will be able to see the current date time
[02:54] value based upon my current time zone.
[02:57] But to our surprise, you can see this is giving an object of GregorianCalendar and the same is being
[03:04] displayed.
[03:04] And it has lot many other details like from which time zone I'm trying to run this program.
[03:10] What is the total time in milliseconds?
[03:12] So this may not make sense to you.
[03:14] To get the actual date from these Calendar objects, what we can do is we can invoke the getTime() method.
[03:22] This getTime() method is going to give you an Date object.
[03:26] So let me type currentDate object as a variable name.
[03:31] Now I can try to print out this currentDateObj so that we will know what is the current date.
[03:37] So this is the current date I'm able to get from the Calendar instance.
[03:41] You might be thinking that using the calendar seems to be complex, because first you need to create
[03:47] the Calendar object from the Calendar object
[03:49] you need to get the Date object.
[03:51] So you might be thinking this is very complex and you may not like this Calendar, but believe me,
[03:56] once you started using the Calendar, there are many methods which is going to make your life easy.
[04:02] I'm going to show you demo of them in few minutes.
[04:05] For now, let's focus on the basic details around the Calendar object as a next step
[04:09] what I can do is, I will keep a breakpoint here, and I'll try to debug the program and I'll show you
[04:15] what is there inside these Calendar object.
[04:17] You can see there are a lot of information available around your date and time, whereas with the java.util.Date
[04:24] you'll have only the time and date information.
[04:27] But here we have many other details like if you can scroll here, you'll be able to see zone details
[04:33] like from which Joan this Calendar object is created.
[04:37] Since I ran this program from India, it is showing the zone ID as Asia/kolkata.
[04:43] So these kind of information we cannot populate inside the java.util.Date object.
[04:49] I hope this is making sense to you.
[04:50] Let me release the breakpoint.
[04:52] Just like how we are creating the Calendar object with the help of Calendar.getInstance()
[04:56] in the very similar lines, we can also create the object of
[05:00] GregorianCalendar directly.
[05:01] So here I'm trying to create an object of GregorianCalendar with the default constructor of
[05:08] GregorianCalendar().
[05:08] So now if I try to use the same GregorianCalendar variable to get the time, I'm going to get the same
[05:15] kind of behavior.
[05:16] So let me release this breakpoint
[05:17] you can see I'm able to see the current date and time value that I populated with the help of getter
[05:23] time method using the GregorianCalendar object.
[05:26] Now, as a next step, I'm going to show you one of the beautiful advantage of GregorianCalendar or
[05:31] Calendar system.
[05:32] Think like I'm trying to create a particular Date object.
[05:36] So for these kind of scenarios, what we can do is instead of invoking that default constructor of
[05:41] GregorianCalendar, I can directly pass the year which is 2100, whereas with the java.util.Date you have to
[05:48] do the calculations like from 1900, you need to add 200, the same 200 you need to mention here.
[05:54] So that drawback is overcomed inside the Calendar classes was that I can mention the month as zero followed
[06:01] by Date.
[06:02] So if I try to print these Date inside my console with the help of get time, you'll be able to see
[06:08] the date as January 1st is to 2100 year.
[06:13] Did you see the beauty we overcome these year?
[06:15] Related calculations?
[06:16] If people has a confusion around the month, since it is going to start from zero, what they can do
[06:22] is they can use a constants available inside the Calendar class.
[06:26] So instead of mentioning the 012, they can directly mention the month they are trying to refer.
[06:32] For example, for January I can mention the constant which is January itself.
[06:37] Behind the scenes it is going to hold the value zero.
[06:39] Similarly, for February 1st two, three, for all the remaining months, the constants are declared.
[06:44] So did you see
[06:45] we are able to overcome the month related drawback as well.
[06:49] So with this there won't be any confusion to the developers around the year calculations and the month
[06:55] number.
[06:55] So these are very first advantage of Calendar related classes.
[06:59] Once you have an object of GregorianCalendar, you can invoke many other methods supported by Calendar.
[07:05] Let me show you a demo of few of them.
[07:08] For example, using these GregorianCalendar object, I'm going to invoke the get() method.
[07:14] To this get() method we can pass a constant which is Calendar.YEAR.
[07:21] If you are looking to get an year, you need to pass Calendar.getYear() on the left hand side.
[07:27] Let me catch the output with the variable name as year.
[07:30] So let me try to repeat this code multiple times, this time instead of year
[07:36] if you try to invoke the constant month, you're going to get the month value inside your Calendar object.
[07:42] Similarly, I can use date constant to get the date inside my GregorianCalendar, and after that date,
[07:49] I can get the hour of the day.
[07:52] By using this constant hour of the day, and the output I'm going to get is hour, followed by I can
[07:59] invoke the minute constant to get the minutes details inside my Calendar object.
[08:06] Similarly, we can try to invoke the constants second to get the seconds details, and at last we also
[08:14] have a constant with the name milliseconds on the left hand side
[08:18] let me mention this constant name as milliseconds.
[08:22] You can see how easy it is to get multiple details from a single object, with the help of a same get
[08:29] method.
[08:30] This get method, it is going to accept a int value which represents which field you are trying to fetch.
[08:37] The same method is going to invoke regardless of which field you are trying to fetch.
[08:41] But inside that Date class which is present inside the java.util package.
[08:46] Inside this class, there are so many get related methods like getDate(), getDay(), getHour(),
[08:54] getMinutes(), getMonth(), getSeconds(), getYear().
[08:57] So all these methods, they are deprecated.
[08:59] Instead they are asking to leverage the calendar related Get methods.
[09:04] The reason is if you invoke these deprecated methods available inside the date, they'll have a logic
[09:09] which is specific to the each field, whereas inside the calendar they have a common logic which is
[09:15] going to be invoked behind the scenes regardless of which field you are trying to fetch.
[09:20] On top of that, inside the Date class, they are trying to perform some dirty calculations by subtracting
[09:25] from 1900, in the case of year.
[09:28] So these kind of dirty logics can be avoided if you try to use these get method available inside the
[09:35] Calendar class.
[09:35] As a next step, what I can do is, I can try to print out all these fields in any format that I would
[09:41] like, with the help of System.out.printf().
[09:44] Here I'm trying to paste a few lines of code.
[09:47] You can see I'm trying to invoke the printf() method, which is going to help me to performing the format
[09:52] of a given String.
[09:53] We discussed long back about the printf() method.
[09:56] I hope you remember to this printf() method I'm
[09:59] trying to pass a String with various placeholders, like at the very first placeholder, I'm trying
[10:05] to print the year value followed by month, date, hour, minutes, seconds, and milliseconds.
[10:11] So if I execute this program at the end, you'll be able to see the output current date and time in
[10:18] one, followed by time as all zero values.
[10:20] Just like how we have get() method, we also have set() method whenever we want to change a specific value
[10:27] inside your Date object, you can happily use a set() method.
[10:31] So let me show you how to do that.
[10:32] Think like I want to change the year value and the month value inside my GregorianCalendar object.
[10:38] As of now, we have the year as 2100 and the month as January.
[10:42] To change these values, what I can do is after the System.out.printf(), I'm going to first
[10:48] mention the GregorianCalendar object reference name, followed by
[10:51] I'm going to invoke the set() method.
[10:53] To this set() method, I'm going to first mention Calendar.YEAR and the value I'll try to mention
[11:00] as 2101.
[11:02] After this, I'll also try to change the month details by invoking Calendar.MONTH, followed by
[11:10] I'll set the value as Calendar.FEBRUARY.
[11:14] So now if you try to get the time from this Calendar object and try to print out on the console, you'll
[11:21] be able to see the latest year and the latest month that we tried to override with the help of set() method.
[11:27] So let me show you the demo as well.
[11:29] I will try to copy this line of code and paste it here towards the end.
[11:34] So with the help of this GregorianCalendar, I'm going to get the getTime().
[11:39] Post that I'll rename this to currentDate object one and the same
[11:42] I'm going to print out onto the console.
[11:44] So if I execute this program, you can see we are getting the date as February 1st in the year
[11:51] 2101.
[11:52] Did you see the beauty of Calendar?
[11:54] Regardless whether you are trying to fetch the data or set the data, you need to use the same method
[12:00] which is get and set based upon the parameters that you are trying to send to this method.
[12:05] Accordingly, they are going to execute the business logic behind the scenes.
[12:08] I hope you are clear with these initial introduction around the Calendar.
[12:12] Let's try to continue about the Calendar in the next lecture as well.
[12:16] Thank you,
[12:17] bye.

----------------------------------------
