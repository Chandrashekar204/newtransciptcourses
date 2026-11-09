# 16.7 — Updating Spring Auth Server to authenticate the end user using DB

> Section 16: OAUTH2 Auth Server using Spring Authorization Server

Instructor: I made very few changes inside my auth server so that it can start authenticating the end user by leveraging the database. Most of these changes may look very familiar to you because we already discussed all these concepts. So let's try to quickly revise these changes. So first I have created an authentication provider implementation inside the config package. If we can open this authentication provider, it is leveraging the UserDetailService implementation to load the user details.

You can see we are trying to get the username, password. The username, we are trying to pass to the loadUserByUsername() method to the implementation class of UserDetailService. So I also created an implementation class with the name EazyBankUserDetailService. So here you can see, we are simply loading the user details from the database by using these CustomerRepository interface. So we're populating the authorities and at last we're trying to create an object of User with the help of email, password, and authorities, the same we are returning from this method.

So inside the authentication provider, with the help of passwordEncoder(), we are trying to check if the passwords are matching after the hashing process. If the passwords are matching, we are going to create an object of UsernamePasswordAuthenticationToken, which represents an successful authentication. Otherwise, we're going to throw the bad credential exception. After these authentication provider and UserDetailedService, I also created couple of beans inside the ProjectSecurityConfig.

Towards the end of this class, you can see I have created a bean of PasswordEncoder with the help of this code, because right now all our passwords in the database are hashed using the decrypt hashing algorithm. So to leverage the same, I need to create this bean. Next, I also created this CompromisedPasswordChecker bean so that the authorization server will not accept any simple passwords during the registration process. As of now, we don't have any registration process supported by the auth server, but if needed you can build it by exposing an REST API.

The next change that I have done is inside the model package. I have created a model package, and inside this, I have created entities representing the customer table and the authority table. So these entity classes are exact copies of what we have discussed in the previous sections. Next, under the repository package, I have created a CustomerRepository. This is going to help me to load the customer details based upon the given email. With all these changes, now my auth server know how to authenticate an end user.

At the end, I also want to highlight about the DB configurations that we have done here. So please make sure you have started your DB container and you configured the correct details here. In the next lecture, let's see the demo of Authorization Code Grant Type flow and PKCE Grant Type flow end to end. Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
