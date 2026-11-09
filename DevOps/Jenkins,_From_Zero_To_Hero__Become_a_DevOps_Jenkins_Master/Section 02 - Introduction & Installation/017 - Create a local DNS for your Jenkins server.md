# Create a local DNS for your Jenkins server

*Section: Introduction & Installation*

Instructor: Hello and welcome back. In this video, we're gonna be changing this IP because we're going to start using a DNS, local DNS. So for doing this, we need to open up notepad, and we're going to click on, right click, run as administrator. When we are here, let's select the file location, open. Let's go to your Windows partition. In my case, it's Windows C. So let's look for Windows. Let's look for System 32 here.

Okay. Let's look for drivers. And in drivers we click on "etc." And after that here we just click on all the files. When we are presented to this we're going to choose the host file. And what we are going to do is to graph the IP address that you can select from PuTTY or from your web browser. And we're going to paste that IP here. Please don't include this http, so the IP only. And after that you can give a name that you want.

Any name, it's okay. So for now we're just gonna say like, Jenkins.local, and we're gonna say file, save. After that, you can close it and you can open a new tab, and you can type Jenkins.local colon 8080, hit enter, and magic. You have now created a local DNS. So for this, we can reach Jenkins using this, and even we can modify our PuTTY session in order to change the IP and start using the DNS. So if you wanted, you can just, instead of using the IP address here, you can use the DNS that we have just created, which is Jenkins.local.

So I'll see you in the next video.
