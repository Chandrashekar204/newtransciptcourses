# 14.1 — Introduction to the agenda of OAUTH2 implementations and demos

> Section 14: Implementing OAUTH2 using spring security & social logins

Instructor: Now is the time to start playing with the OAUTH2 framework or OAUTH2 standards inside our own Spring Boot applications. To show you the demo of OAUTH2, I'm going to take two different approaches. Inside the very first approach, I'm going to build a Spring Boot application. Inside the Spring Boot application, I'm going to have some secure pages. So to access these secure pages, I'm going to allow my end user to use the social logins like GitHub, Facebook.

So using these social logins, my end user should be able to access my secure webpage inside my Spring Boot application. So this is one approach that I'm going to take. The other approach is we already have the Easy Bank Spring Boot application. Inside this Spring Boot web application, we have some secured APIs. All these secured APIs, I'm going to protect them with our own Auth server. So I'm going to build an Auth server with the help of Keyclock.

Apart from Keyclock, I'm also going to use the newly introduced Spring security Auth server. Using Spring Security Auth Server project, we should be able to build our own Auth server from scratch. So here, I'll just mention Spring Auth server. The reason why I'm taking these two different approaches is inside the very first approach, we are going to use the social logins. So whenever we are using the social logins in this scenario, we are never going to build our Auth Server.

We are just going to leverage the Auth server belongs to other organizations, and this approach will work only for simple applications like blog applications or some single page applications where they don't have lot of business functionality. Whereas for real enterprise applications, like a bank application or a insurance application, for all such applications, the organization, they have to build their own Auth server either by leveraging the products inside the market like Keyclock, Okta, or they can build their own Auth server with the help of Spring based Auth server library.

We are going to explore all these approaches so that you have enough information about all these scenarios. Inside this section, we are going to focus on this approach, which is the approach one. In the coming sections, we are going to talk about the approach two where we are going to leverage Keyclock and Spring based Auth server for the Easy Bank application. I hope you're clear with the plan. In the next lecture, let's try to create a simple Spring Boot application with a secured path inside it.

Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
