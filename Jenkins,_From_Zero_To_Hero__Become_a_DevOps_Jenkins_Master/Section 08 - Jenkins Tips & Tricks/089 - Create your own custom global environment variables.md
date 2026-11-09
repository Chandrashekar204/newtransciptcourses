# Create your own custom global environment variables

*Section: Jenkins Tips & Tricks*

Instructor: Hello and welcome back. In this video, we're going to learn how to create our own environment variables. Remember that as I told you in the previous video, by default you have global environment variables that allows you to know the number of the execution, the URL of your execution, the name of your job, and more. But what happens if you want to create your own environment variables that are going to be globally accepted?

Well, that's a good question. So let's go to Manage Jenkins, and we're going to go to the configure the system. And in here, we're going to scroll down a little bit, and we're going to look for global properties. Under this section, you're going to see something that is environment variable. So let's click on this, and you can add as many variables as you want, clicking on the add button. So we're going to name this variable, for example, name of the course, and then we're gonna give it a value like Jenkins, Jenkins course, just to keep it simple.

Then we can add a new one. And we're going to say country. And that's my current country, so we're gonna say Columbia, and that's pretty cool. So remember this name. I'm just gonna copy this in here, and I'm gonna copy this in here. And okay, so we're gonna click on Save. And now if we go to our environment job that we created to test the global variable, we're gonna go to configure. And here we're going to hit enter.

We're going to give some asterisks in here, and let's go to do an echo to this name of the course, which is the variable that we created, and we're going to do an echo for the country global variable that we created. So let's do like this, and let's hit on the Save bottom. So let's click on Build Now, and let's see what happens. So the execution already finished. Let's go here. Console output. And as you can see, all of the previous values already changed.

The build number, the build URL already changed. The name is, of course, the same. But as you can see here, you are having the output of the Jenkins course environment variable that we created and the echo country that we created. So this means that you can also create your global variables in order to call those variables from any job. So for example, you have something that it's pretty constant, like a server name or a configuration file or a configuration option, or anything that you need in all of your jobs.

And probably you're going to be using a global environment variable to use that variables in all of your available jobs. So this is what global variables are for. I hope you can use them, and you can find them useful. If you don't find them useful, don't worry. Probably you will need to use them in the future or probably not. Just give it a try. This is it for this video. I'll see you in the next lesson.
