# Build a table using HTML, CSS and PHP to display users

*Section: Jenkins & Ansible*

Instructor: Hello, and welcome back. In this video we're going to be creating the table that's going to display the information about users in the database. So for that, I already created a sample table file, which is an HTML file that has a little bit of CSS and a little bit of PHP to display that information. So let me show you this file in here, in Sublime, so you can see it better. Here I'm just creating a sample table, which is a table, and it has an ID, a name, a last name, and age.

Then I'm populating that information doing a sample query using PHP to our DV host. Remember that our DB host is db. That user is root, password 1234, and database is people. I have a little bit of inline CSS in here just to give it colors, and here I am just doing a sample query, asking for all the columns, and doing our where, age equals to 25. So this is the file, pretty simple. And you are going to have that file and the resources.

So, that file is in here, but remember that our web server is actually serving the content inside of the docker container that has that web service. So we're going to copy this table dot j2 through our container, which is the web container, to var, ww, html, index dot php. And if we do this, then, Oh, docker cp, my bad. And if we do this, then the index php that we created before, it's going to be replaced with this content.

So now, if we go to our browser on the port 80, we're going to see this beautiful table that is displaying the age, or, that's actually displaying the people that have age of 25. So if we want to display another thing, we could just modify the fable file, and we can simply change the where. So for example, we want to display people with 20 years. So let's save this. Remember that we need to copy this again because we modified this outside of the container.

So let's copy this, and if now we refresh, then a new query is going to be done to the database, and that result is going to be displayed in this table. So, this is it for this video. I'll see you in the next lesson.
