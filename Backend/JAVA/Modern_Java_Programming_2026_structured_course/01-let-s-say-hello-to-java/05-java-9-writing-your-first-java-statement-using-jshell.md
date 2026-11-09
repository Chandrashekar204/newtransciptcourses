# 1.5 — [Java 9] Writing your first Java statement using jshell

> Section 1: Let's Say Hello to Java

[00:00] Inside this lecture, I'm going to teach you on how to print your name onto the screen with the help
[00:06] of a Java statement.
[00:08] I know it might be too early for us to explore this, because as of now, we didn't learn anything about
[00:14] Java.
[00:14] But there is a tradition that we need to follow whenever we're trying to learn a programming language.
[00:20] Do you know what is the tradition?
[00:21] The tradition is to write a simple hello world program.
[00:25] That's why let's try to follow the tradition.
[00:28] And in the same process, I'm also going to introduce a tool called jshell that we are going to use
[00:34] inside this course as well.
[00:36] Whenever we are trying to learn about Java keywords, Java statements, Java syntax.
[00:41] So here you may have a question like what is jshell?
[00:44] jshell means Java shell tool.
[00:47] So it is an interactive tool for learning the Java programming language.
[00:53] With the help of this tool you can prototype the Java code.
[00:57] Maybe you're trying to learn Java and in the same process you want to try whether a given particular
[01:02] Java code is going to work properly or not, or whether you want to check whether the given Java statement
[01:08] syntax is valid or not in all those scenarios, instead of you leveraging various text editors or various
[01:14] Java based products, you can simply leverage this jshell, which is going to give you the feedback
[01:21] immediately without a complex setup.
[01:23] So jshell is a tool that is going to work based upon the principle REPL.
[01:29] So what is REPL?
[01:30] Read Evaluate Print Loop.
[01:33] So based upon the instructions that you are going to give, this jshell is going to read your instructions.
[01:39] It is going to evaluate if the statement is correct or not.
[01:42] If the statement is correct, it is going to print an output from your statement, and the same process
[01:48] is going to loop again and again until you exit this jshell.
[01:52] And this particular jshell is introduced in the version of JAVA 9.
[01:57] So before JAVA 9, whenever someone want to learn Java with by giving some small instructions, they
[02:04] always have to go through the complex setup of installing an IDE like eclipse or IntelliJ Idea, which
[02:11] are the products that we are going to explore throughout this course as well.
[02:14] So when we install those products, they are going to make your life easy to write programs based upon
[02:19] Java language.
[02:20] So instead of installing all those products or text editors, we can directly leverage this jshell very
[02:26] quickly to learn Java.
[02:29] So to make students life easy who are trying to explore Java very first time, this jshell tool is
[02:35] introduced in the JAVA 9.
[02:37] Throughout this course I'm going to highlight inside the slides also when this particular feature is
[02:44] introduced.
[02:44] So if you see jshell is a feature which got introduced in the JAVA 9.
[02:48] That's why I have highlighted here inside the slide.
[02:51] So this is going to act as a reference for you.
[02:54] Since you are going to have the slides with you whenever you are trying to quickly brush up the concepts
[02:59] that we are going to discuss, these version numbers are also going to help you to understand when a
[03:04] particular feature is introduced.
[03:05] So we'll go to the installation process.
[03:08] I'll show you how to install Java,
[03:10] what is the version right now present in the market.
[03:12] So all those details I will show you in the coming lectures.
[03:15] But before that I want to make your hands dirty by writing a Java statement and printing your name on
[03:22] the console.
[03:23] So now you have details about jshell.
[03:25] The next question you may have is how can I print my name
[03:29] or how can I print a statement hello world onto the screen or the console?
[03:34] So this may sound very scary for you if you are new to the Java, so don't worry, this is going to
[03:39] be super, super simple.
[03:40] I'm going to guide you on the same. Like you can see here,
[03:43] whenever we want to print our name onto the console, we need to write this Java statement which is
[03:50] System.out.println and inside the brackets,
[03:54] we need to provide our name within double quotes, and at the end we need to terminate the statement
[04:02] with the help of semicolon.
[04:03] So don't worry about what is the System,
[04:05] what is this println.
[04:07] We're going to discuss all of them in the coming lectures.
[04:09] But for now, please note that since this is a very common requirement for any Java programs or for
[04:16] any Java applications to print a given output onto the console Java team, they have provided some inbuilt
[04:23] classes and methods that we can use to print a given input onto the console.
[04:28] So what are those predefined classes?
[04:30] System is a class available inside the Java library, and inside this System class we have a static
[04:38] variable with the name "out".
[04:39] So whenever we want to invoke a variable or a method available in a particular class, we need to use
[04:46] dot.
[04:46] So that's why after system we need to use dot.
[04:49] And after the dot we need to mention out which is a static variable.
[04:54] After that out, we need to mention dot one more time and mention the method name that
[04:59] we want to invoke the method name that we want to invoke here is, println.
[05:04] And to this method we need to pass the input that we want to print onto the screen.
[05:10] So here I'm giving my name which is Madan.
[05:12] So when you are trying to execute this Java statement you you can replace my name with your own name.
[05:18] So if you closely look at this Java statement which is System.out.println(), it is very clear
[05:24] that whenever we are trying to invoke a method or a variable inside a class, we need to use "." operator.
[05:32] So that's a very rule number one that you need to be aware.
[05:36] And this is one of the syntax that you need to aware to write Java based programs.
[05:41] And apart from this dot operator you should also take care of terminating your Java statement with a
[05:47] semicolon (;).
[05:48] So each and every instruction and every Java statement that we are going to write inside any Java program,
[05:55] it has to be terminated with a semicolon.
[05:58] So don't worry about why we should follow the semicolon.
[06:01] I'm going to explain that in the coming lectures.
[06:04] But for now, let's try to execute this Java statement and see the output on the screen.
[06:09] Usually these jshell will be available inside your local system whenever you install a Java.
[06:15] But as of now I'm assuming you have not installed Java.
[06:18] We are going to do that in the coming lectures.
[06:20] So we have some websites which are going to help us by providing a replica of this jshell tool in online.
[06:27] For the same,
[06:28] let me go to one of the website.
[06:30] The website is tryjshell.org, the same I'm going to mention inside our GitHub repo page as well.
[06:37] As soon as you try to land onto this page, you will be able to see the screen like this.
[06:43] You can see here the cursor is waiting for my input.
[06:46] So let me type the statement that we have discussed which is System.out.println().
[06:54] So please make sure you are following the same case sensitivity.
[06:58] If you try to give a different case sensitive alphabets, you're going to get a compilation error.
[07:03] For now, please type the exact statement that you're seeing on the screen.
[07:07] Since println() is a method, every method is going to have opening and closing brackets.
[07:14] And since I want to give an input to this println() method, I need to provide my name inside double quotes.
[07:21] So the name that I want to provide here is Madan.
[07:24] And since I'm done with the Java statement, I need to make sure I'm providing the colon here.
[07:30] If I try to press enter here, you can see I'm getting my name as an output, which is Madan.
[07:37] Hooray!
[07:37] We got a successful output!
[07:39] I'm assuming this is your very first Java statement that you have written.
[07:44] I hope you are able to see your own name on the screen. This time
[07:48] let's try to give our favorite person name.
[07:51] It can be your sibling name,
[07:53] it can be your parents name,
[07:54] It can be your girlfriend or boyfriend.
[07:56] The name can be belongs to anyone.
[07:58] But I just want you to try this statement one more time by giving the name of your favorite person.
[08:04] So to run the same command again, we can type the command again, or you can press the upwards arrow.
[08:11] If you try to press the upwards arrow, it will show you the last executed command.
[08:16] So here I'm going to replace the name of Madan with Saanvi.
[08:21] So who is Saanvi,
[08:22] saanvi is my daughter name, so I have given her name here.
[08:26] So similarly you can give your favorite person name.
[08:29] So if I try to execute this command by pressing enter, you will get the output as Saanvi.
[08:35] So do you see the beauty here?
[08:37] We're able to see our name and our favorite person name on the screen.
[08:41] Now as a next step, I'm going to share a few more details here.
[08:44] Whenever we are trying to use a jshell, giving the semicolon towards the end of the statement is completely
[08:51] optional.
[08:52] The reason why it is optional is, Java team
[08:54] when they develop this jshell tool, they want to give flexibility to the Java developers to not type
[09:00] colon for every statement.
[09:02] Behind the scenes
[09:03] this jshell tool is going to add the semicolon for you, but whenever you are trying to write a serious
[09:09] code inside your text editor or inside your Java based products, then you need to make sure you are
[09:16] completing that Java statement with the help of semicolon.
[09:19] But for jshell it is completely optional.
[09:22] So I can also execute this statement without semicolon and I'll get the same output.
[09:27] Now the next instruction that I want to share here is think like you're not following the syntax that
[09:33] is expected by the Java compiler.
[09:35] In that scenario, let's try to understand what is going to happen.
[09:38] Maybe I will not provide this bracket and try to execute this line.
[09:42] You can see my jshell is assuming that I'm going to provide the bracket in the next line.
[09:48] So once I provide the bracket in the next line, then only it is going to execute. Very similarly
[09:53] let's try to understand what will happen if I don't provide double quote after the name.
[09:58] So if I try to
[09:59] excute this command you'll be able to see and getting a compilation error saying that unclosed string
[10:06] literal.
[10:07] So there is a string value, or there is a text value, which is Saanvi, but I'm not closing that with
[10:12] a double quotes.
[10:13] With this, it is very clear that my compilation failed because I have not followed the Java syntax.
[10:20] So please try to make as many mistakes as possible and see the behavior of this jshell with this Java
[10:27] statement.
[10:28] This way you are going to learn a lot.
[10:31] Always
[10:31] please remember, the best way of learning any programming language is by making more mistakes.
[10:37] For your reference, I also mentioned the website details in this slide.
[10:41] So this is just Java statement that we ran and this is how the output is going to look like.
[10:46] And like I said, every statement inside the Java statement has to be terminated with a semicolon.
[10:52] But this semicolon is completely optional inside the jshell.
[10:56] So once you are exploring about jshell you can try to run a command which is /exit or /ex to close
[11:04] the session of jshell and to come out of that specific jshell connection.
[11:09] Like I said, please, please make lot many mistakes so that you can learn more about Java language.
[11:15] I can also show you some funny meme images which will show you the advantages of making mistakes.
[11:21] Are you ready for this
[11:22] funny note?
[11:23] So this is the very first funny meme that you can see here.
[11:26] There is a statement I learned a lot from my mistakes, so I decided to make more mistakes to learn
[11:32] more.
[11:32] So that's a motivation you should have always.
[11:34] So whenever you have done some mistake, don't get demotivated or don't get frustrated.
[11:39] The person who is going to make more mistakes, he is more knowledgeable than a person who got an output
[11:46] in the very first attempt.
[11:47] Let's try to see what is the next meme image that we have.
[11:50] So here you can see, a person
[11:53] he will grow a lot only if he make lot of mistakes.
[11:57] So this is one of the basic principle and how we are going to increase our knowledge inside any programming
[12:03] language.
[12:04] Let's move on to the next image.
[12:05] So here you can see there is a message saying that it's okay to make mistakes,
[12:10] we all make some silly mistakes.
[12:12] Don't worry about others like they are going to judge you about your silly mistakes.
[12:16] It's completely fine making silly mistakes, but you need to learn something from that silly mistake.
[12:22] So here the question is very simple.
[12:24] Which of the following is the largest?
[12:25] The person in a hurry.
[12:27] He didn't check the option which is the moon.
[12:29] She directly answered elephant as an answer.
[12:32] But obviously moon is bigger than elephant, so this is such a silly mistake.
[12:37] Usually a lot of these things will happen whenever you try to learn the programming language, so don't
[12:43] get demotivated.
[12:44] Let me show you the last image that I have here.
[12:47] Mistakes makes you stronger,
[12:48] we know that there is a person here,
[12:50] you can see after he completed an exam, you'll be able to see how strong he is because this person
[12:57] has done all his mistakes inside his exam
[13:00] only.
[13:01] Instead, the approach should be while we are practicing a programming language or while we are learning
[13:06] the programming language, we need to make lot many mistakes,
[13:09] we need to ask lot many questions,
[13:11] we need to try various combinations.
[13:14] Then only we are going to make less mistakes inside exams or inside interviews, or inside the real
[13:21] production code that we are going to write.
[13:23] So these are small motivation I want to give you.
[13:25] I hope you like this.
[13:27] With this, I'm assuming you are super happy with the first accomplishment that we have inside this
[13:32] course.
[13:33] So it is very small accomplishment, but we should be proud of ourselves that we are able to print our
[13:39] own name with the help of a Java statement.
[13:42] And in the same process, we also learned about the tool available inside the Java, which is jshell.
[13:47] I hope this all clear to you.
[13:49] Thank you.
[13:50] Bye.

----------------------------------------
