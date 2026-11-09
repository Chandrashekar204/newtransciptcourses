# 14.20 — Custom Checked Exception

> Section 14: Exception handling using try, catch and finally

[00:00] As of now, we are trying to build the exception handling logic based upon the exception classes provided
[00:07] by the Java library.
[00:08] But in real projects, you will definitely have requirements to build your own custom exception based
[00:16] upon your business requirements.
[00:18] Here you may have a question, which is why should I build a custom exception if we already have enough
[00:24] exceptions inside the Java library, the question is very valid.
[00:28] But please note that my friend inside real projects, you may want to throw the exception in a more
[00:35] friendly manner or in a more meaningful manner are based upon a respective scenario.
[00:41] That's why in any real project that you are going to work, definitely there will be a scenario to develop
[00:47] a custom exception.
[00:48] Let me show you on how to build our own custom exception inside this lecture.
[00:53] First I'm going to build a simple Java class.
[00:56] The class name I'm going to mention as AcceptAgeDetails.
[01:01] Inside this class we are going to write a main() method, and inside this main() method we are going to
[01:07] write a logic to accept the age details of an end user. For the same
[01:12] first, I'm going to write the Scanner related logic, where I'm trying to create the Scanner object,
[01:18] and to this Scanner constructor I'm going to mention System.in first that I'm going to have a
[01:25] System.out.println() statement where I'm going to ask the end user to enter his details.
[01:30] Enter your age, followed by I'm going to catch the ageDetails into an int variable with the help of
[01:40] Scanner.nextInt().
[01:43] After catching the age details from the user, I can print out the same to the console
[01:49] saying that you are age is followed by semicolon, and at last I can try to append the age number to
[01:57] the statement.
[01:58] If I execute this program, it is going to ask the age details.
[02:02] For now, I'm trying to enter an age which is 25, and if I press enter, we are going to get the output
[02:07] which is your age is 25.
[02:09] So this is a super happy scenario.
[02:11] Now let me show you a negative scenario.
[02:13] This time I'm going to enter the age as -50.
[02:17] Do you think it is valid?
[02:18] But still my program is processing the age value and printing the same onto the console.
[02:24] It is also allowing me to provide the age like 190.
[02:29] Obviously this is an invalid age.
[02:31] Any number which is greater than 100 or less than zero can be considered as invalid age.
[02:39] So if I press enter, you can see we are still processing the age details and printing the same onto
[02:44] the console.
[02:45] So in this kind of scenario, I'm going to build a if logic, which is going to check if the age is
[02:52] less than zero or age is greater than 100.
[02:56] If any of these conditions are satisfied, I want to throw an exception in with the help of throw keyword
[03:04] and new operator followed by exception, and to this exception constructor, I am passing an String
[03:10] which is Invalid
[03:13] age details entered.
[03:15] Please enter a age between 0 to 100.
[03:21] So this is what I want to throw as an exception.
[03:24] Whenever we are trying to throw a normal exception with the help of this Exception class, it is going
[03:29] to be considered as a checked exception.
[03:31] That's why I'm getting a compilation error.
[03:33] Maybe I can resolve this by adding a throws statement to my main() method.
[03:40] Let me add exception to the method signature with the help of throws.
[03:43] So now this time I'm going to execute the program and enter a value which is -10 and I'm pressing
[03:50] enter.
[03:51] You can see we are getting the exception which is of type exception itself with the message invalid
[03:58] age details
[03:59] enter
[04:00] Please enter a age between 0 to 100.
[04:02] So if you see the data type of the exception is java.lang.Exception.
[04:07] So it may look good here, but in real projects it is always advisable to throw a specific exception
[04:15] based upon a scenario.
[04:16] So to handle these kind of scenarios we need to create the custom exceptions.
[04:21] So let me show you how to create a custom checked exception first.
[04:25] Later on we can discuss how to create an custom unchecked exception.
[04:30] So I'm going to create an custom checked exception.
[04:33] For the same I'm going to create a new package which is com.eazybytes.exception.custom.
[04:41] Inside this custom package I'm going to create a Java class.
[04:44] The exception name that I want to give here is InvalidAgeException.
[04:50] After giving this class name, we need to make sure we are extending the exception class which is available
[04:57] inside the java.lang package.
[05:00] So this will make your exception as a checked exception, because you are trying to extend the Exception
[05:06] class.
[05:06] Post that inside your exception, you can try to define an constructor with the class name as invalid.
[05:14] As exception to this constructor, you can accept the message like what is the exception message that
[05:21] we want to pass whenever we are throwing these invalid exception?
[05:25] So inside this constructor we need to make sure we are invoking the superclass constructor as well with
[05:31] the help of the super, followed by the message that we have received.
[05:35] Similarly, if you want, you can also create a default constructor with the class name as invalid exception,
[05:41] followed by I'm not going to accept anything, and you can see from this default constructor, I can
[05:46] try to invoke the default constructor of the super class.
[05:51] Now I have my own custom checked exception is ready.
[05:55] How to use that?
[05:56] It is very simple.
[05:57] We just have to go to these AcceptAgeDetails and here this time instead of throw new exception, I'm going
[06:04] to throw the new InvalidException with the same message like invalid details entered.
[06:12] Please enter a age between 0 to 100.
[06:14] With that we can mention the same inside the throws statement as well.
[06:19] Now, if I try to execute this program and enter an invalid age details, this time I'm going to get
[06:26] my own exception.
[06:28] Like you can see, this is the exception data type which is present inside the package
[06:33] com.eazybytes.com.exception.custom and the exception name itself is self-explanatory to others.
[06:39] Like whenever they see these InvalidAgeException, they don't have to look further about the message
[06:45] that we are trying to provide.
[06:46] So these are the advantages that we have whenever we try to develop our own custom exceptions, our
[06:52] code will look more professional or more user friendly.
[06:56] I hope you are clear on how to create an custom checked exception
[07:00] it is very easy.
[07:01] You just have to create a Java class and inside your Java class you need to extend the Exception class.
[07:08] Post that you can define some constructors and from these constructors you need to invoke the superclass
[07:14] constructors.
[07:15] In the next lecture, let's try to understand how to create an custom unchecked exception.
[07:20] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
