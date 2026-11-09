# Integrate Jenkins and Gmail

*Section: Jenkins & Email*

-: Hello and welcome back. In this video, we're going to learn how to integrate Jenkins with Gmail. In the previous video, we learned how to integrate by using Amazon services. Now, if you don't have an Amazon account we're going to use Gmail. So you need to go to the configured system. And here we're going to modify only the SMTP configurations. So now we're going to be using the SMTP Gmail server.

So for that, let's go to SMTP Gmail server or settings, and you're going to find all this information in here. So this is actually free. If you have a Gmail account, then you can just configure this. If you don't have a Gmail account, what are you waiting for? Go ahead and create one. Okay, so I'm just gonna copy this and this is going to be our SMTP server. Now if we go to advanced, we're also going to use authentication, but in this case the authentication is going to be our email.

So in this case, my email is this one, and the password is going to be, of course, your password, your email password. And then we need to mark this, use SSL, because we're going to be using it. And the port, it's going to be four, six, five. You can find that port in here for SSL and I think this is everything we need. Oh, I'm forgetting something. You go to Gmail less secure apps. Let's click on the second result that says myaccount.google.com.

We're gonna click on this. So in this case, this is in Spanish. I don't know why, but don't worry. It's only asking you do you want a lot? If you turn this on, it means yes. If you turn this off, it means no. So we're gonna turn this on, and now you have a lot lesser secure applications. This is because from Jenkins, as I've said before Gmail doesn't like that kind of application so that's why it has some restrictions.

But if you turn on lesser secure applications then you're going to have no errors. So we already defined this. We're gonna copy this. And finally we're gonna click on test configuration by sending an email, and we're gonna paste our email in here. And let's click and test configurations using the Gmail settings. So let's wait. And as you can see, the email was successfully sent. Please make sure that you mark the toggle or the button to turn on less secure applications because otherwise you're going to have errors, and Gmail is not going to send your mail.

So as you can see here, we have some alerts about turning on our less secure application. But if you can see here we have our mail, which is sent, and that's pretty cool. So now we integrated our Jenkins server in Gmail to be able to send mails. In the next video, we're going to learn how to integrate these notifications with jobs. So I'll see you in the next lesson.
