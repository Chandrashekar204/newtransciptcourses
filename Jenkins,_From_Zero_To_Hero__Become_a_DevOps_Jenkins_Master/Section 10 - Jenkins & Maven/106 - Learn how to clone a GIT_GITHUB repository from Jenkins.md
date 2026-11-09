# Learn how to clone a GIT/GITHUB repository from Jenkins

*Section: Jenkins & Maven*

Instructor: Hello and welcome back. In this video, we're going to learn how to clone a Git repository using Jenkins. So we're going to be working with a Maven repository. So let's go to Google, and we're going to search for sample Maven app, Enter. And we're going to find out this first result and this is a GitHub repository. So if you click on it, you're going to find out here all the Maven stuff.

And this is a Git repository, a GitHub one. So we're gonna clone this repository using Jenkins. So the first thing that we need to do is to create a new item. So let's create a new job, and we're going to call it like maven-job, for example. And this is going to be a freestyle project. So hit OK. And now, let me introduce you a new concept which is SCM, which stands for Source Code Management. And this means where your code is located.

In this case, our code is located on GitHub. And the Git plugin works for GitLab and for GitHub. So in this case, our code is located on Git. So we're gonna copy the repository URL. This is the repository URL. So we're gonna copy this. Let me copy this all. And we're going to paste that in here. And as you can see, this is all we need to do. If we go to advance, we can add the name of the branch that we want to clone, if you want to clone a different one.

But in this case, we're cloning the master branch because normally, that's the branch that we're going to be cloning. This is the master one. So this is the branch that we're, by default, specify in here. So in this case, we don't need credentials because this is a public repository. But in the future, we're going to be building our own GitLab server and we're going to be learning how to use authentication.

So that's pretty cool. Let me click on Save. And that's it. Now, if you click on build, what's gonna happen is that the Git plugin that you installed, it's going to go to this repository and it's going to clone that. So let's look for this build history, execution, console output. And as you can see, this actually was success. So you may be wondering, "Okay, this actually cloned this repository, but where is located the code?" And let me introduce you a new concept that is a workspace.

And workspace is the place where the Jenkins things occur. For example, in this case, Jenkins is cloning this repository, and it's cloning that to a workspace. And every single job has a workspace. And all the things that will occur within that job are happening in that workspace. So let me show you. If we go to our console, and then we try to do something like docker exec -ti jenkins bash, and you go to your var jenkins_home workspaces and you hit Enter, and you hit ls -l, you're gonna find out workspaces for all the jobs that you have executed.

So in this case, we want this Maven job which is the one that we're executing right now. So let's go to Maven job. And if you enter in here and you do an ll or ls -l, you're gonna find out all of the files that were cloned using Git. And how do we know that these files are the original ones? Okay, if you go to Google and you go to the GitHub repo, you're going to find exactly the same structure. So this is Jenkins, source, pom, and README.

These files are hidden. So if we just do an la, you're going to find those files but this is exactly the same repository. And please keep in mind that Jenkins always clones those things to the workspace of the job. So remember that everything that happens in the job, it's happening in our workspace. So having said that, we already know how to clone a Git repository and your Git repository is going to be cloned in the workspace.

So from there, you can modify files, you can access those files, and you can do things. So this is it for this video. I'll see you in the next lesson.
