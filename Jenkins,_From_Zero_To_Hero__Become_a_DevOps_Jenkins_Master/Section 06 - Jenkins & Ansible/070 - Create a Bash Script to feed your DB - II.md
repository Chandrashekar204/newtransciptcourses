# Create a Bash Script to feed your DB - II

*Section: Jenkins & Ansible*

Instructor: Hello, and welcome back. In this video, we're going to keep creating our script, our put, that is, a script to retrieve the fake information from the file. So remember that at this point, we already have the name from the people, and we're grabbing the name via the id. For example, in the first iteration, we have the name of $name, and the last name of $lastname. So let's print this so you can see it.

Let's print in here, the $name and the $lastname. Oh, it's Python, actually, let me do it in the batch way. echo. We wanna print the $name and we wanna print the $lastname. So, and we wanna type here done. So if we do this and then we execute the script. Let me give it executable permissions, put. You are going to see that all the names are being printed. But in this way, we can modify this, for example.

And we can say like echo, for example, "name for person with id $counter is", and then if we execute it back, you're going to see that our script's working good. So name for person one is this. Name for person two is this, three is this, and so on, and so forth. So in this name, we already have captured the names and the last name for every single person, which is going to be cool. So let me remove this echo from here, and we're going to keep our data in this.

So we already have the $name and the $lastname to populate our database. The only one thing that we're missing is the $age. So let's create an $age wherever in here. And I wanna teach you a cool command in Bash, which is the shuf command. And this shuf command returns at random number from a range. So for example, if I say something like -i, and then I give it the range, like 20-25, it's going to return a lot of numbers in here from that range, random numbers.

But if I wanna get the first one, then I pass -n 1. And that's gonna retrieve the first number from the list. As you can see here, this is something like a list. So -n retrieves the first one. If I hit this simultaneously, you're going to see that random numbers are being given. So our $age is going to be this command. Because, for example, if I do this, then the first person is going to have this random age.

The second person is going to have this random age. The third person is going to have another age. So on, and so forth. So let's modify our script. And let's say the $age is going to be equals to the output of this. Oh, I didn't copy the command. It's going to say equals to the output of this shuf command. So let me copy this. And now we're going to paste this in here. And now $age is going to have a value, a random value.

Cool. So now we only need to insert the data in the database. So how do we do this? Remember that we're going to execute this script from the database container. So we're going to do a mysql -u root -p1234 people. Remember, people is our database. And then we wanna insert things to our registered table. So we pass in -e, and we say "insert into". This is a SQL sentence, so insert into register, which is the table that we created.

And we're going to insert the values that we are creating. So in this case, we need to insert the $counter. Which is going to be the $counter. Which is the id, remember. And then we need to insert the name for that person, which is going to be something like. Let me use single quotes in here because we are already using double quotes. So the $counter is going to be the id in the registered table. Then we need to insert the $name, which is, you know, it's going to be taken from the people.txt file.

And we need to insert the $lastname as well. And finally, we need to insert the $age. So we're inserting the $counter, which is the id. We're inserting the $name. There's the name. We need to insert the $lastname. This is the last name. And we need to insert the $age in here. So this is the $age, which is a random number. So, pretty cool. Now, to make sure that everything works good, we're going to do an echo here.

And we're going to do something like, for example, $counter, which is the id. And then we're gonna print the $name. We're gonna print the $lastname. And we're gonna print the $age. Let me put in here like a comma, $age. And we're going to say, was correctly imported. So, okay, this is pretty cool. So we already have all the information in here extracted from one fake file. Then we're inserting that data in every iteration.

And finally, we're printing every single name to make sure that it was successfully imported. So let's save this file. And I will see you in the next lesson.
