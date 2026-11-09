# Multiple Jenkinsfiles

*Section: Advanced Jenkins*

1 If you've been following along 2 with the course, we set up a multi-branch pipeline 3 and we forked the simple-java-maven-app repo. 4 What I'm gonna do is go inside the Jenkins folder. 5 We can see this Jenkins file. 6 What I'm gonna do is click on Raw. 7 Copy everything. 8 Let's go back, back again, and back again. 9 And inside here, I'm gonna create a new file. 10 And I'm gonna call it test.jenkinsfile, 11 paste in the contents.

12 And again, we're gonna push this directly 13 to our master branch, so this may 14 actually trigger a new job. 15 But the key thing to note here 16 is that we are gonna have two Jenkins files, 17 but as far as Jenkins is concerned, 18 it's still gonna point to the one inside the Jenkins folder. 19 We have to explicitly say which one to use, 20 and that's why we can have multiple Jenkins files inside.

21 Now let's commit this. 22 So we'll say added new Jenkins file, 23 and let's commit the file. 24 Awesome, and we can see it there.
