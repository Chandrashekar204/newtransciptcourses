# Set Up Twilio and Import Phone Numbers for AI Voice Agents (VAPI & Retell AI)

*Section: Build AI Voice Agents with n8n, Retell AI, Eleven Labs & VAPI*

Welcome! In this short tutorial, I'm going to show you how to create an account on Twilio, which in short, is a platform where you can buy phone numbers and then import them into tools like VWAP and retail I. This will be essential for building the AI voice agents we are going to create in this course. Now, although you can buy phone numbers directly in retail, AI and Vaapi, there are some limitations on retail AI.

Outbound international calls are not supported, so if you buy a number directly there, you won't be able to make calls outside your country. And on Vaapi. The functionality to create phone numbers is only available for US based numbers. So if you need numbers from the other regions, you have to use the import phone numbers feature anyway. So the easiest and most flexible option is to buy your number on Twilio and import it into retail AI or Vaapi.

If you want to build AI voice agents on these platforms, you can always come back to this lesson and follow it step by step whenever you need to. Set up a voice agent with little AI or Vaapi. So let's get started. If you are new to Twilio, it's a communication platform that provides virtual phone numbers, messaging, and voice services in over 100 countries. And using Twilio, you can buy a virtual phone number and make calls as if you have a local presence in multiple countries.

And that's why we are using it. So if you are using Twilio for the first time, you will get a $15 shell credit. Usually it costs just $2 a month. So basically you have seven months for free. First, create an account. Now go to the phone numbers section. Which is in the left menu. then under manage by number. And search for a number in your country. After you have bought a number, we need to connect it to our agent via SIP trunking.

So go to search bar and search for SIP. Click on elastic SIP trunks. Give it a friendly name and click create. Now we need to configure the connection. And this is really important step. So please don't miss it. Otherwise it won't work. So under general We have to. Enable code transfer as I prefer and also enable transfer. Then under termination provides some name right here. Then scroll down. Create credentials.

So give it some friendly name username and password. Then click create. And that's it in this section. The next one origination we're going to add the origination URL. So let's copy it from the retail documentation I'll attach the web page as a resource for this lesson. So copy it. Add a new origination. Paste the URL here and click add. And on the numbers. Just add the number you bought on Twilio by clicking on add a number and add an existing number.

So you can select from the list. Now go back to termination. Copy this sip. Go to your retail account. And under phone numbers. Connect to your number via SIP trunking. And paste it right here. Also, you need to provide the phone number you just bought and click save. And now we successfully connected the phone number we bought to our agent on retail AI. Now let's actually look at how to set up a phone number in.

Your agent can actually make calls. So click on phone numbers. Create phone number. Now if you are based in the US you can use the number. So just enter area code and click create. And these numbers are completely free. And you can have up to ten of them in your account. So if you are outside the US like me you will need to use the import tab. So you need to go to Twilio, create an account, purchase a number and then import it here.

So once you buy a phone number on Twilio and the phone numbers in folio section, scroll down. You should see account info. Just copy this account ID. And paste it right here. The same for of token. Copy it. Paste it here. And your phone number. Then simply click on import from Twilio and that's it. Alright great. Once you successfully import the number from Twilio, you have to assign your voice agent you just created right here.

All right. That's it for this lesson. I hope it was helpful and see you in the next one.
