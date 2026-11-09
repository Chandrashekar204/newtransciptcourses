# How to Update Your Locally Self-Hosted n8n Instance with Node.js

*Section: Self-Hosting n8n Locally*

Welcome back. In this video, I want to quickly show you how to update your local N810 instance. If you are self-hosting a n810 on your own machine using NodeJS. So this is super important because the N810 team pushes updates all the time. New features, improvements, bug fixes. So they roll out updates regularly and keeping your local version of N810 up to date means you don't need you. Don't miss out anything and your N810 instance will work perfectly fine.

So let me show you how to how simple it is. First thing first we need to check if an update is available. So open up your local N810 instance in the browser. And now if you go to the right bottom corner and click on your name on this on this three dots and then go to settings. You might see a red dot at the bottom. So currently my version is up to date so I don't need to update my instance. But if you see the red dot, that means there is an update available, and it's probably a good idea to to update your instance.

Now, before updating, we need to shut down the current instance of N810. So just simply go back to your Node.js command prompt. So open this terminal window. So the one you use to start n810 and close that window. Now if you try refreshing your browser tab when it was running. It won't load anymore because that was expected because the server just shut down. It runs over the node. Now if you visit the GitHub page you will see just how often they push updates.

So sometimes multiple times a week. And for example, you might see that the last update was committed to GitHub a 54 minutes ago. We have some 14 hours ago four days this last month. Last week? Yep. So as you can see, the team shipping features and fixed boxes all the time. So this is very active. And we need and we need to keep our N810 instance up to date. So you don't need to update your N810 instance every day, but doing it from time to time is strongly recommended to keep your setup running smoothly.

There is also a dedicated page for tracking all the updates and releasing notes. I'm going to leave the link to this web page in the resources section, so you can keep an eye on the new updates. All right. Great. Now let's actually update our instance. So let's open the Node.js command prompt again. This time let's type The n pm. Update. Dash G and a10. And then press enter. So this will take a couple of minutes depending on your internet speed and what's being updated.

So behind the scenes it's removing all the packages, adding new files and synchronizing everything. Alright, here we go. As you can see, in my case it changed to packages in one minute. So it wasn't a big update because I just installed the N810 locally for the sake of this tutorial review. Alright, great. Now as soon as the updating process is completed, you can simply type in N810 to start running N810 instance again.

Just wait a moment. Okay, so as you can see, we are not able to run our local instance yet because the process has not completed. So let's just wait a few more seconds. Okay. Everything is ready. So now when I reload this page to reset our instance. Now we get access back. Brilliant. So, yeah, there are two ways to start your local N810 instance. Just copy and paste the URL from the terminal to the browser, or just simply refresh the old tab if you still have it open.

Now your local N810 is now fully updated and ready to go. Just to let you know, you can absolutely continue working locally for most things like building and testing and experimenting. But for certain use cases like triggering telegram, WhatsApp or hosting workflows you want to share or sell a local setup will be not enough. That's when you need to move to a cloud hosted version. I already showed you how to use the N810 cloud version and pay for the subscription.

And also the second option was to self-hosting on the virtual private server. So these are three ways of using N810. So each method has its own pros and cons. So yeah this is how you can update your local N810 node instance. Thanks for listening. See you in the next lesson.
