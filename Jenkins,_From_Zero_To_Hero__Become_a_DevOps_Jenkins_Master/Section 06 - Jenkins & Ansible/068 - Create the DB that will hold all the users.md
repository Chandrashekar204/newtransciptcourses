# Create the DB that will hold all the users

*Section: Jenkins & Ansible*

Instructor: Hello and welcome back. In this video, we're going to create a MySQL database to store our application or at least the data for our application. So to create a database, let's go to our DB container that we created in the past. So let me fix this. And in here we're going to log into MySQL using MySQL -u root -p. Enter 1234. Cool, so if we hit show databases, we're gonna find out the current databases.

So we wanna create a new one. And for example, let's kill this database like people. So let's say create database people. Pretty simple. Semicolon and hit enter. If you hit show databases again, you're gonna see your new database created. So, cool. Now we need to create a table in here. So let's use the people database and we're gonna create a table. So to create a table, we need to do something like create table.

Then you give the name of that table. So for example, let's say like register and then we're going to say the columns for this table. In this case, we want the ID, which is going to be something like an int and this is going to have like three of len. You can give you whatever you want. Then we're gonna have the name of that person who's registering to our application, which is going to be at varchar 50, for example, because you know, there are long names.

And finally, we're going to have the last name for that person. Last name, that's going to be our varchar as well. 50 again. And I think that we need to include the age. So let's type something like age, and this is going to be an int for example of three in line. Cool. So let's put a semicolon at the end. Hit enter and then you have successfully created your table. So if you wanna see it, you do show tables and then you find this out.

Cool, so now let's describe our table. We'll just call it register. And then we're going to see this structure that we just created. So this is cool. We already have our database created and our table to store the information. So this is it for this video. I'll see you in the next lesson.
