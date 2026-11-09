# Learn how to manage sensitive information in Jenkins (Keys, Passwords)

*Section: Jenkins & AWS*

Instructor: Hello and welcome back. In this video, we're going to learn how to manage sensitive information, such as passwords or keys in Jenkins. So remember that now in our script, we have one key which is the AWS key and then we have the database password. So this is actually sensitive information and we need to manage this information correctly. So for this, we're going to click on Credentials.

Now we're going to click on Jenkins. Let's click on Global credentials and let's click on Add Credentials. So in this case, we're going to add a secret text which means that we're only going to secret the text for the password and for the key. So in the ID we're gonna give it a name, which is, for example, MYSQL_PASSWORD, something like this. It doesn't matter. And then the secret is going to be the password.

So let's look for our Docker composed file. And remember that here we have the password for the database, which is 1234. So let's give that password here. 1234. Cool. And now let's click on the OK. So we already created our password in here for the MYSQL. So now let's do the same thing for the AWS secret key. So let's use a secret file, sorry, a secret text and the ID is going to be something like AWS_SECRET_Key.

And the secret, it's going to be the value that Amazon gave us when we created these credentials. So let's copy the secret access key and let's paste in here. Cool. So let's hit on OK. Now you have one sensitive data, which is your MySQL_PASSWORD. And this is actually secure because if you want to update it, you're going to see that you have here a lot of characters which doesn't allow you to see the real content.

And the same thing happens to this AWS_Secret_Key. If you wanna update this, then it's going to show you a lot of things in here and you're not going to be able to see the real content of this, which is pretty cool. So this is it for this video. You've learned how to create keys, how to manage sensitive data in Jenkins in order to secure this information. So I'll see you in the next lesson.
