# Modify the Jenkins URL

*Section: Jenkins Tips & Tricks*

Instructor: Hello and welcome back. In this video we're going to learn how to change the Jenkins URL. So remember that in this case we created a local DNS, but this actually is hidden the IP address of our machine. So if we go to Manage Jenkins, you're going to see a horrible error in here. And this error is because in the initial setup when we created the user, the URL, everything, we actually gave the IP of our machine.

That's why we have this error. So let me show you, if we go to the Configure System again, and here we scroll down a little bit, looking for Jenkins URL. Let me look for it here under Jenkins Location. You're gonna find out what I'm telling you. And this is that we have here the IP of the machine. And remember that here we should be using the DNS. So we're gonna call it like jenkins.local. Now this is the current Jenkins URL, and that's the URL that we're using.

But doing this, Jenkins now knows that the URL which is going to be accessible, is this one. And this should fix the error. So let's Save this, and let's go to Manage Jenkins again. And as you can see here the error is gone, which is pretty cool. So now we fixed this small issue that we had. You can find this useful if you have a real DNS, because people is going to be accessing your Jenkins server using that DNS.

And then you probably want to have that correctly configured on your URL. So this is it for this video. You know how to change the Jenkins URL to point to your current DNS. So I'll see you in the next lesson.
