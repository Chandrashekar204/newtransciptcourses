# 15.17 — Social Login integration with the help of KeyCloak

> Section 15: Securing EazyBank using OAUTH2 and KeyCloak

Instructor: Keycloak is a very big product and it has lots and lots of features. Any enterprise organization, they should be able to use this product without any issues. Though it is open source, all the features that are required by the enterprise organizations are present inside this product. If you want to learn everything about Keycloak, it requires lot of efforts. Usually the developers, they don't have to know everything about the Keycloak.

In real projects, there'll be a separate role with the name Keycloak admin. So these Keycloak admin, they need to know everything about the Keycloak. If we start talking about Keycloak, it's going to take 10 more hours. So that's why on a high level, I try to provide most important information around the Keycloak. In future, whenever you have some questions around the Keycloak, you can go to their website and they have a very good documentation.

If you can click on these guides, you'll be able to see lot many guides, like how to configure Keycloak for production, running Keycloak in a container, Configuring TLS, Configuring the database, so there are good amount of guides present inside this page, which you can explore based upon your requirements. Similarly, we also have detailed documentation. If you can click on these docs, we have various types of documentation. If you're looking from developer perspective, you need to click on the server developer, whereas if someone is an administrator, they need to open the server administration.

Similarly, if you're looking to understand the REST APIs exposed to by the Keycloak, you need to click on these administration REST APIs. As a last step inside this section, I'm going to explain you how to set up social login with the help of Keycloak. It is going to be super easy. You just have to go to these identity providers. Here, under the social login, you can see there are many options that we can use to set up inside our login page. I'll try to select the GitHub option, and inside this page, we need to provide our client ID, client secret, which we received from the GitHub during the registration process.

So inside my GitHub, I'll try to create an OAuth 2 app. So let me go to settings. Inside the settings, I can go to developer settings option and click on these OAuth apps. As of now, you can see I don't have any application. So let me click on this button. And here, I'm going to provide the application name as eazybytes. Coming to the homepage URL, I'll just try to give the homepage URL of Angular application by giving local host 4200/home. Next, we need to provide the authorization call back URL.

So here, you can't give whatever you want. We need to give the URL that is recommended by the Keycloak. So Keycloak is asking to configure these redirect URI inside our GitHub OAuth 2 app. So let me copy the same and mention the same here. Once I entered all these details, I'm going to click on this register application. And with that, I'm going to get a client ID. So let me take this client ID and mention here. Next, we need to generate a client secret and paste the same here.

So here, I'm going to generate a new client secret. Once a client secret is generated, I can try to copy the same and paste it here. So let me go to the end of the page and click on this update application. With this, we should be good. Inside the Keycloak also, let me click on this add button. You can see here, I got a successful message. Now, if we try to go on login, the Keycloak, it is also going to give me an option of social login. So let me show you the demo very quickly.

So this is my UI application. Let me click on this login button. This time you can see we have an option of GitHub social login. If I click on this GitHub social login, it is going to ask the end user to enter their GitHub credentials. As of now, we are on the GitHub login page. So let me enter my GitHub credentials. Once I enter the GitHub credentials, I'm going to click on the sign in button and authorize the same. Right now, we are seeing an option to configure the multi-factor authentication.

This is happening because since a new user came and trying to log in with the GitHub, a new end user profile is going to be created behind the scenes inside the Keycloak auth server. And since Keycloak is considering this as my very first login, it is asking me to configure the OTP app. I'll try to complete this registration by opening my Google Authenticator and scanning this code. Once the registration is completed, I'm trying to enter an OTP, which is 480991.

Let me click on the submit button and you can see, I am logged in into the application. You can see this is my name that is fetched from the GitHub profile. But if I try to click on this accounts, balance, cards, nothing is going to happen. And if I click on this loans, I will not be able to see any loans information. This is happening because whatever end user right now logged in with the help of GitHub, this end user does not have any roles configured.

Can I go to the GitHub auth server and configure my own roles to the end user? Off course not. I can't do this. GitHub is not going to allow me to do that. So that's why social logins, they're not going to be useful or helpful for the enterprise applications. They're not going to give you the freedom to configure whatever roles you want. But I just showed you this demo so that you are clear on how to integrate social logins with the help of Keycloak.

I hope you're clear. With this, I'm concluding this section. In the next section, we can try to build our own auth server with the help of spring authorization server. Thank you, and I'll catch you in the next section, bye.


########################################
