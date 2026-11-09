# How to Self-Host n8n Locally on Your Own Machine with Node.js (Macbook)

*Section: Self-Hosting n8n Locally*

Welcome. In this quick tutorial, I'm going to show you how to install anything locally on your machine if you are using iOS operating system. So if you have a MacBook. In the previous lesson I showed you how to self-host n810 on your own virtual private server. That setup is ideal if you want your automations running 24 over seven with access from anywhere and still working even when your computer is off.

It also gives you more control over resources, so your local machine's power does not limit you. And it's stable, flexible, and a great option if you build serious workflows or offer it as a service. But maybe you just want to experiment with n810 or test things locally without testing up a full server. So it's super practical if you are just getting started. Want to learn the platform or build workflows offline?

So in this video I will show you how to install locally on your own machine. It's a great option because you can use N810 completely for free under the license. And we'll be using NodeJS, which makes the process super simple. So let's jump in. So first thing first. Google and GitHub. Is the first link. So for code workflow automation platform. Click on it. As you can see the code is publicly available for free.

It has a lot of stars which means N810 has big and strong community and a lot of people are using it. So a lot of no code builders and developers love it. So once you are on the page, scroll down. You can read the documentation if you want to, but we are looking for a quick start so you can see you can try instant NGP which requires no JS or if you know how to use Docker, you can install N810 using Docker, which is a little bit more technical.

But in this video we are going to use NodeJS. So just click on it. Now as you can see NodeJS is used to run JavaScript everywhere, so it's free and open source. Cross-platform JavaScript runtime environment that lets developers create serverless web apps. Command line tools and scripts to download Node.js. It takes just a minute. Now simply click on the file to start the installation process. Click next.

Accept the terms in the license agreement. Next. Automatically install the necessary tools. Next. Install. Confirm. Let's wait for the installation process to be completed. Now click on finish. All right. So once Node.js is installed we need to install N810 globally on your machine. I'm going to open up my terminal here. And I'm going to type a simple command. Sudo. NPM. Install. And hit enter. Now we need to provide password to give it admin access.

What this command does is it installs n810 permanently on your system. So if you were to just type Npx N810. Like you might see on the GitHub page. That would only install it temporarily. So you would need to run that command every time you want to use an A-10, and you would have to add a bit every time as it fetches all the dependencies. So it's not great. So by using the global install we are setting it up once.

And we are done. Now once we start let's run another simple command to open our localhost. So simply type n810. And hit enter. And you will get a URL with your localhost that you can paste into your browser. So let's copy it. Let's open browser. Past here for the first time, you will get a window to create an account. So just provide your name, email and password and you will land on this main dashboard page.

From here you can access this main dashboard using this localhost URL anytime now. If it terminates or seems to stop working, just refresh the web page and it should be good to go. Now this is really important. You need to remember that every time you want to run your local instance, after you turn off your MacBook, you will need to open terminal and type N810, and then you will have access to your dashboard where you can build your agents and automations.

So when I press enter now, it will load up and launch N810. So now I can use this localhost URL as a server and just simply paste it to my browser and it will launch my N810 instance. Thanks for watching and see you next time.
