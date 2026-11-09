# 17.14 — Sorting ArrayList of custom data type using Comparable

> Section 17: Lists and ArrayLists Unleashed – A Hilarious Journey through Data Structures

[00:00] As of now
[00:01] we saw the demo on how to sort the ArrayList object elements of type Integer String.
[00:07] The same kind of logic we can use to sort the elements of type double, float, short, byte, character.
[00:14] As a next step, we should also understand how to perform the custom data type sorting.
[00:19] To show you that demo around the custom data type sorting, first let me create my own custom data type.
[00:25] So the class name that I'm going to mention here is Student.
[00:28] Inside my Student, I'm going to create the variables.
[00:32] The very first variable is String name followed by internal number.
[00:37] So every student he's going to have a row number the same I'm trying to save using these rollNUmber
[00:43] variable.
[00:44] After the row number I also want to store the marks of the students.
[00:48] So these are the simple instance fields that I want to store as of now inside my Student object.
[00:53] So based upon these instance fields I want to generate a constructor with all the fields as an input
[01:01] followed by
[01:02] I also want to generate the toString() method.
[01:05] So let me select these toString() method and generate the same by considering all the instance fields.
[01:10] So you can see these are toString() method that is generated.
[01:13] This will be used whenever I try to print out my Student object.
[01:17] As of now, I'm not going to write any getter method and setter method because I don't have any requirement
[01:24] to fetch the data or to set the data.
[01:26] So this is a simple Pojo class that I have created.
[01:29] As a next step, let's try to create an ArrayList object which is capable of storing multiple student
[01:35] objects.
[01:35] Post that we will try to perform the sorting. Inside my project under this package.
[01:41] Let me create a new Java class, the Java class name
[01:45] I'm going to keep it as StudentSortingDemo inside this class,
[01:50] first let me create a main() method followed by
[01:54] I'm going to create an ArrayList object with the name students, and on the right hand side I'll just
[02:01] mention new ArrayList() and inside the angle brackets we need to mention the data type as student because
[02:08] we are trying to store the student related objects.
[02:12] Here, let me paste a few lines of code you can see with these lines of code.
[02:16] I'm trying to add a objects of Student into the students Collection object.
[02:21] How I'm creating the object of a Student, with the help of the constructor.
[02:25] By using the new operator to the constructor I'm passing what is the name of the student?
[02:29] What is his role number, and what are the total marks of a student.
[02:33] This way in total, I have stored four different Student objects.
[02:37] If needed, we can store any number of Student objects as well.
[02:41] First, let me try to print out these students object and you'll be able to see the details of the students
[02:48] are printed onto the console based upon the order of insertion that we have maintained inside the code.
[02:55] First we have John, followed by Smith, followed by Will, and at last we have Madan.
[02:59] Now think like we want to perform the sorting of these Student objects based upon some parameter.
[03:05] It can be age, it can be marks, it can be name, or it can be a row number, or it can be a combination
[03:11] of row number and the marks.
[03:13] The sorting criteria can be anything, but let's try to understand how to perform the sorting of our
[03:19] custom data types. First without writing any of our custom sorting logic, let me try to invoke the
[03:26] sort() static method available inside the collections.
[03:31] To this, I'm going to pass the students as an input.
[03:35] With that, you can see I'm getting a compilation error saying that no instance of variables T exist,
[03:42] so the Student conforms to the comparable.
[03:45] So these are compilation error that I'm getting.
[03:47] And of course we can't invoke the other sort() method with the help of Students object itself.
[03:53] Because anytime when we want to invoke the sort() instance method, it is going to expect the object of
[03:58] our own custom comparator.
[04:00] As of now, we have not written any custom comparator.
[04:03] So that's why as of now, I can't use this as well.
[04:05] And the very first one also I can't use it. Because my students are not comparable,
[04:11] that's why this compilation error is coming.
[04:14] So what do I mean by my students are not comparable?
[04:17] Let's try to understand more details about this by going into the SortingDemo class.
[04:22] So here, whenever we want to pass these numbers and countries as an input to the Collection.sort(),
[04:29] we didn't get any compilation error.
[04:31] Why we are getting only compilation error for our Student objects.
[04:36] To understand the same, you need to open the either Integer class or a String class.
[04:41] Here you can see Integer class
[04:43] it implements Comparable interface.
[04:46] So whenever it is implementing Comparable interface, we need to override a method which is compareTo().
[04:52] .
[04:53] So inside these compareTo() method you can see Java team
[04:56] they have written a logic to compare the values of
[05:00] Integer objects. The same, you will be able to see inside the String as well.
[05:04] So whenever you want to perform the sorting, there are two options.
[05:07] One is by implementing the Comparable interface and the other one is by implementing the Comparator
[05:14] interface.
[05:14] So there is a difference between Comparator and Comparable.
[05:18] We're going to discuss in detail about them.
[05:20] For now, let's try to implement the sorting of our Student objects by using these Comparable interface.
[05:28] For the same,
[05:28] so I'm going to copy these implements logic and paste it inside my Student pojo class. Here I'm getting
[05:35] a compilation error here
[05:36] we should not mention the Integer.
[05:38] We should mention Student only because we are trying to overwrite these Comparable interface to compare
[05:44] the Student related objects.
[05:47] Since we implemented an interface, we are getting a compilation error to overwrite the method which
[05:52] which is comparedTo().
[05:53] So let me click on this, implement methods and overwrite these comparedTo() method.
[05:58] So whenever you are trying to overwrite the compareTo() method, you are only going to have a single
[06:05] input parameter to your compareTo() method.
[06:08] Whereas whenever you are trying to implement the Comparator and overwrite the method compare(), you're
[06:13] going to get that two objects as an input parameter.
[06:17] Do you know the reason?
[06:18] It is very simple.
[06:19] With the help of Comparator, we are writing our comparison logic outside of our classes.
[06:25] Whereas whenever we are trying to implement the Comparable interface, we are trying to provide the
[06:30] comparison logic within the same class, like inside the Student, inside the Integer, and similarly
[06:36] inside the String.
[06:37] So whenever we are trying to write our custom comparison logic inside the same class, we don't have
[06:43] to pass the two different method input parameters.
[06:47] Instead, we need to pass only a single method input parameter.
[06:51] But you may have a question which is then how the comparison is going to happen between two elements.
[06:56] It's very simple.
[06:57] The very first element object is going to be referred with the help of this keyword.
[07:02] This refers to the current object, whereas the other object which we want to compare is going to be
[07:08] passed as an input to this method, which is compareTo().
[07:12] I hope it makes sense.
[07:13] But coming to the Comparator, we can't use that this
[07:16] when we say this here it is referred to the object of LastCharComparator, but not the object of Integer
[07:22] or Student.
[07:23] So that's why whenever you are trying to implement the Comparable, there are two thumb rules that you
[07:28] need to take care.
[07:29] One is you need to implement these interface in the same Pojo class which you are trying to sort.
[07:35] And the second one is you need to override these compareTo() method.
[07:39] And to this compareTo() method, you need to accept a single method input parameter.
[07:44] Now think like
[07:45] I have a custom sorting requirement to sort my Student objects based upon their marks.
[07:52] So how to do that?
[07:53] It's very simple.
[07:54] We need to first invoke the Integer wrapper class.
[07:58] And inside this wrapper class we have a compare() method which is going to compare two int values.
[08:04] Since we have created the marks as an int, I'll try to mention two different marks to compare and accordingly
[08:12] this is going to return zero, -1 or 1 based upon the same logic that we have discussed here.
[08:19] So the next problem is how to get the two marks details of that two different students.
[08:24] The very first student marks details we can get by using that this keyword followed by marks and the
[08:31] second student object to marks we can get based upon o.marks.
[08:37] We know the second Student object is being passed as an input to this, comparedTo() the same I'm trying
[08:43] to pass as an input to this compare() method, which is available inside the Integer wrapper class.
[08:48] I can take this code and mention just after these return.
[08:53] So now the Student comparison is going to happen based upon their marks.
[08:58] Let me go to the StudentSortingDemo.
[09:01] You can see right now the compilation error is resolved because our students can be compared right now
[09:09] since the Student class implemented a Comparable interface and override the compareTo() method.
[09:16] Now my JDK or Java, they have complete details on how to sort my Student objects.
[09:23] Before I try to execute this program, let me copy this System.out.println().
[09:28] After the sorting related code, let me execute this program and you'll be able to see the Student objects
[09:35] are sorted in an ascending order.
[09:37] First we have a student with the marks 92, followed by 92, followed by 97 and the class.
[09:44] We have one more student with the 99 marks.
[09:47] Here the sorting is happening based upon the ascending order.
[09:51] If you want to perform your sorting based upon the descending order, the logic is very simple.
[09:55] You just have to swap these elements so that the sorting is going to happening
[09:59] in an descending order.
[10:02] If needed instead of invoking this compare() method, you can write these logic inside your compareTo() method,
[10:08] like if the very first argument is less than second argument, you're going to return -1.
[10:13] Otherwise, if both of them are same, you're going to return 0, and at last you're going to return
[10:19] in the scenarios where if x is greater than y.
[10:22] I hope this makes sense.
[10:23] As of now, you can see we're trying to perform the comparison of the Student objects based upon their
[10:29] marks.
[10:30] Think like I have a requirement to sort the student based upon their marks and the rollNumbers.
[10:35] I want to have two different parameters for my sorting to implement these new sorting requirements.
[10:41] Let me make a few changes.
[10:43] So what I can do here is I can try to first compare the marks details and the output from these comparison
[10:51] I'm going to catch inside an int variable with the name marks comparison.
[10:57] If my marks comparison output is 0, then only I want to consider the second parameter for my comparison.
[11:05] Otherwise we should always perform the sorting based upon the first parameter, which is marks.
[11:10] That's why I'm going to write an if block, saying that if marks comparison holds 0, which indicates
[11:16] that the marks in two different student objects is same, then in such scenarios only, I'm going to
[11:22] consider the rollNumber details of the Student.
[11:25] So here instead of marks I'll invoke the rollNumber.
[11:28] And here also I'll just mention the roll number so you can see if the marks comparison resulted into
[11:34] 0.
[11:35] Then I'm going to consider the second parameter.
[11:37] Otherwise I'm going to simply return the output from the marks comparison.
[11:42] This way I'm trying to sort based upon two parameters.
[11:46] The very first parameter is marks.
[11:47] If marks are same then I want to consider the rollNumber.
[11:51] So this time let's see the demo of these changes.
[11:54] By running the program StudentSortingDemo, you'll be able to see this time that first two Student
[12:01] objects marks are same like like 92 and 92, but the rollNumber is also considered.
[12:06] That's why the rollNumber is 168 here, followed by 169.
[12:10] And after this you'll be able to see the marks with the value 97, followed by 99.
[12:17] I hope this makes sense to you, and you are clear on how to perform the sorting of custom data types
[12:24] by using the Comparable interface.
[12:27] As of now, we are using the Comparable approach as a next step.
[12:31] Let's try to understand how to achieve the same with the help of Comparator interface.
[12:36] So once we discuss everything about Comparable and Comparator, I'm going to discuss what is the differences
[12:42] between them and when we should use Comparable and when you should use the Comparator interfaces to
[12:47] implement your own custom sorting requirements.
[12:50] I hope you are clear.
[12:51] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
