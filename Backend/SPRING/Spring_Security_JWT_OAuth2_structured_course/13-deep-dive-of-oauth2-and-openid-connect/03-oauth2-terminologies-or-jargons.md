# 13.3 — OAuth2 terminologies or jargons

> Section 13: Deep dive of OAUTH2 & OpenID Connect

Instructor: During our discussions around the OAuth 2 framework or OAuth 2 standards, you will hear a lot of jargons, and you may not have any clue about these jargons. That's why, inside this lecture, let me spend very few minutes explaining about these jargons so that you'll be clear for all the discussions that we are going to make around the OAuth 2 standards in the coming lectures. The very first jargon that you may hear inside the OAuth 2 grant type flows is Resource Owner.

I'll try to explain all these jargons by taking our PhotoEditor scenario that we have discussed previously. In the scenario of PhotoEditor, the Resource Owner refers to the end user who owns the photos inside the Google Photos application. So in the scenario of PhotoEditor, what are the resources that everyone tried to get? The resources are images or photos. So who owns those photos? The end user. That's why we call the end user as Resource Owner inside the OAuth 2 flows.

The next jargon is Client. Client is an application which is trying to read the end users resources or the Resource Owner resources. So in the scenario of PhotoEditor, the PhotoEditor application, our website, it is going to be called as client because this is the application which is showing some interest to interact with the Google after taking enough permissions from the Resource Owner or the end user. The next jargon is Authorization Server.

So this is the server which knows about the Resource Owner. In other words, the Resource Owner should have an account inside these Authorization Server. In the scenarios of PhotoEditor, we can consider Google Auth server as the Authorization Server because it is going to have all the authorization logic. So always please remember server which is responsible to store the end user credentials and to perform the authentication and issue the access tokens.

So that component we can call it as Authorization Server. In the scenario of PhotoEditor, since Google is going to have a common authorization for all its other products, that's why I have mentioned these Google logo here. The next jargon is Resource Server. This is the server where the resources are going to be stored. If the client application want to read the resources or the images of the end user, the client application needs to reach out to the Resource Server.

We are calling this as a Resource Server because this is the server which holds all the resources, and it is going to expose enough APIs and services to the client applications so that they can consume and get all the resources that they want. So in the scenario of PhotoEditor, the PhotoEditor application, it is going to invoke the /getimages API, which is exposed by the Google Photos resource server. So when client application asks for the resources, obviously, the resource server will expect an access token before providing the response.

So how to get the access token, the client first has to reach out to the authorization server to get the access token. Once the access token is received, using the same access token, it can reach out to the Resource Server to fetch the resources. In smaller organizations, there is a good possibility that a single server can act as both resource server and auth server. As of now, the spring boot application that we have built so far, though, we're not following any OAuth 2 standards, we clubbed all our business logic and security logic into a single application.

That's why we can call our spring boot application as both auth server plus Resource Server. At last, the next jargon that you may hear is scopes. Scopes are the granular permissions the client wants, such as access to data or to perform certain actions. In the scenario of PhotoEditor, the auth server can issue an access token to client with the scope of only reading images. So since the scope is only read images, if the client application trying to invoke the Resource Server to delete an image, then it is going to get an 403 Error because it does not have enough privileges.

So these scopes, in other words, we can call it as authorities or roles that we have discussed in the previous sections. So just like how we have authorities and roles concept inside the Spring Security framework, very similarly, inside the OAuth 2 standards, we call them with the name or with the jargon scopes. So these are the very commonly used jargons inside the OAuth 2 standards. I hope you got some clarity. Once we start discussing about OAuth 2 standards in detail, I'm going to use these jargons a lot.

In the same process, you'll also get used to these jargons. Thank you, and I'll catch you in the next lecture, bye.

----------------------------------------
