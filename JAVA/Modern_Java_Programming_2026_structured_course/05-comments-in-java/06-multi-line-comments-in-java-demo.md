# 5.6 — Multi line Comments in Java - Demo

> Section 5: Comments in Java

[00:00] Let's see the demo of multi-line comments by creating few methods and classes inside my section5
[00:07] Java project, I'm going to create a new Java class.
[00:11] The name I want to give for this class is Customer.
[00:15] Think like I want to document about this class the purpose of this class,
[00:19] why someone should create an object of this class,
[00:22] what kind of information the object of this class is going to hold to share all such details, single
[00:28] line comment may not be sufficient.
[00:31] That's why I'm going to use multi line comments here.
[00:34] The syntax that we need to follow whenever we want to define multi line comments is, first we need to
[00:40] mention /* Mark inside your intellige as soon as you press enter
[00:46] after mentioning the asterisk mark, the end symbol also will automatically populate.
[00:51] You can see this is the end symbol which is going to have */.
[00:57] And this is the starting symbol.
[00:59] I can write any number of lines of comments between these multi-line comment symbols.
[01:06] Let me try to define some multi lines of comments.
[01:09] I'm going to paste few lines of comments here just to save some time.
[01:12] Like you can see here
[01:13] I have mentioned multiple lines of comment, the comment clearly saying what is the purpose of this class?
[01:19] You can also see my intelliJ is graying out all these comments, which means my Java compiler is
[01:26] going to ignore all the comments that we have written with the help of multi line comments here, you
[01:32] may be thinking that we should always start these first line of multi line comments in the next line
[01:39] of the starting symbol.
[01:40] That is not mandatory.
[01:41] You can always start immediately after your starting symbol of the multi line comment.
[01:47] And you can also terminate your comment by immediately mentioning the ending comment
[01:52] like this.
[01:53] So this way also you can define multi line comments, but I would always recommend you mentioning the
[01:58] starting symbol and the ending symbol in their own lines, so that it will improve the readability of
[02:04] your multi line
[02:06] comments.
[02:06] So now we have defined comments on top of it Java class.
[02:10] Very similarly we can define the documentation of a Java method.
[02:14] So to create more multi line methods I'm going to create one more class,
[02:19] the class name is going to be MultiLineCommentsDemo.
[02:23] This is the class name.
[02:24] And inside this class first I'm going to create public static void main() by using the shortcut psvm.
[02:31] And after that I'm going to create a method which is public double,
[02:37] after double I need to mention the method name.
[02:40] The method name is going to be calculateRectangleArea().
[02:43] To this method I want to accept two input parameters.
[02:47] The very first input parameter is double length and the second input parameter is double width.
[02:54] After declaring the method, I want to write the business logic, which is the product of these two
[03:00] input parameters
[03:01] I want to return as an output.
[03:04] So to multiply two variables inside the Java, we need to use a symbol, which is asterisk.
[03:11] So I'm trying to multiply the values represented by these two variables like length and width.
[03:16] Think like I want to document more details about this method.
[03:19] I know it is very simple, but let's imagine this method has some complex business logic with that assumption
[03:26] If I want to document this method, first I need to start the /*
[03:33] and I'm going to press enter.
[03:34] And my interface is going to automatically populate the end symbol for my multi-line comments.
[03:41] Now here I can define multi lines of comments.
[03:44] So let me paste few lines of comments here so that we can discuss very quickly.
[03:48] So these are the comments explaining about the purpose of this Java method.
[03:53] Very similarly we can also define multi level comments on top of a Java field as well.
[03:58] The field can be within a method or it can be a class level Java field.
[04:03] Regardless of where the field are variable is present
[04:06] the process is going to be same.
[04:07] Here I'm going to create a class level static variable for the same,
[04:13] I'm going to mention static.
[04:14] Since I want to define a final variable, I'm going to use the final keyword and mention that data type
[04:20] as int, followed by what is the name of the variable?
[04:23] The name of the variable that I want to give here is MAX_RETRY_ATTEMPTS, and to this I want to assign
[04:30] a constant value 3.
[04:31] In the previous lecture also, we have defined very similar kind of variable inside the
[04:36] SingleLineCommentsDemo class.
[04:37] And here I tried to explain about this variable within a single line of comment.
[04:43] But sometimes it may not be sufficient, and we may want to share more details about the variable.
[04:50] In such scenarios we can go with the multi-line comments.
[04:54] So let me mention the multi line comments here.
[04:56] I have mentioned the purpose of this variable with
[05:00] these lines of statements.
[05:01] With this, I'm assuming you are clear on how to define multi lines of comments on top of a field,
[05:08] on top of a variable, on top of a method, or on top of a class.
[05:12] So there is no restriction where we can use these multi line comments if needed.
[05:17] You can write these multi line comments inside your Java methods or inside a block of code.
[05:23] It's up to you based upon your requirements you can leverage them.
[05:27] Now let me show you how to comment out the code with the help of multi line comments.
[05:32] Think like I want to comment out this entire method, which means I want to temporarily deactivate this
[05:39] method or temporarily disabled this method so that no one can invoke this method.
[05:45] If they are trying to invoke they will get an error.
[05:47] I can also show you this in demo, since this is a instance method or a non-static method,
[05:53] in order to invoke this method, first we need to create an object of this class.
[05:57] So let me try to create the object of this class inside my main() method.
[06:02] So I'm trying to use a new operator and using the constructor of the MultiLineCommentsDemo(), I have
[06:09] created an object with the reference obj.
[06:12] Using the same reference, I'm going to invoke the method calculateRectangleArea() to this method
[06:18] I'm going to pass two double values like 24.5 and 34.6, and I'll terminate this statement and the output
[06:28] I'll try to catch into the variable which is total area is a variable name.
[06:35] The same I will try to print out onto the console.
[06:38] So if I try to execute this class you'll be able to see the total area which is 847.7.
[06:46] Think like
[06:47] for some reason I want to temporarily disable this method or deactivate this method.
[06:52] I have two options one
[06:54] I can remove this if I remove these permanently in future
[06:58] whenever I want to bring this back, then I need to type this method manually.
[07:03] So to avoid these kind of situations, we can comment out the method with the help of multi-line comments.
[07:10] To comment out this entire method, I can go just to before this public keyword and start the syntax
[07:16] of multi-line comment.
[07:18] And at the end of the curly brace of the method, I'm going to mention asterisk forward slash.
[07:24] With this you can see this entire method is commented out.
[07:27] That's why I'm getting a compilation error here.
[07:30] No such method available inside this class.
[07:33] There is also a shortcut that you can follow to comment out a method, or to comment out a block of
[07:39] code with the help of multi-line comments.
[07:41] Let me show you the shortcut. To demo you the same
[07:44] let's imagine that we want to comment out these three lines of code.
[07:49] So to comment out all these three lines, first we need to select all these three lines of code and
[07:53] go to the help and click on these Keyboard Shortcuts PDF.
[07:58] This is going to give you the list of shortcuts that you can follow inside your IntelliJ.
[08:04] I'm going to search for comments here.
[08:07] As soon as I try to search for comments, you can see there is a shortcut that we can use to comment
[08:12] out entire block of code.
[08:14] The shortcut in windows is Ctrl + Shift + /, whereas inside the mac it is going to be command
[08:23] option forward slash.
[08:25] I have to use a mac shortcut in my scenario since I'm using mac operating system.
[08:29] So based upon your operating system, please your own shortcut.
[08:33] I'm trying to press command option forward slash.
[08:37] And with that you can see my lines of code has been commented out with the help of multi-line comment
[08:44] syntax, we can use the same shortcut to uncomment the code.
[08:48] Maybe after few days I want to activate these code, or I want to bring back these code into my business
[08:55] logic.
[08:55] In such scenarios, you can remove these forward slash asterisk symbols manually.
[09:00] Otherwise you can select all the lines of commented code and type the shortcut which is command option
[09:07] button forward slash in my scenario.
[09:10] Accordingly, type your windows operating system shortcut.
[09:13] We can do the same for methods as well here
[09:16] also, I'm trying to select my whole method and I'm trying to type the shortcut
[09:21] and that is going to uncomment my code.
[09:24] So the process of removing the commenting is called Uncommenting.
[09:28] The same you can see for commenting or uncommenting with the block code you need to use the shortcut,
[09:34] whereas for the single line it is going to be this shortcut.
[09:37] Let me try to use the same.
[09:39] For example.
[09:39] Think like I want to comment out this System.out.println().
[09:43] I'm going to select this entire line and press the shortcut which is command forward slash.
[09:48] You can see the line of statement is commented with the help of single line comment syntax.
[09:53] I can press the same shortcut again to bring back my code with the help of Uncommenting process.
[09:59] Whenever possible, I'm going to share these kind of shortcuts that you can use inside IntelliJ,
[10:05] but my humble recommendation is to download these PDF and have it handy for the initial few months till
[10:13] you use to the shortcuts available inside IntellIj.
[10:16] So anytime you have question, open this PDF and try the shortcut multiple times so that your fingers
[10:22] and brain will get used to these shortcuts during your day to day development process.
[10:28] As a last step, let me show you the demo of writing the multi lines of comments in between the Java
[10:35] statement.
[10:36] So here I have a Java statement which is static final int MAX_RETRY_ATTEMPTS = 3.
[10:42] What I can do is just after this variable name, I can try to mention the syntax of multi line comments,
[10:50] which is /* and the ending should be */.
[10:57] So I can write some sample comment here between these two symbols.
[11:02] And my Java compiler is not complaining anything.
[11:05] The reason is it knows the entire content that we have written
[11:09] here is a comment, and it is going to ignore these entire comments.
[11:14] And with that, there is no issues with my Java statement.
[11:17] After the variable name I'm going to have, this is equal to followed by three, and at the end there
[11:22] will be semicolon.
[11:23] I hope this is clear, but my recommendation is never ever try to use these in between your Java statements,
[11:31] because that is a bad practice since it is going to reduce the readability of your code.
[11:37] With this, I'm assuming you are clear about how to define multi-line comments inside Java.
[11:43] Based upon your business requirements
[11:45] always feel free to use them to explain a complex piece of code.
[11:50] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
