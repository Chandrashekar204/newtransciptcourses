# 6.4 — Environment specific Security configurations using Profiles - Part 1

> Section 6: Understanding Authentication Provider and Implementing it

Instructor: Inside any real-time projects, the code is going to be deployed across multiple environments. These environments are like production UAT, SIT, development environment. So development environment is for the developers to test their changes. SIT environment is a place where the system integration testing is going to happen, and UAT is a place where the user acceptant testing is going to happen. If the testing across multiple environments is successful, then the code is going to be deployed eventually into the production environment.

Any environment other than production environment, we call such environments as non-production environments or lower environments. The reason why they call them as lower environment is these are the environments where the testing of the applications or testing of the scenarios is going to happen. Once everyone is happy with the outcome of the testing, the application or the code is going to be deployed into the production. You might be scratching your head why this fellow right now talking about the production.

There is one interesting scenario that I want to address inside this lecture. Let me share more details about the same. Regardless of in which environments you're trying to use your application, any user has to enter their credentials to enter into the system. So there'll be a login page. Inside the same login page, everyone has to enter the username and password. We know the story and behind the scenes spring security is going to perform the authentication.

During the login operation, the person is going to enter the username and the password. This expectation is perfectly valid for the production environment because inside the production application, the real users, they're going to use the application. So who are going to use, they are real end users, but coming to the lower environment, the same login page is going to be available. And here who are going to use the application Inside the lower environment?

The QA people, the dev people or some business analysts. They're going to use the application to test some scenario. Many times I see in many organizations, they will set up the authentication in such a way that inside the lower environment they will ask only the username and the password can be any value. So the password, they can enter any value. So this is going to provide some convenience to the testers or convenience to the developers or any other people who are trying to access your application.

These people from your team, they already have to remember a lot, many things. That's why many times, especially from the UAT team or QA team, you may get requests saying that at least inside the lower environment, please allow me with any credentials that I enter. Off course, username, we can't allow any username because to the username, only the authorities are, or the roles or the data is going to be mapped. So there is no need of remembering the password here.

That's why as a developer, we should give some flexibility to the QA or dev or business analyst to access the application with any password, they can enter 1, 2, 3, 4, 5, or any other password. That's why, as a next step, we are going to explore this scenario, how to conditionally authenticate the end user based upon the environment where the authentication is happening. Inside Spring Boot, we have a concept called profiles. Using these profiles, we can conditionally load the properties.

We can conditionally load the beans. We can conditionally create the beans. So let's try to explore these profiles concept to conditionally implement the authentication inside our application as a next step. I hope you are clear what we are trying to achieve. If something is not clear, don't worry. When we start implementing it and testing it, it's going to be super clear for you. Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
