# 23.22 — [JAVA 8] Demo of ZoneOffset

> Section 23: Date and Time in Java

[00:00] Just like how we have journeyed inside the new Date-Time API.
[00:03] We also have a class with the name ZonedOffset.
[00:07] Before we try to understand more details about this ZoneOffset, first let me explain you about what
[00:12] is offset and how it is different from time zone.
[00:16] To know more details about the offset, I came to the browser and inside Google
[00:20] I'll try to search for a keyword which is List of UTC offsets.
[00:26] So if you search for these keyword, you'll get a Wikipedia page in the search results with the title
[00:32] list of UTC offsets.
[00:33] Please click on that.
[00:35] And with that, this page is going to open.
[00:38] Here on the left hand side, you'll be able to see there are multiple UTC along with their offset.
[00:43] So basically offset is a number.
[00:46] It can be a negative number or a positive number.
[00:48] First I want you to click on these UTC zero offset.
[00:52] So what scientists have done is they tried to divide the whole world date and time by taking the center
[00:58] of the Earth as UTC.
[00:59] So what is UTC?
[01:01] If you go to the top of the page, there is a definition for UTC.
[01:04] UTC means Coordinated Universal Time.
[01:08] This UTC is marked at the center of the Earth with the UTC zero offset, and this offset all these countries
[01:15] like Denmark, Iceland, Ireland, United Kingdom, Portugal, Senegal.
[01:21] So all these countries are covered.
[01:23] And you can also see these are the important cities covered under this offset.
[01:27] So London, Dublin
[01:29] and similarly there are other cities as well. From this UTC zero offset
[01:33] if you try to move one hour that will be called as UTC+1.
[01:38] So under this other countries and other cities are covered like Berlin, Rome, Paris, Madrid.
[01:44] For India
[01:45] I can click on this 5:30 UTC.
[01:48] So under this you can see India and Sri Lanka are covered with the major cities like Mumbai and Colombo.
[01:54] Whereas for the UTC 5:45, Nepal is covered. This way with the help of offsets
[01:59] also, we can represent date and time across various countries and cities.
[02:04] With that, you may have a question which is then what is the difference between time zone and offset?
[02:09] Time zone is going to represent a specific region, whereas offset is going to represent a number.
[02:15] Under this offset, multiple time zones also can present, and there is also a possibility in a single
[02:21] time zone we may have multiple offsets as well.
[02:24] So basically there are two approaches to represent date and time throughout the world.
[02:28] The very first approach is with the help of time zone.
[02:31] And the other one is with the help of UTC offset.
[02:34] I'm assuming you have idea to which offset your country belongs.
[02:38] I want you to open the corresponding offset inside this page, and confirm whether your country and
[02:43] city comes under a specific offset.
[02:46] Now I'm thinking you have a clarity around offset.
[02:49] As a next step, let's try to understand about the ZonedOffset.
[02:52] With the help of ZoneId we can represent the time zones like Asia, Kolkata, America, Chicago.
[02:58] In the similar lines, if we want to represent a date and time with the help of offset, you can use
[03:04] the class which is ZoneOffset.
[03:06] So ZoneOffset it is going to represent a fixed offset time from the UTC.
[03:11] Typically, this ZoneOffset is used in the cases where a specific time zone is not required.
[03:17] It is defined by an offset in hours and minutes such as plus two minus five.
[03:23] We should be able to create the ZonedDateTime objects with the help of ZoneOffset as well.
[03:29] First, we need to create the objects of ZoneOffset by invoking these ofHours() method to these ofHours()
[03:35] method
[03:36] if you are passing that two as an input, then it is going to represent UTC plus zero two offset time.
[03:42] So these are very first object that I have created.
[03:44] Later on I'm trying to create a DestinationOffset with the offset number as -8.
[03:50] So these two represent two different offsets, which means they are representing two different time
[03:54] zones.
[03:55] Now by passing these offset objects, I should be able to create the ZonedDateTime object.
[04:01] So here you can see to the now() method.
[04:03] I'm trying to first pass the offset object, which belongs to the plus two offset.
[04:07] Later on using this date variable, I'm trying to find the equivalent time in the offset -8.
[04:15] We need to invoke the same method which is with the zone same instant, and to this we need to pass
[04:20] the DestinationOffset as an input.
[04:23] With that, we are going to get a date and time value on the left hand side, which is an equivalent
[04:28] time that we passed for the UTC -8 offset.
[04:31] This should give a clarity to you that we should be able to use ZonedDateTime, both with the ZoneId
[04:37] and the ZoneOffset.
[04:39] If you ask me under which scenarios you want to go with the ZoneId or ZoneOffset, the answer is very
[04:44] similar.
[04:44] If you are looking for an option to display the time in a more user friendly format along with the region
[04:50] name, then in that scenario you can go with the ZoneId otherwise, if you are looking to display the
[04:54] time with the help of offset, you can always go with the ZoneOffset.
[04:58] Let me show you that demo.
[04:59] More of this ZoneOffset.
[05:01] And we can also try to integrate the same to the ZonedDateTime.
[05:05] We already have a class with the name ZonedDateTimeDemo.
[05:08] Inside this class I'm going to create the ZoneOffset objects by typing the ZoneOffset class name followed
[05:15] by variable name.
[05:16] I'll just give as offset and on the right hand side
[05:20] with the help of ZoneOffset, I'm going to invoke the ofHours() method to this ofHours() method
[05:27] I'm going to pass UTC offset as two.
[05:30] If you are trying to represent an offset which has both hour and minutes like 5:30, like in the case
[05:36] of India, the offset number is 5:30.
[05:39] For all such scenarios, instead of invoking the ofHours(), you can try to invoke ofHoursMinute(),
[05:45] which is going to accept hours and minutes.
[05:48] Like you can see
[05:49] this is how you can pass like five comma 30.
[05:51] For now, let me go with the offHours() method to create a zoneOffset() object, which represents the
[05:58] UTC plus two offset.
[06:00] Similarly, I'll try to create one more offset object with the variable name as distOffset.
[06:06] And to this I'm going to pass the offset as -8.
[06:10] For that, I'm going to copy these lines of code and paste it here.
[06:14] I'll try to change this name to utc2DateTime.
[06:19] Similarly, I'll try to change this variable name to utcDistDateTime, so I can mention -8
[06:27] inside the variable name.
[06:28] That's why I'm trying to give this name here.
[06:29] The same I'll try to print out with the help of this .
[06:32] System.out.println() statements.
[06:34] Before I try to execute this program, I need to make sure I'm passing the object of ZoneOffset.
[06:39] That's why I'll try to pass this offset object as an input to this now() method.
[06:44] Similarly, I'll also pass distOffset object.
[06:48] So if I execute this program, you can see right now the time in the plus two offset is 10:34.
[06:55] But coming to the UTC minus eight offset the time is midnight 12:34 a.m..
[07:01] I'm also assuming you're also seeing the differences between the ZonedDateTime that we have created
[07:05] with the help of ZoneId and ZoneOffset.
[07:08] In the case of ZoneOffset, your date and time is going to have only the offset details, whereas in
[07:14] the case of ZoneDateTime objects that you have created with the help of ZoneId along with the offset,
[07:19] they are also going to have time zone details like for Asia and Kolkata the offset is 5:30, whereas
[07:25] for America Chicago the offset is -6.
[07:29] I hope you are clear with the purpose of ZoneOffset class and how to integrate it.
[07:34] While we are trying to build the ZonedDateTime objects.
[07:37] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
