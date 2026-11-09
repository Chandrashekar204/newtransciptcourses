# Step 07 : @BeforeClass @AfterClass

*Section: Unit Testing with JUnit*

Instructor: We looked at the before and the after methods, right? They're executed after and before every test. There would be certain things which I don't really want to do after and before every test. I would want to do them before a class only once. So for this entire class, I want to do it once and I don't want to do it again. Those are the kind of things that you can use before class and after class for.

So @BeforeClass, and let's do a Control + Space Import. Yeah, that's good. And public void beforeClass. I'll call it beforeClass. You could have called it anything else as well. I mean, the important thing is the annotation and the name of the method does not really matter. As our convention is, I would just call it sysout Before Class. Okay, let's quickly run this. Aha. What would happen? Aha. As expected, there's an error being thrown.

What it says is method beforeClass should be static. Okay, that's one thing you need to remember about before class. The before class, any method which is implementing @BeforeClass annotation should be a static method. So that means all the constraints that are around static methods as well. You cannot refer to instance variables and all that kind of stuff. So you can only have class level things initialized in here, only really static things initialized in the before class.

And now, let's see what would happen. Aha. You would've seen the green bar as well as nav. You can see before classes only executed once, Before Class, Before Test, After Test, but the Before Class is only executed once before the class. And this can be used probably to initialize some database connections or things like that. I mean, I really prefer to use before and after rather than using before class and after class unless you are really concerned about performance.

So if there are some things you are doing before and after which are taking a lot of time and you don't want to run them in every test, then you can use the before and after class. So now, I used AfterClass nav, I'll import it in. I'll call this afterClass and After Class again. And let's run this. Okay, so Before Test, Before Class, and the Test, another Test and After Class. So Before Class is executed once.

After Class is executed once. Before Test and After Test are executed as many times as there are tests in this particular class. So that's the introduction to before class and after class. So if we look at the summary of what we have learned in this particular section, we have started off writing assert through assert false methods. And then we used @Before, @After, @BeforeClass, and @AfterClass. Let's meet in the next section.
