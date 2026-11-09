# How to Connect WhatsApp to n8n in 6 Minutes

*Section: How to Set Up Credentials in n8n: LLMs, APIs & Messaging Tools*

Before we jump into configuration, just quickly to give you some insights. Why using WhatsApp as a communication channel is so important, and why almost every business should use it. Did you know that WhatsApp is one of the fastest growing communication channels for businesses? Over 50 million businesses are already using WhatsApp to connect with their customers, and the app has over 3 billion users globally.

WhatsApp messages have a 98% open rate, compared to just 21% for email, and 68% of users say WhatsApp is the easiest way to reach a business. It's less common in the US but is very popular in Europe, South America and Asia. Now let's move on to the integration part. First, we need a trigger to activate our workflow. So we'll start with the WhatsApp business cloud node. So search for WhatsApp. Choose WhatsApp Business Cloud.

And choose on messages. Basically, this node acts as a trigger it listens to for incoming messages on your WhatsApp account. Now we have to set up credentials to connect to our WhatsApp business account. So we will need our client ID and client secret. So we need to get it from Facebook business account. Since WhatsApp business is managed under meta. So go to business dot facebook.com and log in with your Facebook account.

If you are already logged in, it will take you to your Business Manager dashboard. If you have never used Facebook Business Manager, you will need to create a business portfolio. So go to business.facebook.com slash settings and provide all the required details like your business name, email and any other information requested and click Create Business. Now choose the business portfolio you have created.

And in your business manager, look for the account section on the left hand menu and click apps. Now click add and create a new app ID. Here you have to provide an app name. So let's say an app contact email. So. Then click on next. Scroll down. Choose. Other. Next. Business. Next. And create app. Now click on the app you created. App settings. Basic. If you remember, we are looking for an app ID and App Secret.

So this is our app ID. Copy it. Go back to Nan. Paste it here. Show up secret. Then copy app secret. Paste it here and test connection. So now let's set up WhatsApp node to send replies back to the user. So this will allow your agent to respond to messages automatically. Search for WhatsApp. And choose send message node. Now we have to provide access token and business account ID. So let's go back to our business manager account.

Go through API setup. And here you have to generate access token. And then copy this access token to paste it here. And you can find business account ID. Right here. Let's copy it and paste it here. Then hit Test connection. Just the last step. You need to choose your business mobile number. Or you can use the test number to test the connection.
