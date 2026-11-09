# 7.9 — Listening Authentication Events - Theory

> Section 7: Spring Security customizations for most common use cases

Instructor: Many times inside real applications, we may have requirements to handle the authentication events. For example, on successful authentication, you may want to send an email to an end user saying that you have successfully authenticated, just informing the end user about the login operation. This might be required for the super critical applications, and similarly, in the scenarios of authentication failure also, you may want to send an email or you may want to make an entry inside the database that so and so failure attempts happened.

So, these kind of requirements are very common inside real applications. To handle these kind of requirements, Spring Security is going to publish events whenever an authentication is going to be successful and whenever the authentication is a failure. We have an event with the name AuthenticationSuccessEvent, so this is going to be published by the Spring Security Framework whenever the login operation or the authentication operation is successful.

On the similar lines, Spring Security's also going to publish an AuthenticationFailureEvent in the scenarios when the login operation is failed due to invalid credentials or due to any other reason. So, these events, they are going to be published by a class, DefaultAuthenticationEventPublisher, inside the Spring Security Framework. We as developers, if we want to execute some business logic based upon these events, we don't have to make a lot, many changes.

We just have to build event listeners to listen to these success events and failure events. So, how to do that, it's very simple. We need to first create a bean. Inside this bean, we can define normal methods, like onSuccess(), onFailure(). These method names can be anything, but please make sure these methods are accepting the input, same as the AuthenticationSuccessEvent and the AuthenticationFailureEvent, or AbstractAuthenticationFailureEvent.

Sometimes, failures can happen due to multiple reasons. That's why Framework is going to give you all the failure details. Inside these methods, as of now, I just have some logger statements. For example, whenever the AuthenticationSuccessEvent publishes, I'm going to log this message, which is, "Login successful for the user", and what is the username. So, how to get the username? From the success event, I can invoke the getAuthentication() method, and inside the Authentication object, we know we are going to have the named details of the logged in user, the same I'm trying to use here.

And in the scenarios of failure authentication, I'm trying to log an error() message saying that login failed for the user due to the reason, and to this logger message, I'm trying to upend what is the current authenticated user who is trying to authenticate with the help of these failures.getAuthentication().getName(), and similarly, we will know what is the reason if you try to invoke this method, which is getMessage() with the help of getException() method, but we need to make sure we are mentioning these @EventListener annotation.

So, these annotations are not specific to Spring Security Framework. These are from the Spring Boot Framework. When you mention these annotations, what is going to happen is these methods, they're going to be continuously listening for these events, like AuthenticationEvent and AbstractAuthenticationFailureEvent. I hope you are clear. The Spring Security, always, it is going to shout your result, like whether it is a success or failure with these events.

We as developers, it's our responsibility to listen to them with the help of the EventListener annotation, and inside these EventListener methods, we can write any business logic that we want to execute. To keep things simple, right now, inside these methods, I'm just trying to log the messages, but in real applications, your requirements may be more complex, like sending an email, making an audit entry into the database. The requirement can be anything, but the process is going to be similar to what we have discussed.

I hope you're clear about this theory introduction around the authentication events. In the next lecture, let's try to implement all these authentication events-related logic inside our Spring Boot application. Thank you, and I'll catch you in the next lecture, bye.

----------------------------------------
