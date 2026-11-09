# Step 12 : Organize JUnits into Suites

*Section: Unit Testing with JUnit*

Instructor: Now we have four different tests, which we have written during this particular course, and we want to organize them and I would want to run a set of them only. One of the ways is if you do a right-click Run As as JUnit Test, and here right-click Run As JUnit Test in here, it would run everything there is. So you would see that all the tests run, all the four classes run, but I would want to only run three among them.

Let's say I want to only run two of them. How do I want to organize them? I would want to be able to organize a group of them into a specific group. So those groups are called test suites. So how do I create a new test suite? So the way I do that is right-click New, Other, and you can type in JUnit test suite. So this is how we would create a test suite. Now I can create it. Next. And I can actually choose which classes I would want to have in here.

I'll just choose couple of them for now, so I'll choose couple of the tests in here and I can say Finish. And now, you'd see that when I run this suite, like when I created this suite and run this test, what would happen? Only those two suites would run. So if I look at the JUnit test which ran, it would only have six tests of two belonging to... I mean, two belonging to one class and four belonging to the StringHelperTest.

That's the set of things that we added in here, so QuickBeforeAfterTest and StringHelperTest. If you want to add more tests, you can add a comma in here and you can add more tests. I mean, it should be a very simple thing to do that. So you can group tests. If you really want to understand what the code was generated, actually similar to parameterized test, in the parameterized test that we wrote, we used a RunWith Parameterized.class.

Similar to that, there is a suite.class. When you run with suite.class, you get an annotation called @SuiteClasses. In the annotation, this is basically an array. I mean, if you just want to run one class, you don't need to create an array. But because I want to run two different test classes as part of this suite, I mean, what is the use of creating a suite when you just want to run one test? I mean, it doesn't really make sense.

So ideally, this should be an array and it should have multiple classes defined in here. I mean, multiple classes listed in here. So you'd have all those listed in here. And when I run this test, all the things which are present in here would run. I mean, a suite is really a good way of organizing your tests. Let's say I have a few tests which are running very slow, I don't want to run them a lot of times.

Probably I would kind of group them and I would run them very... I mean, less frequently than all the other tests. If I have any memory intensive test, performance intensive tests, which I don't want to run very often, then I can group them into a suite and kind of exclude them. So that's the kind of flexibility that suites bring in. Suites is kind of an advanced feature, but I really wanted to introduce it to you because it's nice to know what are the features that a framework offers.

So it is one of the good features that are present as part of the JUnit framework.
