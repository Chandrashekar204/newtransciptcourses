# Continuous Integration

*Section: CI/CD - Definitions*

Instructor: Hello and welcome back. In this video, we're going to have a look at continuous integration only, because in the introduction video we actually saw all of these steps together and probably that's too much information at once. So we're gonna split it and we're gonna be talking here about continuous integration. So, okay, it's super important to keep in mind that your code should always be a version using probably Git or something that you want.

In this case, that's a thing that you have a Git repository and you have your code there. So we're going to be thinking about a Java application. Your developers are pushing code here and are pushing Java code, right? So your continuous integration process will be started by your Git server, probably using a Git hook or the way that you prefer. Then your Jenkins or your continuous integration process starts, normally viewed in the application.

In this case, normally the process starts doing something like Maven package or something like that and then you start testing that package, that jar, that artifact that you actually built. So that's super important. In continuous integration, you only have the trigger. Okay, the trigger is not actually considered a part of continuous integration, but it's super important. But in the continuous integration process you have the build of your application using the code that was pushed to your repository, and then you have the functional testing or any kind of test that you wanna do there.

Remember, testing is super important for a continuous integration process, because test tell you that your application is behaving as you expect. So this is it for this video. Remember, continuous integration is nothing else but building and testing your application.
