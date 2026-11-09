# 23.7 — Demo of java.sql.Date

> Section 23: Date and Time in Java

[00:00] Inside the Legacy Date API.
[00:02] If you try to type date and search inside the all places, you'll be able to see that Date class is
[00:10] present in two different packages.
[00:12] One is java.util, the other one is java.sql.
[00:17] As of now, we discussed everything about these java.util.Date.
[00:21] As a next step, let's try to understand what is this java.sql.Date and how it is different
[00:27] from the java.util.Date.
[00:30] To show you the demo, I'm going to create a new Java class inside the legacy package with the name
[00:36] java.sql.Date.
[00:39] Inside this class
[00:40] first I'm going to create the main() method.
[00:43] First, let's try to understand what is there present inside the java.sql.Date.
[00:48] For the same, I'm going to search for date and change this option to all places and open these Date
[00:55] class present inside that java.sql package.
[00:57] The very first important point that you can observe here is this Date class present inside the
[01:02] java.sql package.
[01:04] It is extending the java.util.Date.
[01:08] That means all the properties and methods present inside the java.util.Date
[01:14] they are going to be inherited into this class as well.
[01:17] If you try to read the definition of this class, it is a thin wrapper around a millisecond value that
[01:23] allows JDBC to identify this as an SQL date value.
[01:29] I know this statement looks very confusing, but let me try to break it down into simple words.
[01:34] One of the major difference between java.sql.Date and java.util.Date is, with the help of
[01:42] java.sql.Date, we can represent only date ignoring that time.
[01:47] Whereas with the java.util.Date we can't represent date and time separately.
[01:53] Always the time values are also going to be present inside your Date object.
[01:58] If you are looking for an option where you want to store only the date, ignoring the time, you can
[02:03] happily create the object of java.sql.Date.
[02:07] With that, you may have another question, which is what is the need for me to store only the date?
[02:13] Ignoring the time?
[02:14] What is the harm in storing that timestamp with all zeros, which indirectly represents that there is
[02:20] no time being stored?
[02:21] It's a great question
[02:22] let's try to understand whenever we are trying to store our data inside a database.
[02:26] Inside database
[02:27] also, they are going to be columns capable of storing various kinds of data.
[02:32] There are certain columns where the support to store the numerical values, and similarly there will
[02:37] be some columns where they are going to support only date value but not the time value.
[02:42] So in these kind of columns, if you try to store the data with the help of java.util.Date object,
[02:48] you're going to get a runtime exception because your database column is only capable of storing only
[02:54] date values, but you're also trying to send time values.
[02:57] In all these kind of scenarios, you can use the java.sql.Date.
[03:02] So this java.sql.Date is present inside the library belongs to the JDBC.
[03:09] So inside Java there is a concept and library with the name JDBC Java Database connectivity.
[03:16] So using JDBC we can connect to your database.
[03:19] We can store the data into the database
[03:21] or we can read the data from the database.
[03:23] So whenever you are trying to write logic with the help of JDBC library and trying to store the date
[03:28] objects inside the database, in all such scenarios you need to use the object of this class.
[03:34] So this class is present inside the package
[03:36] java.sql, sql is related to database.
[03:39] That's why they have given the package name as sql.
[03:43] So all the database related classes and interfaces you should be able to see inside this package.
[03:48] One such class is Date, which is going to help us to store the date object inside a database column
[03:55] that supports storing only date value.
[03:57] I hope you are clear with this quick introduction.
[03:59] Let me show you the demo as well so that it is going to be super clear for you.
[04:03] To show you the demo, I'll try to create the object of java.sql with a variable name as currentDate
[04:11] and on the right hand side I'll try to invoke the default constructor of Date, but there is
[04:17] no support
[04:18] to invoke the default constructor, you should always make sure you are invoking one of the parameter
[04:24] constructors.
[04:25] So the very first one is going to accept year, month and Date.
[04:29] It is deprecated
[04:30] the other one is it is going to accept the time in milliseconds.
[04:34] For example, to pass the current time in milliseconds from the epoch time.
[04:38] What I can do is, I can type the System class and using this System class, I'm going to invoke the method
[04:44] which is currentTimeMilliseconds(), the same kind of code
[04:48] I'm also going to write with the help of java.util.Date.
[04:53] So this time I'm going to select the date from the java.util package and the variable name I'm going
[04:59] to mention
[04:59] as currentDate1 and on the right hand side
[05:03] also, I'm going to invoke the constructor of java.util.Date.
[05:06] And to this constructor I'm going to pass the time in milliseconds with the help of the method present
[05:13] inside the System class.
[05:14] Here we're trying to use a complete qualified name.
[05:17] The reason is we can't import the same class name with the two different packages inside the import
[05:24] statement.
[05:25] So to clear the ambiguity which date I'm trying to refer this time I need to use the complete qualified
[05:31] name along with the package name inside my code.
[05:34] So now to show you the difference, what I'm going to do is I'm going to display both of these objects
[05:40] onto my console.
[05:41] The very first object that I'm going to print is, currentDate, which I built with the help of Java
[05:47] java.sql.Date, followed by I'm going to print the object currentDate1, which built with the
[05:53] help of java.util.Date.
[05:55] For both of them, I'm trying to pass the same milliseconds as an input, but if you try to see the
[06:01] output, the first date object does not store time anywhere, it simply storing the year, month and
[06:09] date.
[06:09] Whereas the second one, which we built with the help of java.util.Date, it is storing the complete
[06:15] time, date and all other details.
[06:17] With this, it should be clear for you that java.sql.Date is just a wrapper that is built on
[06:25] top of the java.util.Date to not consider that time values.
[06:29] So the thumb rule is very easy if you are trying to build that Date object for general use inside your
[06:36] programming language, you can happily use the java.util.Date.
[06:41] And even if your database has columns which support storing both the Date and time in such scenarios.
[06:47] Also, you can use java.util.Date, but if your database has columns where they are going to
[06:53] accept only date value in those kind of scenarios, definitely you need to create the object of
[07:00] java.sql.Date.
[07:01] I hope you're clear with the difference between java.util.Date and java.sql.Date.
[07:08] All the data points that we have discussed I have highlighted in this slide as well for your future
[07:13] reference.
[07:14] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
