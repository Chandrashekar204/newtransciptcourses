# Learn how to create a Jenkins list parameter with your script

*Section: Getting Started with Jenkins*

Instructor: Hello, and welcome back. In this video, we're going to learn how to create a list parameter in our Jenkins here. So whenever we click on the build button, it's going to show up a list and we can choose the value that we want. So to add a new parameter, we click on the Add Parameter button, and we choose, in this case, Choice Parameter. So we're going to give it a name which can be like last name for example.

And in here we're going to give choices. So let's say that the last name is gonna be like Smith. Second one is going to be my last name. Third one is going to be a random one. And that's it. So cool. Here, in this case we have a parameter which is called LASTNAME and a list of values. So depending on which value the user picks up, then this variable is going to take that value. So let's make it clear.

For example, now we have the FIRST_NAME, now we have the SECOND_NAME. And now what we need to do here is say like LASTNAME. So let's save this and let's click on Build with Parameters. As you can see here, we still have the FIRST_NAME parameter which is a string parameter, SECOND_NAME is a string parameter as well. But the third one, the LASTNAME that we just created is a list. And if we click on this list, we are going to see the allowed values that we created before.

So the user can only choose one of these values. So let's go ahead and choose the last one. And as you can see, let's just give a random name here and click on Build. Once the execution finishes, you are going to go here, Console Output, and then you're going to see your Hello, the first parameter, second parameter, and the third parameter that is the result of the choose an option by the user. So as you could see, we choose the Doe last name as the value for this parameter.

So let's click for example in this. Let's hit Build. And after the execution finishes we're going to go into the output and as you can see here, the script is actually taking the values that we are sending, which is pretty good. So cool. You already know how to create string parameters, how to create list parameters, and how to make your Jenkins job to print those values. This is pretty cool. See you in the next lesson.
