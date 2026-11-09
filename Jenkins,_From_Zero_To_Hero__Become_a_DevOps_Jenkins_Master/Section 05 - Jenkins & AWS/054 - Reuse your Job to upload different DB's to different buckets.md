# Reuse your Job to upload different DB's to different buckets

*Section: Jenkins & AWS*

Instructor: Hello and welcome back. In this video, we're going to see the power of the parameters in Jenkins. So, remember that in here, we have, like, three parameters that we can change, which is the db_host, the testdb, which is the database name, and the bucket name, where we want to upload the file. So, for this video, we're going to create another database, logging into the remote host, connecting to MySQL.

So, to connect to MySQL from the remote host, you type mysql -u root -h db_host. Remember, that's your database host. Then, you pass the password in here, if you want. So, let's keep it like this. And let's create a new database, which is going to be called, for example, test2. Semicolon, enter. And if you hit show databases, then you now have test2 database. Cool. So, now let's go ahead and create a new bucket in here.

Let's give it a name like mysql-jenkins-2, for example, and we're going to hit the create button. So, now what we want to do is to test that we can, without any problem, change the name of the database and the name of the bucket from here to match the bucket that we have just created. So, let's copy this. Let's paste this in here. And if you hit the build button, then it should work. So, what's going to happen here is that, as you can see here, Jenkins now is going to look for the database test2 in the database host, and then it's going to upload that database to the mysql-jenkins-2 bucket that we created.

So, let's look for it. Let me refresh this in here. And as you can see, we have what we expected here. So, this is the power of parameters in Jenkins, that you can actually change whatever you want. This is dynamic, so you can put any data here, and as long as that data is correct, then your job is going to work as expected. So, this is it for this section. I'll see you in the next lesson.
