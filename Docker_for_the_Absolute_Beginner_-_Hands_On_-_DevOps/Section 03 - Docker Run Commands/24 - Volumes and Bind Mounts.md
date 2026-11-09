# Volumes and Bind Mounts

*Section: Docker Run Commands*

1 Now let's look at how data is persisted in a Docker container. 2 Let's say you were to run a MySQL container. 3 When databases and tables are created, 4 the data files are stored in slash vr slash lib slash MySQL inside the container. 5 Remember, the Docker container has its own isolated file system, 6 and any changes to any files happen within the container. 7 Let's assume you dump a lot of data into the database.

8 What happens if you were to delete the MySQL container and remove it? 9 As soon as you do that, 10 the container along with all the data inside it gets blown away, 11 meaning all your data is gone. If you'd like to persist data, 12 you'd want to map a directory outside the container on the Docker host to a 13 directory inside the container. In this case, 14 I create a directory called slash opt slash data and map that to slash 15 var slash lib slash MySQL inside the Docker container using the dash V flag, 16 specifying the directory on the Docker host, 17 followed by a colon and the directory inside the container. This way, 18 when the Docker container runs, 19 it implicitly mounts the external directory to a folder inside the container.

20 All your data will now be stored in the external volume at slash opt slash data 21 dir and will remain even if you delete the container. 22 Now a quick note on the dash V form versus the dash dash mount form. 23 Modern Docker has a more explicit syntax called the dash dash mount form. 24 The same bind mount is rewritten using key value pairs type source and target 25 instead of a single colon separated string. Both work.

26 The dash V form is not deprecated, 27 but the dash dash mount form makes the type of mount explicit bind volume or 28 temp FS, which becomes more useful as your setup gets more complex.
