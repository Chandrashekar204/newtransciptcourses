# Display the result of your tests using a graph

*Section: Jenkins & Maven*

Instructor: Hello and welcome back. In this video, we're going to learn how to store or how to make a graph using the overall or the average of the tests. So for this, we're going to go to the Configure Section, or before doing it, let me show you what happens when you do a Maven Test. What happens behind the scenes is that Maven, let me look for a test, it's actually generating a report. And in that report is an XML file with all the information of the tests.

And you can find that folder in here. So let's go to our container. Remember that I am inside of the container. If we go to this full path, remember that this is the workspace where everything happens inside of the job. So let's copy this. And if we go to target and then surefire-reports, cd surefire-reports, you're gonna find out an XML file, which is that result of your tests. So remember that from here, we actually can reach this target folder in that root, because the workspace is that root for this job.

So for example, let me go back. This is actually that root of your workspace. So Jenkins is actually taking this pom, and it means that you can do something like, ls target/surefire-reports, and you do *.xml and you're going to find your file. So this is a relative path and we can use it because remember, that the job execution is in this folder when the execution is happening. So we're going to copy this path, because here is the file with the report.

So we're gonna copy that and we're going to configure our job. Let's add a Post-Build Actions, and this action is going to be, Publish that JUnit Test Report. So we're gonna click on this and it's going to ask, "Okay, where is that report?" So we're going to copy the folder, and then this, which means that this is the file that it's going to be used. So it's actually going to take this file and create a graph using this.

That's it. Pretty simple. So now we're gonna Save this. And in order for the graph to appear in here, we need to do like five executions, something like that. So we have the execution #9 here. Let me do like three or four more, and probably a graph is going to appear here, showing the behavior of the tests. Okay, I actually executed the job twice, as you can see here, 10 and 11. And now we have a test result trend, which is something like a graph, that actually tells you how are your tests going.

If you have errors, then it's going to appear here. Some things like errors and some red things, so that you can have an overall view of how your tests are behaving. So this is it for this video. You already know how to save or how to record the state of your test and display that information using a graph. I'll see you in the next lesson.
