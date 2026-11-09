# 1.9 — Installation of Java in Windows OS

> Section 1: Let's Say Hello to Java

[00:00] Inside these lecture, let's try to install and set up Java in Windows operating system.
[00:06] In the previous lecture we set up Java inside Mac operating system by using SDK man.
[00:11] But the same SDK man we can't use inside windows operating system.
[00:16] Let me show you the reason for the same inside these SDK man website.
[00:21] If you click on this docs, we will be landed onto this installation page.
[00:25] Inside this page if you can scroll down, there are instructions around the windows installation.
[00:30] There are two different approaches that they provided, but in majority of the scenarios, both these
[00:35] approaches, it won't work inside windows operating system because SDK man is not officially supported
[00:42] inside windows operating system due to the restrictions that we have in the windows operating system.
[00:48] They also mentioned officially here there are some issues with this approach, but it works for the
[00:53] most part.
[00:53] I tried in my windows system and it didn't work.
[00:56] That's why instead of SDK man, I want to show you the another easier approach that you can follow inside
[01:02] Windows operating system.
[01:03] You just have to go to the AWS dot amazon.com slash website.
[01:08] Here you can click on this download I-225 inside this page.
[01:12] If you can scroll down next to the windows operating system, you have two options to set up JDK.
[01:18] The first one is by using the installer and the other one is by using the compressed zip file.
[01:23] I recommend you going with this installer, because when you use this installer to setup to install
[01:29] Java inside your system, it is automatically is going to set up the required environment variables
[01:34] in your system.
[01:35] You can click on this link.
[01:36] Please make sure you are downloading the file which is ending with.mc.
[01:41] Once the file is installed, you can double click on the same and and this window is going to appear.
[01:47] You can click on this next followed by.
[01:49] You need to remember this location where your Java is getting installed.
[01:53] By default it is going to be installed inside C program files Amazon Corretto.
[01:58] In case if you are seeing different path, please make sure you are remembering that path because in
[02:03] future, if you want to know where the Java is installed, this is the path that you need to refer.
[02:08] In case if you want to install in some other location, you can click on this browse and select the
[02:14] required path, but I recommend you going with this default recommendation.
[02:18] You can click on this next, followed by install.
[02:21] After a few seconds.
[02:23] The installation is going to complete.
[02:25] Once the installation is completed, you can click on this finish and open windows PowerShell terminal.
[02:31] Inside the PowerShell terminal you can try to run the command Java Hyphen version.
[02:37] As soon as I press enter, it is giving me an output saying that so-and-so version is installed inside
[02:44] my system.
[02:44] So what is the version that right now install Java 25.
[02:48] In case if you are not able to see this output, I recommend you restarting the PowerShell and your
[02:53] system as well.
[02:54] If you are still not able to see this output, you need to search for Edit System Environment Variables
[03:01] option.
[03:02] You can click on this.
[03:03] Inside this window there is an option of environment variables.
[03:07] Let's click on the same and under the system variables.
[03:11] As you can see, a variable with the name Java Underscore home is automatically created by the Amazon
[03:18] Corretto during the installation.
[03:20] So this will be the variable name and this will be the value.
[03:22] So let me click on this edit.
[03:24] So this should be the name that you need to consider to create the variable name Java underscore home
[03:29] in complete capital letters.
[03:31] Coming to the value, you need to mention the place where the JDK is installed, so it is installed
[03:38] in C program file Amazon Corretto under the folder JDK 25 0.0 underscore 36.
[03:45] By default, the system environment variable is going to be created in case.
[03:49] If it is not created, you need to click on this new and give the variable name Java underscore home,
[03:55] followed by the folder location where the JDK is installed.
[03:59] In case if you are facing any problem, you can take help from ChatGPT or any other website.
[04:04] If you still not able to fix the problem, you can always shoot your question inside Q&amp;A.

----------------------------------------
