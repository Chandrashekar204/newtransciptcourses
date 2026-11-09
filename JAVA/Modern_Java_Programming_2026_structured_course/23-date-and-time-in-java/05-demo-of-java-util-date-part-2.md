# 23.5 — Demo of java.util.Date - Part 2

> Section 23: Date and Time in Java

[00:01] As of now, we are creating the Date object by using the default constructor or by passing the date
[00:08] and time values.
[00:09] There is one more approach that we can leverage, which is by passing the time in milliseconds to the
[00:14] constructor.
[00:15] Let me show you the demo of the same.
[00:17] We know each and every Date object.
[00:20] It is going to be represented by the time in milliseconds from this epoch time.
[00:24] So for this date, which is 2100 September 26th, we can get the time in milliseconds.
[00:31] So how to get that?
[00:32] It's very simple.
[00:33] We just have to invoke the getTime() method.
[00:36] I'll try to assign these getTime() on the left hand side to a variable, which is time in millisecond
[00:44] one.
[00:44] Since we already have a same variable here, I'm trying to mention one here.
[00:48] Now I'll try to print out these time in milliseconds, so that we can see what is the time that we have.
[00:55] You can see this is the time in milliseconds.
[00:57] Now using this value I'm going to create the object of Date.
[01:01] So let me show you how to do that.
[01:03] For the same I'm going to create the object of Date with the variable name as date is equal to new Date().
[01:10] And to this constructor,
[01:12] I'm going to pass this time in millisecond one as an input to this, I'm also going to add few more
[01:18] milliseconds, which is 86 400000.
[01:24] So what is this number represents?
[01:26] This number represents 24 hours in milliseconds.
[01:30] So if you try to convert your 24 hours into the milliseconds, this is the number that we are going
[01:35] to get.
[01:35] So basically what I'm trying to do is I'm trying to append the one day time to this milliseconds.
[01:42] If you try to print out this Date object, we should get the immediate date of the September 26th.
[01:47] So let me try to print out the same onto the console.
[01:51] We should be able to see that the date is September 27th, because we have added 24 hours to the previous
[01:59] date, which is September 26th remaining.
[02:02] All the details are same like year, time, month.
[02:05] Everything is same, only the date is incremented by one day.
[02:08] So this is how you can also create an Date object by passing the time in milliseconds to the constructor.
[02:14] You can see this is the constructor which is going to be invoked behind the scenes.
[02:18] The next common requirement that you may have around the dates is you may want to compare your dates.
[02:24] In this kind of scenarios, you may want to compare them to understand whether it is a future date or
[02:29] whether it is a past date for these kind of comparison scenarios
[02:32] also, there are methods inside the Date class.
[02:35] So what I'm going to do is I'm going to take this future Date object.
[02:39] And using this I'm going to invoke the instance method which is after().
[02:43] So to this after() method I'm going to pass the other Date object which is date.
[02:49] The output from this method is going to be a boolean value.
[02:52] I'll assign a variable name which is uays after and the same I'll try to print out with the help of
[02:58] System.out.println().
[02:59] So if I execute this, obviously we are going to get the output as false because this future date is
[03:05] not after the given date.
[03:06] In fact, these date is one day after the future date.
[03:10] That's why we are getting the output as false.
[03:12] Whereas if I try to reverse this Date object like using the date, I'm trying to invoke the after() method.
[03:17] And to this after() method, I'm going to pass the future date as an input.
[03:22] In this scenario, you're going to get the output as true, just like after
[03:26] we also have before() method as well. So feel free to use based upon your business requirements.
[03:32] For now I'm going to keep the code off after for your reference.
[03:36] The next demo that I want to show around the date is how to modify the date.
[03:41] We know the legacy Date-Time APIs
[03:43] they are mutable in nature.
[03:44] That means once the object of Date is created, we should be able to change the year, date, or any
[03:51] other kind of information, though it is not recommended to change the values once the object is created.
[03:56] Sometimes you may have some peculiar business requirements which you may need to handle, but those
[04:02] kind of scenarios you can invoke various methods available inside the Date class to change a year,
[04:08] month date, or time value.
[04:10] Let me show you how to do that here
[04:12] you can see with the help of this currentDate, I'm able to get the current date value. But once this
[04:17] currentDate value is created, I will be able to change the year by invoking the setYear() method to
[04:26] this setYear() method I can pass any year.
[04:29] For example, if I try to pass 200, the currentDate value is going to be moved to that 2100.
[04:37] So let me execute the same and you'll be able to see that the currentDate value is moved to the 2100.
[04:44] Similarly, we should be able to change the date by invoking the setDate() method.
[04:50] In the same lines, we can invoke the setHour(), setMonth(), setMinute(), setSeconds().
[04:54] We can also invoke the set time by passing the time in milliseconds.
[04:59] So please use all these methods.
[05:01] Whenever you want to mutate your Date object with the new content.
[05:05] But like I said, this is not recommended approach.
[05:07] And in fact, all these methods are also deprecated.
[05:11] For example, if you go and open these setYear() present inside the Date class, you'll be able to see
[05:16] there is a annotation deprecated.
[05:18] Instead, they are asking us to use the Calendar.
[05:21] So we're going to discuss about Calendar class in the coming lectures.
[05:25] So this is how you can change that date time values whenever you are using the java.util.Date
[05:31] class to store the date and time values.
[05:34] I hope you are clear with all the discussion that we have done inside this lecture.
[05:38] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
