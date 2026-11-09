# Test your Script inserting the data to the DB

*Section: Jenkins & Ansible*

Instructor: Hello and welcome back. In this video, we're going to be testing our script. So if you take a look to your script, make sure that it has executable permission during this command. And now we wanna copy this to the DB container which is our MySQL container. So for now, let's copy it to the temp directory. If we exec into the DB container. And if we go to the temp directory, we're going to see our file there.

So now we're going to execute this file and we're going to see the magic happening. So let's hit Enter, and we have an error here. And what's the error about? The error is complaining about the people.txt file was not found. Remember that our script, it's actually reading the TXT file so it should be at the same level. So let's go out of this container and let's copy the people.txt file to that container in the same location.

So we'll put the docker at the beginning and then we have this, cool. So let's exec into the container. Let's go to the temp directory. And in here we have now the people file and the put file. So let's execute the put file again. And as you can see, it's actually working good. So this warning here is because in the script we're using the password directly and that's the warning. But as you can see, it's says ID, name, last name, and age was correctly imported.

If we now log to the MySQL service inside of the container and we do dash P 1234, and then we use the people database, people, and then we do a show tables. Remember that we created a registered table. So if we now do something like select asterisk from this table, you are going to see all of the fake information that we inserted in here. But if you go up, you are going to see these blank columns because remember that in our first import we didn't have the people.txt file in place.

So that's why we have this error in here. So let's fix it because we're going to need a full working database. So let's do a delete from register, and that's going to clean up all our work table. So if you do a select, you're going to say this empty. So let's get out of the MySQL service and let's run the put.sh again. And now it's going to have no errors. And finally we can log in again to the MySQL service use the people database.

And now we can. And now we can query the table and we're going to see all the information displayed correctly. So our script is working good. We already have our database populated with information, age, random age, last name, and names. And we have IDs for every single record in here. So this is pretty cool. I'll see you in the next lesson.
