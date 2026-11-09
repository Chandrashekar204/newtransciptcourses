# Create users manually in the Jenkins DB

*Section: Jenkins & Security*

Instructor: Hello and welcome back. In this video you are going to learn how to create users in Jenkins. Remember that in previous videos, we learned how to allow users to sign up for our Jenkins service. But what happens if we don't want users to be able to sign up? So we can manually create those users on the Jenkins database. So let's go to Manage Jenkins. We're gonna scroll down and we're gonna look for Manage Users.

We're gonna click on this, and in here you can see the user that was created using the sign up button. And in here you can see the first user that was created as a Jenkins admin, which is the admin user. So we can hit the Create User button, here, and then you're going to see exactly the same screen that you saw before when you created the signed up user. So let's give it a name like tom, password, 1234, 1234.

Full name's gonna be tom, and email tom@tom.com And if we hit the Create User button, then you are going to see a new user created, and you are going to see that it says Jenkins' own database. So if you go to the Manage Jenkins, and if you go to Configure Global Security, again, you are going to see here, in the Security Realm, that you have an option to integrate your current old server if you have one.

Here, you only have to type, as you can see here, the instructions, your LDAP://SERVER, and then if you want, you can just go to the advanced configuration. We're not going to cover this LDAP configuration in here because we're going to be touching only the Jenkins database. But if you have a LDAP server, then I am pretty sure that you already know all of this information. Now we're going to test the user that we created, which is the tom user.

Do you remember the user? So if we open up an incognito tab, and we look for jenkins.local, and we hit Enter, you are going to see the login section. But if we type tom, which is that user that we created, and we type the password, 1234 and you hit Enter, now you are going to see an error in here, which is Access Denied. But why? Remember that previously when users were capable to sign up, we actually created the user in that way, and that user was able to remove, to delete, and to do a lot of stuff only via registering.

So why this user is not doing the same thing? And well, the answer is because of the Jenkins plugin that we installed. So what happens if we log out in here and we login with the user that we created using the Sign Up button? Let's try 1234, Enter, and you're going to have exactly the same error. So as you can see now, Users by default are not able to do anything unless you explicitly define that.

So let me close this. And if we go to Manage Jenkins, to Global Security, remember that we actually delegated the power of security to our newly installed plugin. So that's why you are not able to do anything with new users unless you allow it. So this is it for this video. I'll see you in the next lesson.
