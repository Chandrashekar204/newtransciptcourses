# 1.12 — Sequence flow of the Spring Security default behaviour

> Section 1: Getting Started

Instructor: In the previous lecture, we discussed about the internal flow of the Spring Security framework. Inside this lecture, I want to show you the sequence flow that we have discussed so far so that this sequence flow, it is going to be with you as a reference in future for any questions. You can see there are multiple important parties. The very first one is client, followed by Spring Security Filters, Authentication Manager, Authentication Provider, and User Details Manager, or User Details Service followed by Password Encoder.

So these are all the important components involved. In the very first step, the end user, he will try to access a secure page for the very first time without entering any credentials. Without what is going to happen behind the scenes, filters like Authorization Filter, Abstract Authentication Processing Filter, and DefaultLoginPageGeneratingFilter, they all going to work together and display a login page to the end user to enter the credentials.

Once the end user entered his username and password, the details will be processed again by the Spring Security filter. This time, the filters like UsernamePasswordAuthenticationFilter is going to extract the credentials from the request and populate the authentication object. The populated authentication object is going to be provided as an input to the AuthenticationManager implementation, which is ProviderManager. So inside this ProviderManager, we have an authenticate() method.

The same is going to be invoked, and internally this ProviderManager, it is going to iterate all the applicable authentication providers. In our scenario, the AuthenticationProvider, which is going to be invoked is DaoAuthenticationProvider. So inside this DaoAuthenticationProvider also, there is a authenticate() method. The same authenticate() method is going to be invoked by the ProviderManager. So the AuthenticationProviderImplementation, it can't authenticate the user by itself.

It is going to take help from two other components, which are InMemoryUserDetailsManager, which is the implementation of the UserDetailsManager class, and PasswordEncoder to validate the password. So basically, first it will try to load the user details from the memory with the help of these InMemoryUserDetailsManager. Post that with the help of these PasswordEncoder, it will try to validate whether the passwords are matching. If the passwords are matching, the successful authentication details is going to be returned back to the ProviderManager.

From ProviderManager, it will reach to the security filters and at last, the security filters, they are going to store the successful authentication details inside the security context object for future use. Once these details are stored at the end, the rest API response will be returned back to the end user. So here you may have a question, which is nowhere we are invoking the rest API, which is welcome, so don't worry about that. The Spring Security framework remembers what is the API that end user is trying to invoke.

If all the authentication is successful, it is going to invoke the rest API, and the response is going to send back to the filters of the Spring Security framework, which will send back to the client application. Have this sequence flow for your reference. I also have an high level sequence flow, which is another flavor of whatever we discussed so far. If you feel the previous slide has some too much information, or it is too much cluttered, then use this sequence flow.

So this also has the same kind of details but with a different style of representation. So first filters from filters, Authentication object will be populated, followed by ProviderManager, followed by AuthenticationProvider, followed by UserDetailsManager, and PasswordEncoder. The same will come back eventually to the client. I hope you like these sequence flows. Like I said previously, we are going to revisit all the internal working of the Spring Security framework at regular intervals of time based upon the new configurations we are exploring throughout the course.

And in the same process, I'm also going to update these sequence flows and provide you the updated slides as well. Thank you, and I'll catch you in the next lecture. Bye.

----------------------------------------
