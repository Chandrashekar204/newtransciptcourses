# 42.5 — Install and Setup SQLite for Linux

> Section 42: Databases - Old content for Java 11

In this video, we're going to install the SQLite command-line shell for Linux computers. Now if you're using Windows or a Mac, refer to the previous two videos where we actually set it up for those platforms. But if you're running Linux, you're in the right place, so let's get started. Writing database code straight away isn't the easiest way to learn about SQLite and the SQL language because if you get errors you'll have to work out if the errors in your code or in the SQL statements that you've actually used.

So what we're going to do is we're going to start by using the SQLite command-line shell so that we can create databases and use SQL commands without having to worry about code at this stage. Now on Ubuntu Linux, turns out this is really easy. So I'm going to start by opening a terminal session. So I'm just going to use the shortcut on Ubuntu which is CTRL + ALT + T. That opens the windows you can see there. Obviously, I could have just come up here and just type terminal in there and open it that way as well.

All right, so installing SqLite3 firstly, we check to see whether we've got it we type sqlite3. You can see that it's saying that currently, we haven't got the program installed. So again, on Ubuntu Linux, we do a sudo space apt space install space sqlite3, press enter, type in the password. And you can see that was a really, really quick installation, it's only a small program because we're only getting the command-line shell, not SQLite itself.

At this point, we can then check to see whether sqlite3 is installed typing s-q-l-i-t-e-3. And you can see instead of getting an error like we did previously, we can now see down the bottom it's showing the SQLite version number .help for instructions, etc. And incidentally, you might see a slightly different version number to what I've got on the screen, but that's okay. So long as you can actually get it working and you can see that we've actually started the SQLite command-line shell.

And now you're good to go. And just keep in mind specifically with Ubuntu, I'm using 14.04, but if I was use if you're using Ubuntu 16.04, you will actually get a much later version. But both versions will actually work fine with the course. there's no prerequisites for a specific version of SqLite3. All right, so at this point we've completed the installation so I can type.quit to get out of the sqlite3 command-line shell, type exit to close down the terminal session.

And at this point, we're done. So let's now move on to the next video, where we're going to go through a bit of an introduction on using SQLite. See you in the next video.

----------------------------------------
