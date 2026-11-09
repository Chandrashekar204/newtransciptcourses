# 29.4 — [JAVA 22] Unnamed Variables & Patterns - Demo

> Section 29: New features from Java 22, Java 23 and Java 24

[00:00] To explain you about the unnamed variables.
[00:03] I have created a Java project and inside the Java project I also created a Java class with the name
[00:09] Unnamed variables.
[00:11] I'm going to upload this code into the GitHub repo.
[00:14] The link of the GitHub repo is already mentioned in the very first lecture of this section.
[00:20] Since you are already an expert of Java, and since we are exploring the new feature unnamed variables,
[00:25] what I have done is, I have written a good amount of code behind the scenes and using this code, I'm
[00:31] going to show you all the possible scenarios where you will end up using unused variables, but you
[00:37] can't delete them.
[00:38] So in all those scenarios, using the unnamed variables is going to be a good option.
[00:43] So just to save some time of yours, I build this logic behind the scenes.
[00:47] I hope you're fine.
[00:48] So let's try to understand this code.
[00:50] Like you can see here.
[00:51] We have a class with the name UnnamedVariables, and inside this class we have a main() method.
[00:56] So inside this main() method first we have a scenario one.
[01:00] So inside this scenario one first you can see with the help of this line we are trying to create a List
[01:06] object.
[01:07] And inside this List object we have various fruit names like apple, banana, orange, grape and kiwi.
[01:13] So this List object I'm trying to send as an input to the counterWords() method.
[01:19] So let's try to open this method which is present inside the same class.
[01:23] So you can see here this method is accepting the input in the form of Iterable.
[01:29] But from the main() method we are trying to send the input in the form of List object.
[01:35] But still Java is not complaining anything because if you try to open this List, this List is extending
[01:41] Sequencedcollection and this sequencecollection
[01:44] extending the collection.
[01:45] And this collection is extending the iterable.
[01:49] So since List is a child of Iterable, the Java is not throwing any compilation errors.
[01:54] As a next step, let's go to this method one more time.
[01:57] And inside this method you can see the business logic that I have written is just to iterate all the
[02:03] elements present inside these input words, and during the each iteration I'm trying to increment the
[02:10] variable which is total words.
[02:12] Once this for each block is executed at the end, we are going to return the total words as an output
[02:19] from this method.
[02:20] So if you try to closely observe this logic, you can see I have an unused variable.
[02:25] There is a culprit here.
[02:27] The variable name is word.
[02:29] Can I delete this?
[02:30] Off course I can't delete this because the Java expects a syntax that we need to follow whenever we are
[02:36] using the for each block.
[02:38] So that's why deleting the unused variable is not an option.
[02:42] So this is one type of typical scenario that you may end up having unused variables which you can't
[02:48] delete them from your code.
[02:50] And at the same time you can see my IntelliJ Idea
[02:53] it is throwing a warning saying that parameter word is never used.
[02:57] It is giving a recommendation saying that rename word to underscore.
[03:00] So this variable name I can simply replace with the unnamed variable which is underscore.
[03:07] With that you can see I no more have any warnings and at the same time my code also looking good.
[03:14] So any developer who is aware about the unnamed variables, it's pretty easy for them to understand
[03:20] that I have an unnamed variable, and they should not try to update this business logic by leveraging
[03:26] these unnamed variable, because they can't use this anywhere inside the for each block.
[03:31] So with this, we are also having an advantage, which is it is going to improve the readability of
[03:37] my code.
[03:38] Please make sure you are having the latest IntelliJ Idea downloaded which support JDK 22.
[03:44] As of now, I'm using the IntelliJ Idea 2024 version, so this version supports the JDK 22.
[03:52] So behind the scenes I downloaded the JDK 22 and I configured the same JDK 22 as a Java version for
[03:58] this project.
[03:59] That's why I'm not getting any compilation error if you try to use these unnamed variable syntax, which
[04:05] is underscore with the previous versions of Java, then obviously you're going to get a compilation
[04:10] error.
[04:10] I hope you are clear with these
[04:12] scenario one.
[04:13] Now let's go to the main() method.
[04:15] So here we are catching that total words as an output.
[04:19] And we are trying to print the same.
[04:21] Now moving on to the scenario two, I have a List with the name fruits
[04:26] inside this List we also have some fruit names like apple, banana and orange.
[04:32] Now using these fruits ist object, I'm trying to invoke the stream() method so that I can process the
[04:38] elements present inside this List object.
[04:41] Post opening the stream, I'm trying to invoke one of the terminal operation supported by the stream
[04:47] API, which is collect to this collect.
[04:49] I'm trying to pass the code which is collectors.toMap().
[04:53] So what is this toMap().
[04:55] It is going to do to this toMap().
[04:57] We are going to pass a lambda expression.
[04:59] On how to build a map based upon the lambda expressions that we have provided.
[05:04] So the very first lambda expression that we have here, it is going to be used to build the key values.
[05:11] Whereas the second lambda expression it is going to be used to build the value inside the map.
[05:18] So to build our keys we're trying to use the element inside the stream which is fruit name.
[05:24] So that's why I'm trying to give the variable name as f.
[05:26] So the same fruit name I'm trying to assign as a key inside my map.
[05:31] But coming to the value, I'm trying to hardcode a value which is fruit.
[05:36] So for all the key names like apple, banana and orange, I'm going to have a same value which is fruit.
[05:43] So if you see that tricky scenario here, this v is an unused variable inside my lambda expression,
[05:51] nowhere inside my lambda expression
[05:53] I'm using these v
[05:55] so this v also can be replaced with the unnamed variable which is underscore.
[06:00] You can see the warning also resolved.
[06:02] And at last I'm trying to display the fruitMap onto the console.
[06:07] So let me try to execute this program so that we can see the output of this scenario one and scenario
[06:12] two.
[06:12] So if I try to execute this program in a debug mode, you'll be able to see the output from the scenario
[06:18] one is five, which is the total count of the elements present inside the List object, whereas the
[06:24] scenario two output is a map which has a keys like banana, orange, apple and the value for all these
[06:32] keys is fruit.
[06:33] Because inside our business logic, we are trying to populate the same value for all the map keys.
[06:40] So here you can see I'm trying to use the unnamed variables.
[06:43] And with this my code is going to look good and it is also going to have better readability.
[06:49] It is not going to have any warnings.
[06:52] And it is also going to give some information to other developers that this is an unused variable.
[06:58] So don't try to delete these or don't try to use these inside the business logic because that may change
[07:04] the overall output.
[07:05] So this kind of heads up, we are going to go to the other developers who are going to work on your
[07:10] code in future.
[07:11] So we saw the scenario of lambda expression also.
[07:14] Now moving on to the scenario three, I have a method which is convertAndDisplay().
[07:20] So let me open the same.
[07:21] So inside this method we have a simple logic which is we are going to accept and String input the same
[07:29] String data we are trying to parse and convert into a into variable.
[07:34] So if the parsing is going to be successful, we are going to return the output as true.
[07:38] Otherwise, if we end up having an exception like NumberFormatException and any other kind of exception,
[07:44] we are going to return the false as an output.
[07:47] So inside this method also, you can see we are not using the output from the parseInt() method.
[07:54] Maybe the intention of the developer is the developer.
[07:57] Simply want to understand if the String holds a proper int value or not.
[08:01] To handle this scenario, the developer has written this code.
[08:05] Since this is a unused variable, I can replace this with underscore, or I can also delete this entire
[08:14] unused variables.
[08:15] And this is an acceptable solution in this scenario, because in Java catching the return type is optional.
[08:22] But this code is not going to look good.
[08:24] So to improve the readability, I'm going to bring back my unused variable.
[08:28] But to resolve this warning related to unused variable, I'm going to use the unnamed variable syntax
[08:35] which is underscore.
[08:36] Now inside these catch blocks also there is an unused variable like ex which is the variable name for
[08:44] this NumberFormatException.
[08:45] And for this exception we are nowhere using these variables inside the catch block, we're just trying
[08:52] to print out some statement and return A isValid as false.
[08:56] Off course, this is not a production standard code.
[08:58] In production standard code, we're going to use the loggers instead of System.out.println().
[09:03] In this kind of scenarios.
[09:05] Also, we can use the unnamed variables to improve the readability of the code.
[09:11] We can see now where we are getting the compilation error, but if you are having the thoughts of removing
[09:17] the entire underscore and simply mentioning the number format exception, then we are going to get a
[09:22] compilation error.
[09:23] Because inside Java we have a syntax that needs to follow whenever we are defining a catch block.
[09:29] So that's why we can't completely get rid of this unused variable.
[09:33] So what is the perfect solution here?
[09:35] The perfect solution is to use the unnamed variable syntax.
[09:39] I hope you are clear with this scenario three.
[09:42] Now let me go back to the main() method.
[09:45] Inside that scenario four we are going to explore a method which is execute if file present.
[09:51] So there is a method inside the class which is going to execute some piece of logic.
[09:56] If there is a file is present in a given.
[10:00] In this kind of scenario to check if a given file is present inside the given path or not.
[10:05] I'm trying to use a try with resource syntax inside the try with resource, I'm trying to create an
[10:11] object of buffer reader, and to this object of BufferReader, I'm trying to pass the object of file
[10:17] reader along with the file path.
[10:19] So if there is no file available with this name, then obviously I'm going to get an exception which
[10:26] is FileNotFoundException.
[10:28] And with that, the logic present inside the try block is not going to be executed.
[10:33] So here the intentions of the developer is good, but the developer end up creating an unused variable
[10:40] which he can't delete.
[10:41] So to resolve this issue here also we can use an unnamed variable syntax and inside the catch blocks
[10:48] here
[10:48] also, we are nowhere using these variables like FileNotFoundException and IOException inside the
[10:54] catch block.
[10:55] So here also we can use the underscore to improve the readability of the code.
[11:00] So let me execute this program and see the output.
[11:03] You can see we are getting a FileNotFoundException as an output.
[11:07] Because there is no file inside my system with this name
[11:11] that's why straight away this catch block is getting executed, due to which we are seeing this message
[11:16] on the console.
[11:17] I hope you are clear with these scenario as well.
[11:20] Let me go back to the main() method.
[11:21] Inside this scenario, I'm going to show you on on how to use the unnamed variables as part of their
[11:28] records.
[11:29] You can see I have a class with the name point.
[11:31] If you can click on this, I have a record declaration with the name point inside the same class.
[11:37] So what is record
[11:38] inside Java record is a new enhancement introduced inside Java that is going to help you to create an
[11:45] final class, which is capable of creating immutable objects.
[11:50] So this piece of code behind the scenes, it is going to create a final class with the name point.
[11:55] And this point class is capable of storing couple of variables, which is x and y.
[12:01] So using these point I'm trying to create an object you can see with the help of new operator and invoking
[12:08] the constructor I'm trying to pass seven and three.
[12:11] Seven indicates what is the x coordinate and three indicates what is the y coordinate.
[12:16] So based upon these point object I have written an if block
[12:21] so inside the if block I have a condition which is.
[12:24] If point variable is an instance of point class, then execute this piece of code inside the if block.
[12:33] I'm trying to print a statement which is point object with the value of x.
[12:38] So here I'm not using the y variable.
[12:42] So in this scenario also I can remove these y which is an unused variable inside this if block and replace
[12:50] this with the unnamed pattern.
[12:52] So if I select this option you can see I am getting underscore.
[12:55] But here you can see the entire parameter is replaced.
[12:59] We can either mention int underscore or we can simply mention underscore
[13:05] so here though we are not mentioning int.
[13:08] Still it is working because my compiler, it has a context about the second parameter which is int y
[13:17] based upon the declaration that we have done here.
[13:20] So that's why compiler is not going to complain anything in this scenario.
[13:25] So this is another flavor of unnamed variables.
[13:28] In total we discussed about five different scenarios.
[13:32] So these are the typical scenarios that you may face on your day to day coding.
[13:36] Feel free to use the unnamed variables if you are using the JDK 22 version.
[13:42] As of now, we discussed everything about the unnamed variables.
[13:45] Apart from unnamed variables, we also have unnamed patterns also introduced as part of Java 22.
[13:53] So let's try to understand what are these unnamed patterns for the same
[13:58] I have created a Vehicle interface.
[14:01] You can see I have created a sealed interface with the name Vehicle, which will allow implementing
[14:07] only for the subclasses car, bike and truck.
[14:10] So these classes also are declared inside the same interface.
[14:15] So each of these subclasses are going to implement the interface Vehicle.
[14:18] And inside these Bike I have a variable with the name brand.
[14:22] And there is a constructor
[14:24] and there is a getter method which will return me a brand.
[14:27] Similarly, under Car I have a variable name with the name model.
[14:32] Using the same model variable, we have a constructor and we have a getter method, and similarly we
[14:38] have a truck subclass which is implementing Vehicle and it has an instance variable with the name manufacturer.
[14:46] So these are the few subclasses and interfaces that have created for our demo purpose.
[14:51] Now let me open another class I have here.
[14:55] So the class name is Unnamed Patterns.
[14:57] So inside this
[14:59] class, we can go to the main() method in few seconds, but before that we have various other static methods
[15:05] like process car, process bike, process truck, all these static methods, they're going to accept
[15:11] the input parameter in the form of parent data type which is Vehicle.
[15:16] So inside these methods I'm going to check if the given input is an instance of Car.
[15:22] Then I'm going to execute this method which is processing Car model.
[15:27] And to this message I'm going to append the value I have inside the model variable coming to the process
[15:34] Bike.
[15:34] If it is a bike, we are going to invoke the getBrand() method.
[15:37] If it is a track, we are going to invoke the getManufacturer () method.
[15:41] So these are the some static methods that we have inside our class.
[15:45] Now let's go to our main hero which is main() method.
[15:49] So inside the main() method I'm trying to create an object of track by passing the manufacturer name as
[15:57] Toyota.
[15:57] On the left hand side you can see I'm trying to catch the object with the help of the interface data
[16:03] type.
[16:03] Now here comes the main logic which is related to the unnamed patterns.
[16:08] So here you can see I have a switch statement.
[16:12] We call these kind of switch syntax as switch expression.
[16:16] Using the switch expression I have written some logic which is, if the Vehicle is of type Car, I want
[16:24] to invoke this method which is processCar() vehicle, whereas if the vehicle is of type Bike, I want
[16:30] to invoke this method, whereas if the vehicle is of type track, I want to invoke this method.
[16:35] So here I have a local variable which is vehicle, the same local variable I'm trying to use inside
[16:42] a switch expression.
[16:43] So whenever we use local variables as part of switch expression we can call them as type patterns.
[16:49] Because this local variable helping my switch expression to identify what is the type of the object
[16:56] like, whether it is a Car or a Bike or a Truck.
[16:59] I hope you are clear.
[17:00] What is a type pattern?
[17:01] Now coming to the unnamed pattern inside this switch expression, you can see I created a variable which
[17:08] is Car, Bike and Truck.
[17:10] Nowhere inside my business logic I'm using these variables, which in other words we can call them as
[17:17] type patterns.
[17:18] So in these kind of scenarios also we can use the underscore symbol.
[17:23] But here we should not call them as unnamed variables.
[17:27] We should call them as unnamed patterns.
[17:30] So let me replace all these type patterns with the unnamed patterns.
[17:35] So with this I'm assuming you're clear on what is unnamed pattern.
[17:39] So let me execute this program.
[17:41] And you can see we are getting the output which is processing truck manufacturer Toyota.
[17:47] I hope you are clear about what are unnamed variables and unnamed patterns that are introduced as part
[17:54] of Java 22.
[17:56] If you have any questions, please refer to the code that we have discussed so far inside this video.
[18:01] All the code that we have discussed so far inside this video, you can find it inside the GitHub repo.
[18:08] Thank you,
[18:09] bye.

----------------------------------------
