# How to Self-Host n8n Locally on Your Own Machine with Node.js

*Section: Old Course Videos*

Welcome. In the previous lesson, I showed you how to self-host Nathan on your own virtual private server. That setup is ideal if you want your automations running 24 over seven with access from anywhere and still working even when your computer is off. It also gives you more control over resources, so your local machine's power does not limit you, and it's stable, flexible, and a great option if you build serious workflows or offer it as a service.

But maybe you just want to experiment with n810 or test things locally without testing cup full server. So it's super practical if you are just getting started. Want to learn the platform or build workflows offline? So in this video I will show you how to install N810 locally on your own machine. It's a great option because you can use N810 completely for free under the license. And we'll be using NodeJS, which makes the process super simple.

So let's jump in. So first thing first Google N810 GitHub. Is the first link so far code workflow automation platform. Click on it. As you can see, the code is publicly available for free. It has a lot of stars, which means N810 has big and strong community and a lot of people are using it. So a lot of no code builders and developers love it. So once you are on the page, scroll down. You can read the documentation if you want to, but we are looking for a quick start.

So as you can see, you can try it in instant NGP which requires Node.js or if you know how to use Docker, you can install N810 using Docker, which is a little bit more technical. But in this video we are going to use NodeJS. So just click on it. Now as you can see, Node.js is used to run JavaScript everywhere, so it's free and open source cross-platform JavaScript runtime environment that lets developers create serverless web apps.

Command line tools and scripts such as download Node.js. It takes just a minute. Now simply click on the file to start the installation process. Click next. Accept the terms in the license agreement. Next. Automatically install the necessary tools. Next. Install. Confirm. Lets wait for the installation process to be completed. Now click on finish. Now the terminal should pop up so you can install N810.

Now this step is optional but can be useful. So if you want to manage different versions of NodeJS, maybe you want to downgrade or switch versions. You can install a tool called NVM for windows. So as I said this is not necessary. But you can google NVM for windows. Open the first link. And scroll down to the last section. You see right here. Just click on it right now. And look for the. NVM setup zip.

So download it. You can unzip the folder and just run the installer. So this lets you easily switch between different node versions later which can help you if something is not working with the latest version. Now when we visit the NodeJS website, you will notice there are quite a few versions to choose from. So in the download section you can see all the versions right here. So most of the time the latest version works perfectly fine.

But once in a while a new release may cause some issues with certain tools, including ten. So if you ever run into problems, it might help to switch to an older version of node. So not the current one, the older one. So if you have already installed the NVM for windows, you can easily switch between versions with a simple command so you don't need to uninstall or reinstall anything manually. So yeah, it's not required, but definitely useful if you want to have that extra flexibility.

Alright, let's move on. Once you install the NodeJS, just simply go to the search bar and search for NodeJS. Node.js command prompt. Don't worry, you just need to enter a few simple commands. So here we need to run the command to install N810. So let's type npm install. G and then hit enter. So it will start downloading everything it needs. So this usually takes a couple of minutes depending on your internet.

And you only need to do this once. And then you can run n810 anytime from the terminal. Now. As soon as the packages are installed successfully, it will look like this. So now you can close this window. And reopen it. So open Node.js command prompt again. And now in the terminal we need to type n and press enter. And in about a minute or two and then restart running on your local machine. Now once this command is executed you will see a local URL.

So just copy it and paste it to your browser. Hit enter. And you will land on this signup page. So just fill in your email, first name, last name and password to create your local account. And once you are in you will see the Interface. Now when you shut down the NodeJS terminal, you will lose access to your N810 instance. So every time you want to start your n810 local instance, you need to go to Node.js command prompt terminal.

Type N810. Press enter. Wait a few seconds. And copy your localhost URL. And paste it to your browser. Or just refresh the page with localhost URL so you need to do it every single time. Alright, that's it for this tutorial. I hope it was helpful and see you in the next one.
