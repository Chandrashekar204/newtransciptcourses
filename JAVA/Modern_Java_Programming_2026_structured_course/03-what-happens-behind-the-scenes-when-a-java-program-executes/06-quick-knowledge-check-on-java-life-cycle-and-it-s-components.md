# 3.6 — Quick knowledge check on Java life cycle & it's components

> Section 3: What happens behind the scenes when a Java program executes

[00:00] Now is a testing time.
[00:02] Inside this lecture, I'm going to ask a few questions and you need to answer yourself.
[00:07] And please be very sincere here.
[00:09] If you are saying a wrong answer, then you need to promise me that you are going to watch last two
[00:14] lectures.
[00:15] The reason why I am emphasizing a lot on these basics is you should always know what happens behind
[00:21] the scenes
[00:22] as a Java developer, I see many Java developers without knowing these basics
[00:27] they try to learn java, but someday they will get into some situation where they are not able to excel
[00:34] in their Java career because they don't know the basics of Java.
[00:38] These very similar to your car driving. As a car owner or as a vehicle owner.
[00:43] Apart from driving your vehicle, you should also know how your car works.
[00:48] You should know what kind of fuel or gas it accepts, and you should be able to handle minor repairs.
[00:55] Like if there is a flat tyre, you should know how to change your tyre,
[00:58] if you don't know about all these basics of your vehicle or your car, then someday you will be into
[01:05] problems just because you don't know basics about your car.
[01:09] Very similarly, the same applies for Java programming language also,
[01:12] that's why I'm trying to put lot of efforts here to teach you around the basics.
[01:17] Are you ready for the very first question?
[01:20] The first question is, is Java language platform dependent or independent?
[01:25] This is going to be very easy.
[01:27] I'm going to count three and you need to answer yourself one, two, three.
[01:32] Yes, you are correct.
[01:34] Java is a platform independent language, which means we can write Java on windows operating system
[01:41] and can be executed on a mac or Linux operating system.
[01:46] The resulting output is always going to be the same.
[01:49] You're doing great.
[01:50] Let's move on to the second question.
[01:51] The second question is, is Java software platform dependent or independent?
[01:56] So I'm trying to trick you here.
[01:58] Please see the question very carefully.
[02:00] Is Java software platform dependent or independent?
[02:05] The answer is very easy.
[02:06] Do you want a hint?
[02:07] The hint is whenever you try to install Java inside your system, the Oracle or other JDK vendor website,
[02:14] they are going to ask you which operating system you are using.
[02:18] I hope you are able to answer with this hint.
[02:20] Yes, you are correct, Java software is a platform dependent.
[02:24] So when I say Java software, I'm indirectly referring to JVM.
[02:28] So with the help of JVM which is platform dependent, our Java language is acting as a platform independent
[02:36] language.
[02:37] The next question is is JVM installed automatically with operating system.
[02:42] So this is going to be super simple.
[02:44] Please ask yourself if you buy a brand new laptop,
[02:47] do you think by default JVM installed inside your system?
[02:50] Off course not, because JVM comes with the Java installation inside your JDK folder, only JVM is going
[02:57] to reside.
[02:58] This means the answer is no.
[03:00] JVM is not installed automatically with the operating system.
[03:04] We need to install Java ourselves based upon our operating system.
[03:08] The last question that I want to ask here is, what are the important components of Java installation?
[03:14] We discussed a lot about this.
[03:16] The very first important component is JDK.
[03:19] The next one is JVM and the last one is JRE.
[03:22] So let's see what is that details about that JDK refers to the Java installation folder which have all
[03:29] the necessary tools to develop, compile and run your Java program, whereas Java Virtual Machine,
[03:35] it is an abstract machine or a virtual machine that provides a runtime environment in which the Java
[03:41] programs can run.
[03:43] And this JVM interprets the compiled Java bytecode and provides a layer of abstraction between your
[03:49] code and the underlying operating system.
[03:53] And at last, what is JRE,
[03:54] JRE means Java Runtime Environment.
[03:57] It is a subset of JDK that includes only the JVM and other components that are required to run your
[04:04] Java application.
[04:05] With the JRE, you cannot compile your Java code, but you should be able to run your compiled Java
[04:11] code with the help of JVM present inside the JRE.
[04:15] But today is there available.
[04:17] JRE is no more available from JDK 9.
[04:20] If you an organization looking to build their own custom JRE, then they need to use the jlink option
[04:27] available inside the Java.
[04:29] With this, I'm assuming your super clear with the life cycle of Java program. As of now
[04:34] we discussed everything through the slides.
[04:36] Now as a next step, for the next few lectures, let me teach you how to compile your Java code, how
[04:42] to execute your Java program with the help of JDK and JVM, and all the concepts that we have discussed.
[04:50] I hope you are excited for the demos.
[04:51] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
