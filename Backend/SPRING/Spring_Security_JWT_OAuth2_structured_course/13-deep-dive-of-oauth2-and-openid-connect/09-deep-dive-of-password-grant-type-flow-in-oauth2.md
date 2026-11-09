# 13.9 — Deep dive of password grant type flow in OAUTH2

> Section 13: Deep dive of OAUTH2 & OpenID Connect

Instructor: Let's talk about Password Grant GRANT TYPE FLOW inside this lecture. This Password Grant Type Flow, few people they also call it as Resource Owner Credentials Grant Type Flow. I have highlighted a disclaimer here that this is duplicated and not recommended for production, though it is duplicated but still I want to explain this Grant Type Flow. The reason is very simple. Even today you have the legacy applications that are using this flow.

If you try to understand this flow, it's very similar to authorization code Grant Type Flow except with the small change. Inside this flow what is going to happen is that end user is going to hand over his credentials to the client application itself. So usually inside the Authorization Code Grant Type Flow are the Implicit Grant Type Flow or the PKCE Grant Type Flow. What is going to happen is the client application, it is going to redirect the end user to the login page of the odd server to enter his credentials.

But inside this flow, the client application itself is going to have their own login page where they are going to ask the end user credentials that he's maintaining inside the AUTH server. So once the end user credentials are accepted by this client application, it is going to make a request to the AUTH server with the details of user credentials, client to credentials. So both the client credentials and the end user credentials, it is going to send as part of the request to the AUTH server.

If all the credentials are valid as part of the step three, the access token is directly going to be issued to the client application. Using this access token, the client application can make a request to the Resource Server. If the access token is valid, the resource server is going to respond with the proper successful response. So it's a very simple Grant iFlow but the drawback of this flow is the end user has to belive the client application and provide his own credentials.

So there is a very good chance that this client application may misuse the end user credentials. So before it is trying to invoke the AUTH server with the end user credential, the client application may store the end user credentials somewhere inside its own database. Since this serious drawback is present inside this Grant Type Flow, this is no more recommended for any production usage but still you will see some organizations using this Grant Type Flow.

The reason is this flow is very simple to follow, but whenever someone is following this flow, they'll make sure this client application and this AUTH server, Resource Server, they all belongs to the same organization. So in this kind of setup, there is no chance that this client application can misuse the credentials of the end user because both client and AUTH server belongs to the same organization or the same project. In this kind of environment it is acceptable but still we should not use it.

We should always go for the OR to Grant Type Flow or the PKCE Grant iFlow regardless whether the client application and AUTH server belongs to the same organization or different organizations. With this information, I'm assuming you are clear why these Grant Type Flow is also called as Resource Owner Credentials Grant Type Flow, since the Resource Owner handing over his credentials to the client application. In other words, we can call this Grant Type Flow as Resource Owner Credentials Grant Type Flow or in simple words it is also called as password Grant Type Flow because the end user he's going to share his own password to the client application.

I have mentioned more details about this Grant Type Flow inside this slide. So like I said, inside the step two, both the client ID, client secret, scope, username, and password and the Grant Type Flow is going to be sent as part of the request to the AUTH server, so the grant type value we need to mention password whenever we want to use these Grant Type Flow. I hope you're clear with this Grant Type Flow. Unfortunately there is no option for me here to show you the demo of Password Grant Type Flow since Password Grant Type Flow is deprecated very, very long back.

This Grant Type Flow option is not available here but I'm assuming you are clear with our discussions. Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
