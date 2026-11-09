# How to Connect Google Services to n8n (Only for Self-Hosted Version)

*Section: Old Course Videos*

If you want to use Google services like Gmail, Google Drive Sheets, docs in your n810 agents and automation, you have to set up credentials. So if you are using the paid cloud version of N810, it's very simple. You just need to sign in using your email account. So I'm going to show you how. Um. Basically every time when you want to use Google Apps, let's say Gmail. And you want to use a trigger. We need to create new credential and simply sign in with Google.

Or another way to do that is to go to overview. Go to credentials. And sign in here and your credentials will be automatically saved for the next workflows. So you don't need to do it over and over again. But if you are self-hosting, anytime, you have to stop credentials manually, and in the next part of this tutorial, I will show you exactly how. First we need to trigger to activate our workflow.

So click on the add first step, then select trigger manually. To get started we will set up a Google Drive node. So let's search for Google Drive. Select Google Drive. Then we have to select actions we want to perform. So in this case we want to download file from Google Drive. So select this module. Now we have to set up credentials. So click on this little pen here. As you can see I already set up my Google Drive account.

So let's do it from scratch. Click on the create new credentials. So you see that N810 requires a client ID and client secret to connect to your Google account. So this means we need to set up credentials in Google Cloud Console, which is what we will do next. Now we are gonna open docs because we need to set up our Google Cloud account. Scroll down and right here under prerequisites click on Google Cloud.

Now we have to go to our console. So click on console. Now we have to create our project. So let's do it from scratch. Click on New project. Let's name it N810 demo. Click on create. Google cloud will create our project. So this project is where we will set up permissions for N810 to interact with your Google services. So now that the project is created let's open it. In the left menu go to APIs services.

And on or off console. Screen. Choose. External. Recreate. Name it something recognizable, like Google integration. You need to provide support. Email. Scroll down. Provide your developer email address. Click save and continue. Keep the scopes. And hit save and continue. Under test users, add your email address as a test user and hit save. Now we need to provide authorized redirect URL. So go back to n810.

Copy this URL. URL. Paste it here. And click create. Now Google generated a client id and client secret. So copy the client ID. Go back to n810. Paste it here. Copy client secret. I pass it here. Click sign in with Google. A Google login screen will appear. Select the account you added as a test user earlier. And grant the necessary permissions like access to Google Drive or Gmail. Click continue.

And continue. So once authorized, Nathan will show a green status indicator and confirming the connections was successful. So now we are connected. Even though the credentials are connected, we are not done yet. We need to enable the APIs for the Google services we plan to use. So go back to Google Cloud. Go to enabled APIs and services. Search for the API you need like Google Drive API and click enable.

And repeat this step for other APIs like Gmail API, Google Docs API, or Google Sheets depending on your work workflow requirements. Once enabled, these APIs will allow an end to communicate with Google services. And that's it. You have successfully set up Google credentials in N810, giving you full access to Google services for workflows.
