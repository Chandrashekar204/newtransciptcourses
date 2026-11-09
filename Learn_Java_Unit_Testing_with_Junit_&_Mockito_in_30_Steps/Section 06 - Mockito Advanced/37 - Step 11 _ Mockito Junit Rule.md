# Step 11 : Mockito Junit Rule

*Section: Mockito Advanced*

-: We are making a lot of progress and we are now at step 11. In the previous step we looked at all the different Mockito annotations. In this step we will learn a few things called rules. So what is rules? Why is it needed, and what are the rules that are present with Mockito? In the previous step, we added an annotation at run with MockitoJUnitRunner. The MockitoJUnitRunner would make sure that all the Mocks are created and are [Inaudible 00:27] as per the need.

So when I put an InjectMocks then this todoBusinessImpl, all the mocks would be injected into it. So the MockitoJUnitRunner would check what are the dependencies of todoBusinessImpl, and if any of them are available in here then they would automatically be wired in. So they'll be set appropriately. That's what the JUnitRunner is. Let's say I want to use MockitoJUnitRunner, and I also want to use spring framework.

So let's say I want to use another runner. Let's say I want to use the SpringJUnitRunner. So if I want to use two JUnitRunners, that's not really possible. So what JUnit came up with is this concept called rules. Instead of using runners, you would use something called a rule. So, the way you can create a rule is by using something called at rule. I'll input this annotation at rule and I can click this at rule.

As you can see at rule was introduced in JUnit 4.76 It's kind of a latest addition. So it's basically annotation. So what happens when I put an at rule on a test, is that similar to a runner? The rule will be run before and after the test. So if, let's say I put like the specific rule for the Mockito Runner is the Mockito Rule You can find the exact snippet in here public MockitoRule. It can be MockitoRule, MockitoJUnit.rule Let's make sure that we are importing this in.

So basically instead of using the runner you would start using the rule. So now I can remove the runner and run this test. You can see that the rule has to be public. So it's throwing me an error saying this should be public, so let's actually make it public. The most important thing is all the rules should be defined as public because the JUnit framework need to be able to access that to run that.

So let's now do that run as JUnit test. You would see that this would succeed. So the great thing about using rules is the fact that now I can define another rule. So there can only be one runner but you can have multiple rules. So let's say there's a spring framework rule, a spring unit test rule, I can add that in. And that rule would run before and after the test to make sure that the initialization is done properly.

So basically the way you can look at rules is that like with runners, you can only have one runner. -: So it kinds of makes the test very brittle or very dependent on a specific runner. And whenever you want to do something else then you are really tied-up because you cannot use another runner. So instead of using a runner, you can use multiple rules and these rules can do this setup for you. So JUnit is now moving away from runners and moving more towards rules because rules makes the test more flexible.

You can have multiple rules defined and each one independent of each other. So there you go. That's a really short video to discuss a little bit about rules. So you'll see a lot more people using rules going forward than runners. Until the next step. Bye-bye.
