# Integrate your script with AWS CLI

*Section: Jenkins & AWS*

Instructor: Hello and welcome back. In this video, we're going to learn how to upload the backup that we're taking from this script to S3. So cool. Remember that the first thing that we need to do is to define the environment variables to get authenticated. I always like to do this because this is a bash command, which means if this fails, then everything else is going to fail. Right? So the first thing that we're going to do is that we're going to export two variables.

Remember those variables? Those are on your history. So let's look for it. Something like ID. Right, this is it. So let's graph this key ID. Let's copy it. Let's open our script and let's paste that into the first variable. So we're saying we're exporting this variable, which is the ID with its value. You can think this as a user. So that's why I am not passing this as a parameter because it should be, or it shouldn't be sensitive.

But if you want, you can make this a parameter. So the second one, which is the secret key that should be a parameter because that's a password and a password should never be on plain text. So let's look for the key, for the secret key in our history. Remember that if you hit control and the letter R, you are going to have this search here. So let's copy only the, we're gonna enter in here. Let's copy only this name, which is the AWS Secret Access Key.

Let's copy this and then let's modify our script again. Let's paste that variable. And this is going to be equals to maybe the four parameters that we're going to pass. So let's call this parameter like Amazon Secret equals to the four parameter that we're going to pass. Cool. So let's use this name as a variable, oops, in here. Then we're going to say that the key is the value of this another variable.

Pretty cool. So let me give this an ampersand ampersand, ampersand ampersand. And now we need one more important line, which is the aws s3 cp. Remember the line that we use in order to copy the file. This is the line. So we're gonna copy this. We're going to modify our script again. Let's paste this line in here. We can do something like an echo here, which is uploading, for example, uploading. And then we say db, Uploading your db backup.

Cool. So now we're going to modify this and we want to say, okay, AWS s3 cool cp. Right? /tmp/db. No, this is not correct because remember that we're using db-date. So db-date to pick the correct file. And then we're going to upload that file to which bucket? This is a good question. So probably I want the bucket to be dynamic so I can upload to several buckets. So let's give this like bucket name as a variable, which is going to be the fifth parameter that our script's going to receive.

So we're going to remove this and we're going to say bucket name in here, which is pretty nice. And remember, then you can say db date. So this is pretty cool. We could do something like backup, and then we say like db and then we type this date, and then the SQL. So using this backup variable, we can just rename this and we can just put something like this. Let me show you. Backup, pretty cool. And then let's do it again, Uploading your and let's use backup.

And in here, we're going to upload the backup. Right? This backup actually means db-date that was capturing here the SQL. Cool. So this is going to be this script that is going to upload our database to Amazon S3 through Jenkins. So this is it for this video. I'll see you in the next lesson.
