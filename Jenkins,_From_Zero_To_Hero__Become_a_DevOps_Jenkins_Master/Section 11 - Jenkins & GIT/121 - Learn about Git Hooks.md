# Learn about Git Hooks

*Section: Jenkins & GIT*

Instructor: Hello and welcome back. In this video, we're going to learn about Git hooks. If you have never heard about Git hooks before, don't worry, but you must know that a Git hook is like a trigger. For example, whenever someone pushes to any branch, then a trigger is going to happen, and then you can define what you want to do. For example, whenever a developer pushes to your master branch, for example, you could trigger a new script that is going to call your Maven job, and trigger that new bill for that yard, downloading the new code and all of that stuff.

That's basically what a Git hook does. It's nothing but a trigger when an event happens. In this case, we're going to be talking about PushEvents whenever someone pushes to ascertain branch. For this, we need to create that Git hook inside of the Git container. If we do docker ps and then we go inside of the Git-server, and we do bash in here. Let's go to var opt gitlab git-data repositories. Let's go to var opt gitlab git-data repositories, the group that we created, and the repository that we created.

Let's hit Enter. If we do an ls, you're going to find this structure, which stands for the repository structure. In here, we're going to create a new directory which is going to be custom_hooks, and we're gonna change directory to directory. In here, we're going to create the script that is going to be triggered any time that someone pushes to this repository. I will show you I have the file already created here.

I'm pretty sure that you are already familiar with this. We are doing something pretty simple here. We're saying if the branch is equals to master, then you know we're going to generate the crumb. Finally, we're going to trigger the Maven job here. I'm just gonna say Maven job. We're going to trigger the Maven job pass in that crumb, the authentication that we created before. Remember that in here, we should use jenkins because it's going to be internal.

It's not going to be jenkins that local, but it's going to be the jenkins name that we define in the docker compose file. It's pretty simple. Whenever a push occurs, this script is going to be triggered and this is going to say, "Okay, if the branch is master, then generate a prompt and trigger the Maven job." That simple. Let me copy this all. We're going to go inside of the container, in the custom_hook directory.

We're going to create a post-receive file. In here, we're gonna paste that content. Let me copy this again Let me save this and that's it. If you cat your file, then you're going to see exactly the same thing. If the branch equals to master, then generate the crumb and trigger the Maven job, right? Remember that the Maven job is actually going to download the code because we already configured that.

This is it. Let me give this executable permissions, like change mode +x post-receive, and now we go one level back. If you take a look to the owner and the group of this, you can see that the root is the owner. We need to change that to git and git. Let's do change owner git. Group git to the custom_hooks directory. Recursively, let's hit Enter. As you can see, now we have the git as the owner, and the git as the group.

That's pretty cool. Let's go out of this. Now, you have created your Git hook. Whenever you push something to the master branch, that script that we created is going to be executed. Therefore, your job is going to be triggered. We're gonna test that in the next lesson.
