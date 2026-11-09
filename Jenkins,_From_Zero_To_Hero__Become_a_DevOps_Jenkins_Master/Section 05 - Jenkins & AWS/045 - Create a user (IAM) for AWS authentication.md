# Create a user (IAM) for AWS authentication

*Section: Jenkins & AWS*

Instructor: Hello, and welcome back. In this video, we're going to learn how to create a user for authentication. So in order to upload our backup to AWS, we need to get authenticated. So this is what we're going to do. So we're going to click on the Services tab again, and we're going to look for IAM. IAM stands for Identity and Access Management. So here, we're going to create our user. So let's go to the left side and create and click on the User button.

Now let's click on Add a user. And now you can just give it the name that you want. So I'm just gonna call it, like, my name. And then we're going to click on Programmatic access. Now click on Next: Permissions. And here ,we're going to click on Attach existing policies directly. So we want this user to be able to connect to our S3 service. So we're gonna look for S3. And now I think that, for testing, AmazonS3FullAccess is going to work, but in the real life, you should only allow access to your bucket.

But to keep it simple, let's just click on AmazonS3FullAccess. So let's click on Next and now Next again, and you are ready to create your user. So let's click on the Create user button here. And now you are going to see that you have this secret access key here, and you have this access key ID in here, which is something like our username and password. So let's download this file, which is pretty cool.

Don't worry. Once I the video, I'll be deleting these access, so don't try to use them. And that is cool. So if we open up this credentials file, we are going to see that we have the access key ID and the secret access ID.
