# Step 10 : Testing Performance in JUnit Tests

*Section: Unit Testing with JUnit*

Instructor: This would be the last chapter where we would be playing around with arrays and now we want to test the performance of arrays. So what we want to check is, in this particular test, I want to check whether arrays is sort, is performing well. I want to check a few things related to performance on the arrays. So let's go ahead and start. So testSort and let's just call it Performance. If I sort at one array, I don't really will be able to get the performance of it, right?

I mean, it would kind of be running in less than milliseconds, probably microseconds. So it would not really give me a good variety of performance. So what I want to do is, let's say the Array.sort. I would want my performance requirement is I would want to be able to sort million arrays. So I'll write i is less than equal to thousand million and i plus plus. I would want to be able to sort million arrays within a particular period of time.

So I'll just declare an is equal to quickly define something. I'll also introduce a little bit of variations in the array. I'll change array of zero. I'll always keep changing the value there just so that when I'm sorting the array, it's not the same values that are being sorted. So array of the zero, I'll put it as i and now I would want to sort the array. Here in this particular thing, I'm not really concerned about the actual expected value.

I mean, I know that the arrest sort would work because the other tests would test that scenario arrays are being tested. Here, I want to check whether I'm able to run 1 million sorts of this particular area within let's say, 10 milliseconds. So I want to check whether this entire area, sorting of million arrays of three elements each is happening within less than one second. How do I do that? That's where there's a timeout.

So I can say timeout and specify how much is the timeout in milliseconds? So let's say I want one, let's try, I don't really know how long it'll take to test this many arrays but let's run this unit test and see, ah the test succeeds. I mean, this is incredible. So I'm able to sort a million arrays within a thousand milliseconds. Let's reduce the time a little bit. Let's make it a hundred milliseconds.

Still succeed. Able to sort enough 1 million arrays of this type within a hundred milliseconds, let's say that's the performance benchmark we would need to hold. So I would write this test and keep it there so that whenever the performance of this particular array drops below this, this test would start failing. And this is a really good test to have when you want to make array very strict performance requirements on certain things.

So what you do is you would kind of take a little bit of buffer. So let's say I want to have this particular thing run within a hundred milliseconds. So I put a hundred milliseconds in here and I would run a little more than what my performance requirements are. So ideally, I mean, one thing you need to really consider is the fact that this would run on a build server somewhere. And on the build server situations might be little different.

So I mean, the build server might not be as powerful as your production box. You need to take those things also into consideration before you set the time out in here. But this is a really good test because now I can test the performance. So if the array.sort, somebody makes a modification and makes the performance worse then this test would fail and alert that there's a problem with performance in this particular thing.

This is how we test performance using Junit test.
