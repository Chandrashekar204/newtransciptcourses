# 11.9 — Validating the JWT token expiration scenario

> Section 11: Token based Authentication using JSON Web Token (JWT)

Instructor: Every JWT token that we are going to generate is going to have a specific expiration time. Inside our JWTTokenGeneratorFilter, we have set the expiration time as around eight hours. If anyone tried to access this token after eight hours, it is going to be useless for them. The end user again has to restart the login journey to get a new token. Inside this lecture, let me show you a small demo where the end user is trying to access the token after the expiration time.

So what I'm going to do is I'll try to reduce this expiration time to 3000 milliseconds. That means my token is going to be valid only for three seconds. So once the changes are saved, I'm going to do the build. Once the build is completed, inside the Postman, I'm going to invoke the user API with the username and credentials. So let me clean my console and click on the Send button. So inside the headers, you'll be able to see there is an authorization header.

Let me copy this JWT token value and I'll go to the myAccount API and try to mention the JWT token value here. Before I try to click on the Send button, let me clean this console and make sure there is a breakpoint inside my catch block of the JWTTokenValidator. I'll also keep a breakpoint here at the starting. Now I'm clicking on the Send button. So we have received the JWT token and if I try to execute this code during the validation of the JWT token, we are going to get an exception.

So you'll be able to see I'm getting an exception, which is ExpiredJwtException. Here, there is also a detailed message which is, the JWT token expired so and so milliseconds ago and with this, the end user is not going to get a proper response. So if I release this breakpoint, you'll be able to see that we are getting the same 500 error with authentication type as bad credentials exception. As of now inside our catch block, we are always throwing the bad credential exception, but maybe here we can do a better job.

If you're interested, I will request you to build multiple catch blocks, catching different type of exceptions, like one catch block can handle the expiration scenario and the other catch block can handle the tampering scenario. Accordingly, you can throw whatever exception you want and on the client side also, based upon the exception type, you can have different handling business logic. But I'm assuming you are seeing the power of tokens, especially with the JWT token format.

We have so much flexibility on what we can send inside the payload and how we are setting the expiration time. We are ready to see the power of JWT tokens. Once we start discussing about the OAUTH2 framework, we are going to explore more about the JWT tokens. But now I'm assuming you're clear about the expiration scenario. Let me roll back the changes to the previous expiration time so that your token always going to have a expiration time of minimum eight hours.

Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
