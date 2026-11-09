# Automate the backup and upload process with a shell script

*Section: Jenkins & AWS*

-: Hello and welcome back. In this video, we're going to learn how to automate the process to take a MySQL dump from a sample script. So we're going to log in into our remote host. Cool. And in here we're going to create a sample script maybe at /tmp/script.sh And in here, you know we're going to start with the classic /bin/bash. And now remember that the only one thing that we need to do is to type the commands that we use to take the MySQL back up.

So let's look for documenting here in our container. It should be here. Cool. This is in here. So let's copy this and let's modify our script again. Let's paste that in here. And now we want these values to be variable. So for example, I want this db host to be a variable. So let's put it like this. I want the password to be a variable. So let's put it like this. Let's put like db password. I want the name of the database to be dynamic as well.

So let's put like db name here. And this is pretty cool, right? So remember that these variables now are not defined so we need to define them and we're going to use bash parameters. So we're going to do something like this. We're going to say that the db host, oops db host it means this variable, it's going to be equals to the first parameter that our script is going to get. So the password, it's going to be the second I can actually copy and paste this.

The second parameter, the password is going to be the second parameter, and the db name, for example is going to be the third parameter that our script is going to receive. Third, pretty cool, right? So let's test it. Let's give it executable permissions to our script, tmp script.sh And if we run it, tmp/scripts.sh this is going to give an error because we need to define first. Let's look to this scripting here.

We need to define the host name which is going to be the db host. Remember the db password, which is 1,2,3,4 and the db name, which is testdb. So let's hit enter and it doesn't complain. Cool. So if you take a look on your db, that SQL file you're going to have your file there. So normally in backups, this is not good to have a file with the same name, for example, like db.sql because normally you would need to know the date in which that backup was taken.

So let's modify this. If you take a look to the date command you can actually give this command pre formatted output. It means that you can give it the format that you want. So for example, if you type + % and capital H you're going to have the hour, the current time. If then you give it something like % M you're going to have the minute. And then if you do the same for the letter S you're going to have our minute and second which is pretty cool because if you execute this again and again and again you're going to see these values changing which is cool for backups.

So let's use this command to name our resulting file. So let's copy, let's modify our attempt script.sh and we're going to say, for example, the date. It's going to be the execution of this command, right? So we want to name our file, something like db- and then the output of the date command. Cool. So now let's look in the tmp directory. We only have this one, so let's run the script again passing all the mandatory parameters like db host, for example.

In this case, let's hit enter. Now let's look on the tmp directory. And as you can see, we have the db name and then you have the hour, minute, and second for that. If we execute it again and you do an ls you're going to have another file, which is pretty cool. So this is it for this video. I'll see you in the next lesson.
