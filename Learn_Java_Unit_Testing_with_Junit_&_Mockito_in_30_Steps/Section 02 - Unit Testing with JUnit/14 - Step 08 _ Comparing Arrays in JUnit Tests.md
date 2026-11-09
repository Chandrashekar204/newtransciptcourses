# Step 08 : Comparing Arrays in JUnit Tests

*Section: Unit Testing with JUnit*

Instructor: In this section, let's learn how to compare arrays. To make things easier for us, I already have a sample test created and it's failing because that's what Eclipse brings in, a failing test at the start. So I'll remove this line. So what I want to test is really the arrays class. So I would want actually import the array class and check the functionality whether the sorting is working fine or not.

So I'm going to use the arrays.sort method in here. So there's a method called a sort in arrays which you should be knowing I guess. So if you have an array, let's just create a array int numbers is equal to, let's say I have four different numbers. Let's pass them in 12, 3, 4, and 1. So what would be the output if it's sorted? That's the expected values, right? Int expected values, what would be expected array values?

1, 3, 4, and 12, right? That's how it would look sorted. So let's first sort the array. Arrays.sort. I want to sort the numbers. So let's go ahead and type in numbers. So arrays.sort numbers. The thing about arrays.sort if you read the documentation is it does a in place sort. So it does not return anything. So it's written in white. So whatever arrays passed, it would be sorted in ascending numerical order.

So it would be ascending numerical order. That's how we have the expected values. So numbers would be in an ascending order. So now I can use, how can I compare arrays? Can I use a sort equals? Let's try that, actually. Assert equals, I would pass in numbers and expected. Is this right? No, not really, right because ideally we should have the first value as expected and the second one is actuals. So I should have expected comma numbers.

Let's do this. So assertEquals numbers, expected comma numbers and I would rename it. So testArraySort or test sort. I could have called this underscore random array. Some random array does not really matter. I'll run this test enough. Aha, it failed. It's saying expected this, but it's this. The problem with assert equals when I pass into objects to it is it expects them to be the same object. So it's not doing an equals on it, but it actually checks if they are really the same object.

Because this array is really different from the numbers array. It's different, but it has the same values. So it's a different object in memory, but it has the same values that the assert equals does not check. So if I want to compare the values inside the array, I should use something called assert array equals. So I'll import assert array equals, the assert array equals has very similar syntax to assert equals except that it's assert array equals, sounds comical.

Okay, let's run this test now and now it would succeed. There you go. A green bar, famous one. Now I'll just say or wrong expected value. So I'm just changing the values so that they're not really sorted. I want to really check whether the failure is working. Yes, it's failing and it's actually giving me a little bit of good output as well. You can see that it says arrays deferred at element 1, expected 4, but was 3.

So what does it really mean? What information is it giving? The great thing about the Junit framework is when there's a test failure, they try to be as helpful as they can. So I'll paste this in here. I don't really care about the rest of the stuff. If you look at this message which is in the log, when this failure happened, it says arrays first differed at element 1. So index starts with zero, right?

So actually the when it sorted this array would look like how, 1, 3, 4 and 12. So the message which came up says, "array first differed at element 1". So this is zero. I mean, as we know, the index is 0, 1, 2, and 3. So when Junit framework is comparing these two in the array equals method, it sees that at index 1 the values are different. So at index 1, the values are different. I'm expecting a 4.

So the expected value has 4 but the actual value is 3. I mean, can anybody be more clearer. So I mean, when there is an error, Junit gives me exactly what's wrong. And that's really perfect, right? Isn't it? So that's how we compare arrays. We use the assert array equals method.
