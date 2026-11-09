# 23.21 — [JAVA 8] Demo of ZoneId, ZonedDateTime

> Section 23: Date and Time in Java

[00:00] Inside new Date-Time API
[00:02] there are good amount of classes which are going to help us to build the Date and Time objects, along
[00:08] with the complexities of time zones
[00:10] daylight savings.
[00:11] Inside this lecture, let's try to understand all those classes one by one.
[00:15] The very first class I want to talk about is ZoneId, ZoneId is a class inside the new Date-Time API,
[00:22] which represents a specific time zone.
[00:25] By passing this ZoneId as an input to the constructor of the ZonedDateTime class, we should be able
[00:31] to create the date and time based upon a given time zone.
[00:34] Here you may have a question which is how do I know
[00:37] what are all the zone ID supported by the new Date-Time API?
[00:41] It's very simple, like you can see here
[00:43] inside the ZoneId class we have a static method with the name getAvailableZoneIds().
[00:49] This method is going to give you all the supported time zones by the new Date-Time API, in the form
[00:56] of Set.
[00:56] If you try to print out the content of this Set, you'll be able to see all the supported time zones
[01:02] by the new Date-Time API.
[01:04] We'll also see this in demo in few minutes.
[01:07] The next question you may have is how can I create the ZoneId object by passing a specific zone as
[01:13] an input.
[01:14] It is also very simple
[01:15] You can use the of() method available inside the ZoneId class, and to this off method you can pass
[01:22] your ZoneId here.
[01:23] I'm trying to pass a zone which is Asia/Kolkata.
[01:27] So this zone is specific to the India country.
[01:30] Similarly, I'm also trying to create another ZoneId object with the zone details as America/Chicago,
[01:37] For the first zone, I'm trying to create the variable name as zone, whereas the second zone
[01:42] I'm trying to create the variable name as destinationZone.
[01:46] So think like I have a requirement to identify what is the equivalent time in another time zone based
[01:54] upon my current time zone.
[01:55] So to handle these kind of scenarios, first you need to create the object of CurrentZone and the
[02:01] DestinationZone.
[02:01] So that's why here I'm trying to create two different zone ID objects.
[02:05] Later on these ZoneId objects, you can pass as an input to the ZonedDateTime clas.
[02:10] Here like you can see when I'm trying to invoke the now() method with the help of ZonedDateTime, I'm trying
[02:15] to pass the Zone object, which belongs to the Asia/Kolkata.
[02:20] With that this date variable, it is going to hold the current date and time in the Asia Kolkata time
[02:27] zone.
[02:27] If I want to know what is the equivalent time in another time zone, what I have to do is using the
[02:33] same Date object
[02:35] I need to invoke a method which is withZoneSameInstant(), and to this method I need to pass that
[02:42] DestinationZone object.
[02:43] Here we are trying to pass the America Chicago as a DestinationTimeZone object.
[02:49] With that, I'm going to get the object of ZonedDateTime as an output and this destDate object,
[02:54] it is going to have the equivalent time inside the America/Chicago time zone.
[02:59] So this is how you can create always zone specific time with the help of ZonedDateTime and ZoneId
[03:07] ZoneDateTime is also going to handle the daylight saving complexities behind the scenes.
[03:12] Let's see the demo of this ZoneId and ZonedDateTime
[03:15] by going into the intelliJ. Inside my intelliJ, I'm going to create a new Java class with the
[03:21] name ZoneIdListDemo.
[03:25] So first I'll show you how to get the list of zone ID supported by the new Date-Time API.
[03:31] Here, let me create the main() method.
[03:32] Post that with the help of ZoneId class, I'm going to invoke the static method which is getAvailable
[03:40] getAvailableZoneIds().
[03:40] So the output from this method is going to be a Set.
[03:43] So that's why on the left hand side I'm trying to catch the output with the help of Set of String and
[03:50] with the variable name as all zones.
[03:52] After this line of code, I can try to print out all the zones with the help of for each block.
[03:58] So first let me try to create a temporary variable with the name ZoneId, followed by
[04:04] I'm going to mention all zones, which is the set in my case.
[04:07] After creating these for each block inside these for each block, I'll try to print out the zone ID
[04:14] details.
[04:14] So if I execute this program you will be able to see these are all the zones supported by the new
[04:21] Date-Time API.
[04:21] So anytime
[04:22] if you are looking for a specific time zone, what is the equivalent valid value?
[04:27] Don't stress yourself.
[04:28] You can simply use the method which is available inside the ZoneId to get the details of all the supported
[04:34] zones and post that you can try to search for your specific time zone details.
[04:38] Now let's see that demo of ZonedDateTime class.
[04:43] For the same, I'm going to create a new Java class with the name ZonedDateTimeDemo.
[04:49] Inside this class
[04:50] first we need to create the main() method post that I'm going to first create that ZoneId objects by
[04:56] providing some time zone details.
[04:58] The very first zone that
[04:59] I am going to create is related to the India.
[05:02] At the same, I need to invoke the of() method available inside the ZoneId. And to this of() method
[05:09] I'm going to type Asia/Kolkata.
[05:12] So Kolkata is a city inside India.
[05:15] So this is the time zone value that you need to use whenever you want to get an Indian time.
[05:20] Similarly, I'm going to create one more ZoneId object with the variable name as destinationZone.
[05:26] And to this I'm going to mention America/Chicago post that I'm going to create the object of
[05:34] ZonedDateTime with the variable name as IndiaDateTime.
[05:39] And on the right hand side, I'll try to invoke the now() method with the help of ZonedDateTime.
[05:45] So to this now() method you need to pass what is the zone ID that it has to consider?
[05:50] Since I want to consider Asia Kolkata zone, I need to pass the object with the name zone. Later on
[05:55] if I'm looking for the equivalent time of this India time in another time zone, I need to use the same
[06:01] indiaDateTime object and with the same I need to invoke the method which is with the zone same instance.
[06:08] And to this method I need to pass the destinationZone object which is related to
[06:15] America/Chicago. On the left hand side
[06:17] let me catch the output with the variable name as chicagoDateTime.
[06:22] At last I'll try to print out both these time details like
[06:26] first I'll try to print out IndiaDateTime, followed by I'll try to print out chicagoDateTime.
[06:32] If I execute this program, you will be able to see that right now, the time in Asia is 12:42.
[06:39] And these are the date details.
[06:40] And this is the zone details along with that time zone details.
[06:44] You can also see the offset details. India stays at the offset 530 the same
[06:50] we can also see here.
[06:51] If you're not clear about what is offset I'm going to discuss in the next lecture.
[06:55] Now if you try to observe the second date and time, this is the equivalent date and time in Chicago.
[07:01] So right now the time in India is 12:42.
[07:04] But the time in Chicago is midnight 1 to 12, and it is present at the offset of minus six.
[07:13] So this is how you can always leverage the zone ID and zone date time to create the date and times specific
[07:20] to a time zone.
[07:21] Inside real time projects, you will have lot many scenarios around the scheduling.
[07:26] For example, if you take the airline scheduling in all those scenarios, you need to handle the time
[07:31] zones.
[07:32] Maybe the person might be flying from India to USA.
[07:36] If you want to give clear instructions to the end user, like at what Indian time his flight is going
[07:42] to take off and at what Chicago time his flight is going to land.
[07:47] So all those details, if you want to provide inside the ticket or inside the email or inside an SMS
[07:53] for all those kind of scenarios, you can happily use the ZonedDateTime along with that ZoneId objects.
[07:59] I hope you are clear about that ZoneId and ZonedDateTime classes.
[08:03] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
