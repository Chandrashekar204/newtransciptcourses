# 1.13 — Understanding on how multiple requests work with out credentials

> Section 1: Getting Started

Instructor: Inside this lecture, let me try to explain you how Spring Security framework is trying to handle all the subsequent requests coming from the authenticated user. We know by default, if we try to access a protected page very first time, we'll be redirected to your login page where we need to enter the credentials. Once we are authenticated, from the next time onwards, if you try to access any protected API or MVC path, you're not going to be asked for your credentials one more time.

So, here, I'm trying to refresh this page multiple times, but still my Spring Security framework is not asking any credentials. Let's try to understand how this is working. For the same, I'm going to open the developer console inside my browser. And I'll go to the Applications tab. And inside the Applications tab, look for Cookies. And under the Cookies, open the localhost 8080 where our application is deployed. Here, you can see the Spring Security framework, it created a cookie with the name JSESSIONID and it also has a value against it.

So as long as we're trying to access the protected API with these JSESSIONID cookie and with this value, we are going to get the successful response. So if I try to refresh one more time, you can see we are getting the successful response and the value is the same. As a next step, I'm going to tamper this cookie value by right-clicking on it and selecting this Edit Value option. So, here, instead of E, I'm going to give some other value like C. And with that, we tampered the JSESSIONID value.

And for this value, in the backend server, there is no security context details. So what is going to happen this time? This time if I try to refresh the page, this cookie value is going to be sent by my browser to the backend server. And since my Spring Security framework can't find any saved security context details, it is going to redirect me to the login page. So I'm trying to refresh my page. And you can see, we are getting a login page. So this login page right now also has a JSESSIONID value.

To this JSESSIONID value, behind the scenes, the Spring Security framework, it is going to remember this JSESSIONID value belongs to an unauthenticated user. That's why as a next step, when we try to log in into the application and once the authentication is successful, we are going to get a new JSESSIONID value. So let me show you the same. For the same, I'm going to enter the username as eazybytes followed by 12345 as a password. As soon as I click sign in, you'll be able to see this value is going to be changed.

Right now the value started with 273. So let me click on the sign in button. And you can see, we got a new JSESSIONID value. To this JSESSIONID value, behind the scenes, Spring Security will map to a successful authenticated session where my authentication details, they're going to be stored and they'll be reloaded and reused every time when I try to access a protected API. This way, Spring Security framework, also doing a smart job of not invoking the actual authentication every time.

If you try to invoke the actual authentication for each and every request, then definitely it is going to have some performance impact. But by using this JSESSIONID cookie, the Spring Security framework is doing a smart job here. off course, I also want to highlight, this is the default behavior of the Spring Security framework. There are better and advanced approaches also available, like JWT tokens, OAuth2.0 framework, OpenID framework. So all these advanced topics we're going to explore throughout this course.

As of now, inside this section, we just built a very basic application and I just gave the quick introduction about the Spring Security framework, how the internal flow works. But more and more we are going to discuss in the coming sections. Slowly, section by section, we are going to enhance our application. And in the same process, I'm going to teach you all the approaches available inside the Spring Security framework. Before I try to close this lecture, I want to highlight you that every section code I'm going to upload into this GitHub repo, the same GitHub repo I have highlighted at the starting of the course.

Once you open this GitHub repo, you can go to the section1 to find the section1 related code. So please refer to the same code for any questions. And like I promised before, I'm going to keep update this code every quarter whenever a new major version of Spring Security released. With this, we can close this section. And we discussed a lot throughout this section. My humble request is take regular breaks between the section so that you won't feel bored or you won't feel exhausted with all the new information that I'm trying to share.

Thank you, and I'll catch you in the next lecture. Bye.


########################################
