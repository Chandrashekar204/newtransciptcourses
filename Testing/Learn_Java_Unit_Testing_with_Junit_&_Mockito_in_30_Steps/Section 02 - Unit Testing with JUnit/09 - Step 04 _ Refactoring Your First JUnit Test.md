# Step 04 : Refactoring Your First JUnit Test

*Section: Unit Testing with JUnit*

Instructor: This is where we left off in the previous section. We had a small unit test which was working. When I run this, it does work. It shows a green bar. But there are a few things which are not really good about this particular test. Let's start with them and let's improve them. So first thing is the name of the method test. Aha. What is it testing? It's not really clear, right? Let's make it more specific.

The fact that it's testing the truncateAInFirst2Positions method I would make it testTruncateAInFirst2Positions. So now it's at least clear what method it's testing. When you go more advanced into unit testing you would actually go in and specify what condition you are testing as well. So you'd say test this particular method. Which condition am I testing? So am I testing condition one or condition two?

You'd kind of give a business related terms to test, to give a name to that particular condition. So let's say if I'm in a banking scenario probably I'm trying to withdraw amount and checking whether balance is fine. So I would say testTruncateAInFirst2Positions. Aha doesn't really make sense, but you get D drift, right? TestTruncateAInFirst2Positions when amount is withdrawn, something of that kind which gives a significance of the condition being tested.

The other thing that we are doing in here which is not really good is I'm testing two conditions in the same test. Because this is very simple test it's okay because now it's remains readable and if it fails I would be able to debug relatively easily. But in when you're at unit testing complex scenarios it's not really good to have two conditions tested in the same unit test. Ideally you need to create another test.

So how do we create another test? So let's go ahead and do that right now. So at test is how we add in a unit test. And the most important thing when we add in @Test is the method should be public and void. No other signature is acceptable. So if you try with any other signature the unit test will not run. So let's quickly do something of this kind. So test2, and I would write this test because it is public wide, it would work.

But let's say if it was let's say public string something and it's returning something back, can I run this test? Nope, it's not really allowed. If you see the exception which is coming up it would say method test(2) should be void. So you cannot have a return type for the test method. So it should be void. And the other thing is it should also be public. If I remove this also and try and run this test The output the error we get is method test two should be public.

So any test method should be public and wide. The reason it should be public and wide is because some framework should be able to call it and the framework would be in a different package compared to the test. And if it's a default status or a protected status, it's not sufficient. It has to be a public method. So now in here also we want to test the same thing. So we would actually really make this test for now testTruncateAInFirst2Positions2.

This is not really good thing to do one and two but let's quickly do some do it and refactor it a little later. So I would want to test the second condition in here. So I'm moving the code out. So string helper and I would actually copy the code in here assertEquals. We have the second condition being tested in the second method. The good thing about this is when this test fails you would know specifically which condition has failed.

So now let's go ahead and run this test. Okay, there you go. So you see the green bar. However, when you look at it in detail you'd see that there are two tests which are run. So testTruncateAInFirst2Positions, testTruncateAInFirst2Positions2. So that's the reason why you had a green bar with two methods, because we now created two methods. Actually one of the things which we can improve in this is the naming.

So testTruncateAInFirst2Positions. Which condition am I testing? So I would call this AinFirst2Positions. For the simple test that we are writing this might be an overkill but in real world business scenarios, it's really main, I mean this results in really maintainable code. So if you have a test method, underscore the name, I mean the condition that you're testing, that results in really good maintainable code.

There's a specific section that we have in writing maintainable unit test. Will we look at this in more detail. So this has only AinFirstPosition. So now run this test and see what happens. So this test succeeds if I highlight a method and run the test, it'll test only that particular method. However, when I do a right click, run as JUnit test from here, it would run everything. So it would run all the tests in that particular thing.

Now you can see that in this particular test AinFirst2Positions, AinFirstPosition, both tests are succeeding. The reason why we stress on having two different tests for each of these conditions is that if let's say this test failed, so instead of expected, like let's say I'm expecting CDA in here and not the correct output. So what would happen is you'd see that there's a condition which is failing.

So JUnit test, it says there's a condition which is failing and it would also tell you which specific condition. So when I read the test I can say AinFirstPosition test is not working. So what might be the logic that's going wrong? I mean it already gives you a clue as to what might be really wrong. So I would go back. The other thing you would've already noticed is that there is a small duplication in here.

So StringHelper, StringHelper. Why do I really need to create it twice? I mean the same code is repeating twice. So how do we really avoid this? I can actually create an instance at the class level. So I would remove it in from here and I would create an instance at the class level. Now I don't have any duplication in here and this is probably one of the cleanest tests that you can write for the example that we have.

I would leave writing the next two conditions in here as an exercise for you. So try and go ahead and write test methods for testing these two string inputs and seeing whether you can write your unit test. I would really recommend playing around with the framework in here a little bit. So try and create as many test as you can. Try, play around with it. Use assertEquals, pass some dummy inputs that you would want to pass and play around with them.

And that will really give you a really good understanding about the unit test.
