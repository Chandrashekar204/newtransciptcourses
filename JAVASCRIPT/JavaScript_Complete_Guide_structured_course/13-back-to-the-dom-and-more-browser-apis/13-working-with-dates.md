# 13.13 — Working with Dates

> Section 13: Back to the DOM & More Browser APIs

Now to come to an end in this module, there's one last built-in or global constructor function you could say that helps you deal with dates and that's the date object and constructor function. You can use date in a broad variety of ways and attached you find documentation that allows you to have deeper into date. You can for example create a new date object like this and what this gives you if I hit enter is indeed the current date and timestamp here, so that's the current date and time at which I'm recording this specific video here, this is what you get with new date.

Now actually, this is really an object you can work with though. If we store it in a constant, then on this constant, so on this stored object, we get a couple of methods, for example we can call get date to get the day in month, 24th in this case, we got get day to get the day in this week and so on. So there are lots of methods that allow you to analyze this date, get the time for example since the beginning of time in Javascript land which is January 1st 1970, so since then, this is the time of milliseconds that has passed and this can sometimes be helpful for calculating differences and so on and much more, so there are a bunch of methods you can call to work with a date.

You can also construct a date with new date by passing an argument to the date constructor, if you don't pass anything, you get the current timestamp but you can also pass in a date instead which Javascript then tries to parse. Now for one, you can pass in an existing date object, this would simply store that date as a new object in date2 but you can also pass in the string to describe a date and of course then Javascript will do its best to pass this as a date, for example I could pass in 07/11/19 and now what Javascript derived is July 11th 2019 from this date.

Now again, the attached resources allow you to dig deeper and find out which formats you can use there, how you can also specify minutes and hours and so on and much more. Now these date objects can be really useful because for example if you would want to calculate the difference between this first date, which is today and date2 which is in July, then we can just execute date minus date2 and this gives us the difference in milliseconds and therefore if we take that difference and for example divide it by 1000 to have the difference in seconds, divide it by 60 to have a difference in minutes, divide it by 60 again to have the difference in hours and then by 24, we get the difference in days since that date, so that's just one example of what you can do there.

So definitely check out that date object also with help of the attached documentation if you need to work with dates in your application, if you need to store a date, run some date calculation or anything like that, this object has got you covered.

----------------------------------------
