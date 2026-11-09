# Step 09 : Testing Exceptions in JUnit Tests

*Section: Unit Testing with JUnit*

-: In this chapter, let's learn how to test exceptions. I'll copy the previous test just to make it easier for us. We want to test exceptions so I have to create an exception. So how do I create an exception? What I'll do is the numbers instead of passing in a real array I'll make it null and do arrays dot sort numbers. I'll not worry about this right now. What would happen is when I pass a null array to arrays dot sort, what would happen?

Do you want to guess? Run S, do a new test. What would happen is it throws a null pointer exception. So the arrays dot sort, when you call it it throws a null pointer exception. So this is a proper scenario. This is one of the requirements for arrays dot sort. The arrays dot sort when I send a null array to it it should throw a null pointer exception. So that's a proper scenario. That's a valid scenario.

This is not really an error condition in here. So there's not an real code going wrong. This is really code being right and I would want to test for this exception. So how do I say in this particular thing that the exception is expected? Typically, people do something of this kind so you can put a try catch. So I can put a try catch and catch the exception. Let's be as specific as we can. We are getting an null pointer exception.

You don't need to do anything in here because the thing is a success. So this test would succeed. Ah-ha, succeeds, because now I'm expecting a null pointer exception. So the code comes in here and I'm not doing anything in here in a JUnit test. If a test does not throw an exception or it comes out in a proper way, then it's success. Absence of failure in JUnit is a success so this would succeed. But actually a better way to do this would have been to use an specific annotation which JUnit provides.

In JUnit I can say @ expected is equal to the exception, which we are null pointer exception dot class. This is the way I would declare that I'm expecting a null pointer exception. So what would happen? So this test is expecting an null pointer exception to happen. So when the null pointer exception is thrown this would be fine. I mean, this would work properly. But let's just say I'm passing an empty array, an empty array when you sort does not throw an exception.

So what would happen? Oh, the red bar, because now, I'm expecting an null pointer exception, but this is not throwing an exception. So the good thing is testing an exception, I mean, when I'm testing for an exception, I'm really expecting an exception to happen. So if an exception does not happen, it's a failure. So that's what is happening in here. I'm expecting an exception, but there's no exception thrown.

So that basically means a failure. So we have learned how to test exceptions in here. We expected an null pointer exception and we saw that when an null pointer exception was thrown this test succeeded. And when null pointer exception was not thrown, this test failed. And in a normal test where I don't expect an exception, and if there's an exception thrown, then that test would anyway fail. It would say unexpected exception and it would come up with the exception trace.

So that's about handling exceptions in JUnit test. Good luck with them.
