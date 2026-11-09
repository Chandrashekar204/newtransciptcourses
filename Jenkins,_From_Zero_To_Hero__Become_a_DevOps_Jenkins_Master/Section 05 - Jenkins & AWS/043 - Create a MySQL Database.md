# Create a MySQL Database

*Section: Jenkins & AWS*

Instructor: Hello, and welcome back. In this video, we're going to learn how to create a MySQL database in order to take that database as a backup. So if we type docker ps, we're going to see two things in here. The first one is that we have our remote host up and running. And the second thing is that we need to go inside of our jenkins-data folder, and we need to cat our Docker-composed file. So, once we have this information displayed, we're going to go inside of the remote-host container.

And once we are inside of that container, we're going to log into the MySQL container. So let's type mysql -u root, which is the root user. Then we're going to type -h, which stands for the host that we want to connect. And remember that we want to connect to this host, which is the db_host that we created. So let's copy this, let's paste this. And then we need to specify the password, which is going to be specified as -p.

Hit Enter. And this is the password that you're going to use. In this case is 1234. So 1234. And now, as you can see, we're connected to this specific MySQL server. So pretty cool. Let's take a look to the database that we have available. Show databases. We don't have any database created by us. So let's create a new database. Type in create database, and we're going to call it like testdb, for example.

Hit Enter. And now, we're going to create a table in this database. So let's use this database, which is the testdb that we just created. Cool. And now let's create a table. In order to create a table, we need to type create table. And then we need to give it a name, which is going to be, for example, info. So this info table is going to contain a name, which is going to be something like varchar20, for example.

Then we put a comma here. Now, let's give it a last name, lastname. And this is going to be like varchar as well, 20 again. And finally, we're going to give something like age. And this is going to be an int. And this int is going to have a line of 2. So let's put a semicolon in here, and hit Enter. And now, you've created your table. If you type show tables, now you can see your table. Now, if you describe your table, which is called info, you are going to see the structure of this table.

So now, let's go ahead and populate that table with a little bit of fake information in here. So let's insert data here. That's like insert into info. That's the name of the table. And then we're going to give the values. So in this case, we're going to give the name, which is going to be my name. Then we're going to give my last name. And finally, we're going to give my age. So, let's hit Enter. I forgot the semicolon in here.

And if you do select * from info, you are going to see the information that we just created. This is just to populate a little bit of fake information in order to validate our backup once we take it and we want to restore it. So cool. You already know how to create a MySQL database in Docker. You already know how to create a table for it and how to put a little bit of fake information into it. So this is it for this video.

I'll see you in the next lesson.
