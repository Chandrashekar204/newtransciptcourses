# Parameters

*Section: Jenkins & DSL*

-: Hello and welcome back. In this video we're going to learn about parameters, how you can create parameters using D-S-L. So let's look the parameters file in here. And as you can see, it's pretty simple. You define parameters and then you define this curly braces and inside of the curly braces, the type of the parameter. So in this case we have a string parameter and in here you pass the name of that parameter.

If you want, you can define a default value and if you want, you can define a description. Same thing in here, we pass a Boolean parameter, the name, and we define if it's true or if it's false. And we can pass a choice parameter, as well, the name of that parameter, and then we pass a list with the options, and we can even define a default one. It's important to say that you can use one or two or three or the ones that you prefer.

So if you want to find more information about parameters let's go to the documentation, let's look for parameters in here, and always look for freestyle jobs. So in here, look for it, and as you can see, we have a lot of examples. If you click on these three dots, you're going to find all of the available options. So I am just giving you the normal ones. Probably the options that you are always going to be using or most of the times.

So let's go ahead and copy this. We're going to go to our job. Let's go to the seed job. We're going to configure this, and we're going to paste this new code in this configuration. So let's paste that in here. And this new job is going to be called "D-S-L example", this is going to have this description, and these parameters. So let's save this and let's build this job. The execution succeeded, as you can see here, so let's go to the dashboard.

Let's go to our job "D-S-L example". And in here, if we go to configure this job, you are going to find out that you have already parameters. So these already marked this as parameterized and you can see that you have a simple string parameter, which is "Planet", the default value is "World" and the description, "This is the world". So if we take a look to our D-S-L name, default value, and descriptions.

So these are the fields. Let's go to the second one which is the volume parameter. Name, "FLAG" and it's true by default. "FLAG" and "true," pretty cool. And then we should have a choice parameter which is named "Option", and with a list with "Option one", "two", and "three". So let's scroll down and exactly like this, you are going to find the "Option," "Choice" parameter and the choices in here.

So if you save that and you click on "Build with Parameters," you are going to be presented with all of these parameters that are available for the execution of the job. So this is pretty cool. You already know how to create a job and how to create parameters for that job using D-S-L. So this is it for this video, I'll see you in the next lesson.
