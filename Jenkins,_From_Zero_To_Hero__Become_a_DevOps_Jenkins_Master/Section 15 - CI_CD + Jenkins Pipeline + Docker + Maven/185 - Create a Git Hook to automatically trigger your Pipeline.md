# Create a Git Hook to automatically trigger your Pipeline

*Section: CI/CD + Jenkins Pipeline + Docker +  Maven*

Instructor: Hello and welcome back. As you saw in the previous lesson, our pipeline is working good, but we need to trigger it manually. So now we are going to create a Git hook in the repository so that whenever the developers push code to our Git repository, Git is going to trigger our job. And then the entire continuous integration process is going to start, building the jar with the new code, testing it, pushing it, and deploying it to the final environment.

So to do this, we're going to enter inside of the Git repository, so, I mean inside of the Git container. So let's say bash And let's go To var OPT. GitLab, I will say Git theta. Then we go to repositories Jenkins, and we want to go to the pipeline Maven repository that we created in here. Remember that to create hooks, we need to create a custom hook directory in here. We're going to CD to this directory.

And in here we need to copy the script. So we're gonna copy that from the DSL project that we created. Custom hook, post receive, and we're gonna copy the script to this location and now we need to modify it. And the only one thing that we need to change is the URL for this job. So this is not going to be job DSL, this is going to be pipeline docker Maven. So we're gonna copy this. We're gonna paste this in here so that whenever someone pushes to this repository, this job is going to be triggered.

So let's save this. And now we only need to go back and we need to change permission for this. So change owner Git Git for custom hooks recursively, and this is it. Now we have our custom hook directory and whenever someone pushes to our repository, then our entire process of CACD is going to start. I'll see you in the next lesson.
