# Integrate Jenkins and AWS Simple Email Service

*Section: Jenkins & Email*

-: [Instructor[ Hello and welcome back. In this video, we're going to learn how to integrate AWS simple email service with our Jenkins service that we already created. So we're gonna go and sign it in my account. And once you are logged in, you are going to click on the services tab and you are going to look for SES, which stands for Simple Email Service. So you're gonna click on this and that's going to redirect you to this part.

So the first thing that we need to do is that we need to verify a domain or an email address. If you have a domain and you can go ahead and register that in here. Or you can go and register your current email address. So I already registered my email so I'm just gonna go ahead and remove this so you can see how easy this is. You just need to click on verify a new email address and you post your address in here, your email it's okay, and then you're going to click on verify this email.

Then you close this, and if you go to your email, you're going to see a new message the Amazon sends to you. And the only one thing that you need to do is to click on the link that's provided. And as you can see, it's successfully verified. So we're going to go, we're gonna close this. And if you go to your console and refresh, you're gonna see that your mail is already verified. So that's pretty cool.

Once you have your mail verified, the second thing that we need to do is that we need to start configuring our Jenkins service. So to do this, we're going to go to the manage section, configure the system, and once you're here, you're gonna scroll down until the end and you're going to see something that says email notification and some fields that you need to populate. So we're going to go to advance in here and we're going to provide the SMTP server.

What is this? So if we go to the AWS console and we'll look for SMTP settings, you're going to find the server that you're going to use in here. So we're gonna copy this name and we're going to paste that name in here. We're going to leave this empty and we're gonna click on use SMTP authentication. So we need to provide a username and a password. So let's go ahead and create my SMTP credentials in here.

Let's click on that and I will just do something like Jenkins test mail. I will go to create, and then I will show my credentials. Don't worry, I will delete them later. So I will click on download credentials. I'm just gonna copy this username and that's going to be the username in here. I'm just gonna copy the password and that's going to be the password. So let's paste that in here. Now we're going to click on use SSL.

And if we go again, let's click on closing here. And let's go back to simple email service. And if we go to SMTP settings, you're going to find out the ports that you can use. This case, let's choose the 465 port, and we're gonna copy that. We're gonna paste that in here. And it says reply to address. So we're going to give our current address. And now we're going to click on test configuration by sending a test email.

And before testing it, we need to scroll up a little bit and we need to go to the part of the Jenkins URL here. Under this URL, it says System Admin email and we're going to put our email here again. And finally, if we copy this and we scroll down a little bit, remember that if we uncheck this and we check this back, this is going to ask for the test recipient. So we want our mail to be the recipient.

So we're gonna copy this and we're gonna click on test the configuration. And we need to wait for a while for some seconds until the mail gets sent. It was already sent, as you can see here. Now, if you go to your email, you're going to find out your current email in here. So you can see this is exactly the same time. So let's open up here. And, okay, this is a little bit something like that. Is it safe?

Because we know that we actually did this. And as you can see, we're having a mail from Jenkins using Amazon Simple Email Service which is pretty cool. If for some reason you can't find your mail in here, please try to look for that in the spam section because as you saw before, Gmail likes to block this kind of messages. So you can just click on Report Not Spam and then you're going to have those mails on your inbox.

And this is pretty cool. So as you can see now, your integration is working and you can receive mails from Jenkins on your email. So please make sure that this port is reachable from your machine. I mean, for example, your ISP could be blocked that port or if you are at your office, maybe that port is blocked. Make sure that you can access this port because otherwise you're going to probably have errors like connection timeout or something.

But if you're using your home internet, your home connection, you shouldn't have any problem. So this is it for this video. I'll see you in the next lesson.
