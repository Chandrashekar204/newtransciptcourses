# Step 06 : @Before @After

*Section: Unit Testing with JUnit*

Instructor: Some of the tests have some setup to do before I can really run the test and the setup might be common to all the methods which are there in the particular class. What would be the right place to do such kind of things? That's where the at before and at after methods come in. So let's look at a quick example of a unit test with that. So let's create a new unit test for it. So let's not do it in here.

Let's quickly create a new unit test for that. So I'll go to source test Java and I would want to go to the package where we had the string helper test and I'll create a new class or I click New JUnit test case. That's how we created this unit test. And I would want to write a quick test. So I would probably call quick before or after test or something of that kind. We want to learn how the before and after work.

So I just leave the rest of the stuff as detailed I mean as defaults and let's click finish. And the usage the first I mean this is the auto-generated code by Eclipse and when I run this test it would fail because there's a fail method calling not implemented yet in here. So that's good. So let's actually, what we'll do is in the test itself I'll call this test one. Let's keep it very simple and I would actually do a sys out.

Actually, it's not really recommended to do a lot of sys outs in your code. Ideally you should be using a logger or in like I don't really want to set up the logging framework so I'm going to use sys system out. But ideally it should be logger. So system out, I'll say test one, execute it. And let's do a little bit more of setup before we try and at the before and after method. So I'll call this test two and test to execute.

I want to understand how the before annotation works. So I want to run this method public void before like let's call it setup. Instead of calling the before, I'll call it setup. Let's say this is either setting up some test data before executing the test. So let's say this is the executing this setup for each test. So let's call this system out out. I'll call this before. How do you at, say something needs to be executed before every test?

How do you do that? Try and guess. Yeah, at before is the annotation. So I'll at at before annotation. So it's in org.junit. If you type in at before and press Control space Eclipse would bring this drop down down and you can place enter. And then that particular import is ated in to the list of imports. So it's, there's an import our J unit before enough. Let's see what happens. I'm going to just run this test.

Okay, let's see what the output is. Right click run J unit test. Both the tests would succeed. I mean there's no question about it because there's no nothing being tested. Just a sys out. But you can see that whatever is in at before is executed before every test. So that's the crucial thing that we wanted to learn. So if we had some setup to do before a test I can do that setup in the at before. So at before, before test would do that.

So one of the ways if let's say I wanted to create a new string helper, right? It's not okay for me to create have one instance of string helper in here. If it was that kind of scenario where my class I would want to create a new instance of the class every time the test runs. The way I could have done it is I could create a string helper in here and I can create a at before method. So I can use at before, I mean as usual I have to do a import.

So I'll use Eclipse to get that import at before public void. I mean the name before here does not signify anything. You would've called it setup or dummy or yeah, whatever. But give it a real good name. Don't, I mean even though it's not important it might be useful to have a good name there. So let's go ahead and write the new in here. So what would happen now is before every test the new string helper is created and each of these tests would be running with a new instance of string helper.

In this particular test, it's an overkill because I mean we are not having any value stored in the string helper. It's just some kind of an utility helper class. But if let's say there was some data stored in that particular class and you want to renew the setup each time, then you have the at before, and I would have you guess what at after would do. Think about it. Yeah, your guess is very true.

So it's public void. Usually we call it tear down. Let's say I created a lot of data set up for my test and I would want to tear down, tear it down after every test. So let's say I got a connection to the database or connection to something, which I want to give it back. I mean, I don't want to leave the connection open, right? So how do I do that? I'll do that using the at after annotation. Again, I can do control space and get the input in.

And as you know, the way we do it sys out and the way I got the system printer line was sys out and control space and you would have system.out.println. I would really recommend you to become an expert at IDE because if you understand how the IDE works that's half the job work, half the job done. Because as a developer, we are on the IDE all the time. So learn everything that you can do. You can about Eclipse I guess, or IntelliJ if that's the IDE you're using.

Okay, let's go. Go ahead with whatever we are doing in here. Printer, what do you want to print? I want to print after test. Let's run this test and see what after does. Aha, before test, test executed after test, before test, test executed after test. If I had two more tests, then before test and after test would have been executed twice. If I have to explain them in a nutshell before and after. These methods are run before every test method and after every test method.

So the before runs every, before every test method and after runs, after every test method. So if I have five tests then before runs five times, after runs five times. That's the before and after test scenarios.
