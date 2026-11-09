# 4.34 — Debugging of method invocations in IntelliJ

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] Inside this lecture, I'm going to talk in detail about the method invocations.
[00:05] we already know how to invoke methods, but the purpose of this lecture is along with the method invocations,
[00:11] I'm also going to teach you how to debug the methods which are available inside your Java classes or
[00:17] inside your Java project.
[00:19] To get started around this, let me close all the Java classes
[00:23] right now I have,
[00:24] I can right click on one of the Java class and choose the option close all tabs.
[00:30] This will close all the Open Java classes.
[00:33] Now let me go to the Java project and under this source folder I'm going to create a new Java class.
[00:40] And I'll keep the Java class name as method invocation demo.
[00:46] So this is the class name that I want to keep.
[00:48] Let me create this class.
[00:49] So the class is created with the empty class body inside this class,
[00:53] first let me try to create the public static void main().
[00:57] After the main() method I want to create multiple instance or non-static methods.
[01:02] The very first method that I want to create here is public void and the method name
[01:07] I will keep it as method1(), and it is not going to accept any input parameters.
[01:11] And inside this method1(), I'm just simply going to write a statement which is System.out.println().
[01:17] and to this println() method I'm going to pass the String which is method1().
[01:22] Apart from this System.out.println(), I also want to declare a variable which is int number is equal
[01:30] to some random value, which is 10.
[01:33] So similarly, let me create multiple methods like
[01:36] I'll copy the same method multiple times, and each of the method I'm going to rename to method2(),
[01:43] followed by method3() and followed by method4().
[01:47] So right now we have total four methods where they have very similar business logic.
[01:53] Let me try to make some changes inside these methods that I have created just now.
[01:57] I will try to change this value from method1() to method2().
[02:01] And similarly here I'll mention it as method3() and post that I'm going to mention as method4().
[02:07] After this, I'll go back to the method2() and mention the return type as String.
[02:12] Once I mention the return type for the method2(), I'm going to delete this line of code, and in the
[02:18] same place I'm going to create new line of code like
[02:21] I'll try to create a variable which is String.
[02:24] After mentioning the String data type, I'll mention the variable name as output to this variable
[02:29] I'm going to pass the String data, which is Hello World.
[02:34] The same
[02:34] I'm going to return from my method by using the return statement which is return output variable.
[02:41] So now let me try to add different logic inside method3() and method4() also.
[02:46] Maybe my method3() is going to accept an input parameter with the parameter name as input
[02:54] and the same input.
[02:55] It is going to print it on the console as well.
[02:59] So that's what I'm trying to do here.
[03:01] Let me delete this into number is equal to 10.
[03:03] And at last for method4() I want to accept the input parameters like into name and the same number.
[03:10] I want to print it on the console by using the input parameter value that I have received.
[03:16] So these are the methods that I randomly developed.
[03:18] The reason why I have developed so many methods is I want to invoke multiple methods in a single execution,
[03:26] and in the same process, I'm going to show you how the JVM or the Java is going to maintain all these
[03:32] method invocations.
[03:34] So from the method1(), I'm going to invoke the method2().
[03:38] Since it is an instance method, we can directly call the method2() using its name.
[03:43] When we call the method2(), we're going to get an output from the method2().
[03:47] Let me try to accept the same using the output variable inside the method1() the same output value.
[03:54] I'm going to print it here by using the variable output.
[03:58] Now I'll go to the method2(),
[04:00] from method2(), I will try to invoke the method3(). To invoke the method3(),
[04:05] just after this, I'm going to invoke the method which is method3(), and to this method3(),
[04:11] I'm going to pass an input value which is Hi.
[04:15] You can see while I'm trying to invoke this method3() I'm trying to pass the input parameter.
[04:20] I cannot invoke the method3() as a last statement just after the return statement, because always
[04:27] your return statement should be the last statement inside your method.
[04:31] You can see that's why I'm getting an error since I have mentioned that Java code after the return statement,
[04:36] my code is never going to be reachable.
[04:39] So you can see " Unreachable statement " is the error that we are receiving.
[04:43] So to resolve this issue, I need to mention this just above the return statement.
[04:48] Now from the method3() I want to invoke the method4().
[04:53] So let me invoke the method4() by passing a random number which is 10.
[04:57] So my method4() is going to accept
[05:00] the input value 10 and the same it is going to print.
[05:03] So you can see here first someone is going to invoke my method1().
[05:07] From method1() we are trying to call the method2().
[05:10] From method2(), we're trying to call method3(),
[05:13] from method3(), we're trying to call method4().
[05:15] I'm assuming you understand the chain of method invocations that are going to happen with this program.
[05:21] Using these chain of method invocations only, I'm going to teach you how to debug your Java methods,
[05:27] and how the method invocations are going to be maintained by your JVM.
[05:32] So now my methods are ready.
[05:34] As a next step, I need to invoke this very first method from my main() method, because my JVM is going
[05:41] to start the execution from the main() method only.
[05:43] Since my main() method is a static method, and this method1() is a instance or non-static method, I
[05:49] cannot directly call the method1() from my static main() method.
[05:54] So you can see I'm going to get a compilation error.
[05:57] So what is the solution that we need to follow to invoke the instance method from the static method.
[06:03] First we need to create the object of this class.
[06:06] So let me mention the class name first, followed by what is our object reference name?
[06:11] I'll just mention the object reference name as demoObject and post that I'll mention new operator followed
[06:19] by what is the class name?
[06:21] Now using this demoObject variable, I'm going to invoke the method1().
[06:26] With this, we should be able to invoke the method1() without any issues.
[06:30] So what I'm going to do is before I try to invoke this method, I'll try to keep a breakpoint inside
[06:36] my main() method so that we can stop the execution of the program
[06:40] at this point of time, let me try to execute this program in a debug mode with the help of this debug
[06:46] button.
[06:46] Now you can see the breakpoint stopped the execution at the main() method at the line number four.
[06:52] So at this point of time inside the debug window, I only have the arguments which I have received for
[06:59] this method as an input parameter, and there are no values
[07:02] that's why it is showing as empty here as a next step, let me move on to the next step.
[07:07] To move on to the next step, you can click on this step over at the shortcut that it is showing here.
[07:13] So if I try to click on this button, you can see now the execution moved to the next line.
[07:19] At this line the method1() is going to be invoked.
[07:22] So to debug the method1() there are two options that you have
[07:26] either you can directly put a breakpoint here inside the method1() like you can see here.
[07:31] And you can release the breakpoint.
[07:33] If you release the breakpoint the next breakpoint will stop
[07:36] here.
[07:36] You already aware about this, but this time I want to show you something new.
[07:40] Now, since the execution stopped at the line number five, you should be able to see the same here
[07:45] also, I want to use these step into button.
[07:49] The shortcut for this is F7.
[07:51] So if you click on this step into button, the execution will be taken into the method that you are
[07:58] trying to invoke.
[07:59] So what is a method that we are trying to invoke here,
[08:01] method1().
[08:02] So let me use this button.
[08:04] And you can see right now the execution is inside the method1() at the line number nine.
[08:10] Let me try to use this step over to move on to the next line.
[08:14] If I try to click on this button one more time, I can go to the console and I should be able to see
[08:20] the method1() output.
[08:21] Now the control is at the line number 11,
[08:24] you can also confirm the same here.
[08:26] At this line we are trying to invoke one more method, which is method2().
[08:30] If I want to debug method2()
[08:31] also I need to press the step into button.
[08:34] If I click on this, you can see the execution stopped at the very first line of method2().
[08:40] Let me click on this step over and if you go to the console, you should be able to see the method2()
[08:46] output on the console.
[08:47] Now the execution stopped at the line number 18.
[08:50] If I go to the debugger window, you should be able to see the same here under the method2() at the
[08:56] line number 18, the invocation
[08:58] right now it is stopped or passed.
[09:00] So at this point of time, if I want to enter into the method3() and debug line by line, then I
[09:06] need to use the step into button.
[09:08] You can see right now I entered into the method3()
[09:11] and if I try to use this step over, I will be able to see the two output values inside the console.
[09:17] One is high and the second one is method3().
[09:20] So now we are at the last line of the method3() where we are trying to invoke the method4().
[09:25] Let me use this step into which will take me into the method4() and inside this method we are trying
[09:32] to print the System.out.println() with the value num 10.
[09:37] So if I go to the console, you should be able to see that the ten value on the console.
[09:41] And right now the position of the execution point is at the last line of the method4().
[09:46] From this method, we are not going to invoke any other methods.
[09:50] Now, at this point of time, I want you to look very carefully at the debug window.
[09:56] You can see first there is a main() method at the bottom.
[09:59] Next
[10:00] we have a method1() inside the method1() at the line number 11, we invoke the method2().
[10:05] So that's why on top of the method1(), we have method2().
[10:09] Similarly
[10:09] method3(),
[10:10] method4().
[10:11] When you select each of these method debug points, you will be able to see what are the values available
[10:18] at that particular point of time.
[10:20] Inside the method4(), we have the variables with the name num and the value is 10.
[10:25] That's why I'm able to see the same here.
[10:27] If I select the method3(), I will be able to see a different variable which is input with a value.
[10:32] Hi, because inside the method3(), the only variable we have is input.
[10:36] So let me go to the method2().
[10:38] Inside the method2(), we have a variable with the name output the same we are able to see here along
[10:45] with its value.
[10:46] If I go to the method1(), I will be able to see what is the variable available inside the method1()
[10:51] which is number.
[10:52] This way you can always stop the execution and see that what is happening or what is the data available
[10:59] at a particular method.
[11:00] So now where is the execution is waiting.
[11:03] You can click on this top method invocation which is method4().
[11:06] And you can see the line is highlighted in blue color.
[11:10] That means right now the Java execution is passed here and it is waiting for my instructions at this
[11:16] point of time.
[11:17] So here if I click on this resume program, then the program will keep running until it sees a next
[11:23] breakpoint.
[11:24] So nowhere I have a breakpoint inside my program.
[11:27] That means my program will be executed completely, and at the end it will also terminate.
[11:31] But I don't want to do that.
[11:33] Instead, I want to show you one more debugging approach.
[11:36] You can see there is a step out option, a step out button.
[11:40] You will be able to see the shortcut
[11:42] also here you can use either shortcut or you can click on this button manually
[11:47] whatever works for you.
[11:48] If I click on this step out, the execution will be moved from this method to the top method.
[11:54] Like from the method4(), it will move on to the to the caller method, which is method3().
[12:00] So let me click on that.
[12:02] You can see right now the execution stopped at the method3() after this line
[12:07] now let me click on the step out one more time.
[12:09] This time you can see the execution stopped in method2().
[12:13] As you are trying to step out from the methods inside the debug window, all the method details will
[12:19] be removed because we are done executing those methods.
[12:23] So right now there is no entry about method3() and method4(), because right now we are done executing
[12:28] them.
[12:29] If I click on this step out from the method2(), I'll go to the method1() and from method1()
[12:35] if I try to click on step out, I will go back directly to the main() method.
[12:39] So there is one more line to execute.
[12:41] So whenever you are using step out, that means you don't want to examine any other next statements
[12:47] available inside the method.
[12:48] You simply want to go to the parent method.
[12:50] So that's what it is going to happen here.
[12:53] As soon as I click on this step out, I'll go to the main() method.
[12:57] So to let my program continuously I can click on this resume program.
[13:02] And this will run the program continuously.
[13:04] If there are no other breakpoints inside my further execution logic.
[13:09] So let me release this.
[13:10] So at last you can see the program terminated.
[13:12] And these are all the outputs that we have received.
[13:15] I hope you understand how to debug the code.
[13:18] So there are multiple buttons available.
[13:20] All these buttons are going to help you to debug your code and to understand what is the data at that
[13:26] particular point of time.
[13:27] Because inside the real projects, whenever there is a defect or bug is identified by the testing team
[13:34] as a developer, you need to debug your code, and in the process, you may see hundreds of methods
[13:40] being invoked inside your business flow.
[13:43] As a developer, you need to play an very smart role here.
[13:47] First, you need to have initial hunt about where could be the issue.
[13:51] Based upon your doubt, you need to put a breakpoint in that method and you can debug the surrounding
[13:56] methods as well if needed.
[13:58] I'm going to put enough efforts throughout this course to teach you about the debugging inside intelliJ,
[14:04] but if you are looking for more details around that debugging inside the IntelliJ, the official website
[14:10] is the right place for you to learn about how to debug the code inside the intelliJ.
[14:15] You can go to this URL
[14:17] inside this URL, you will be able to see a heading with the name debug code, which will tell you what
[14:22] is the importance of debugging and how to do various types of debugging.
[14:26] You also have videos like Debugger Essentials which is going to teach you the basics, and similarly
[14:33] Debugger Advanced, Debugger Professional.
[14:35] By watching these official videos, you should be easily mastered the debugging inside intelliJ.
[14:42] And believe me, the same style of debugging is going to be followed by other IDE's like Eclipse and
[14:48] Visual Studio Code.
[14:49] So if you learn debugging in one of the IDE, the same knowledge can be leveraged whenever you try to
[14:56] use another IDE.
[14:57] Under this debugging, you also have sections
[14:59] like about breakpoints.
[15:01] There is a detailed discussion about the breakpoint, how to start the debugger session, details about
[15:06] the debug tool window, so all the details that we are going to discuss, you can find it inside this
[15:11] page.
[15:11] I'm going to mention these page details also inside the GitHub repo.
[15:15] So please please refer to this page and try to understand more about the debugging of the code because
[15:21] it is very important for your developer career.
[15:24] A developer who knows debugging,
[15:26] he can fix the issues fastly and he can identify the defects in his code fastly.
[15:33] Just by looking at the source code
[15:35] no one can identify what defect is present inside the code.
[15:39] Before I try to close this lecture, I want to show you an image.
[15:42] You can see this is an image where we are able to see a stack of plates.
[15:47] Why I'm showing this right now because the method invocations inside Java, they follow the stack data
[15:55] structure.
[15:55] So how the stack data structure works by using a principle called LAST IN FIRST OUT (LIFO). In short form
[16:03] we can also call it as leaf or LIFO.
[16:06] That means inside a stack, whatever last element came into the picture, that is the first element
[16:13] which is going to be removed from the stack.
[16:16] So here you can see there are good amount of plates.
[16:18] So what is the last plate that joined the stack,
[16:21] the top plate.
[16:22] So if you want to remove a plate first you need to remove the last plate that came into the stack.
[16:28] So that's why we call the design principle of stack as last in first out.
[16:33] The same principle is followed inside the method invocations as well.
[16:38] Whatever is the latest method that you invoke that will be at the top of the method stack?
[16:43] I can also show you that in the demo once.
[16:46] So here, let me keep a breakpoint inside the method4().
[16:49] Because this is the last method, we are going to invoke and remove this breakpoint inside the main()
[16:53] method.
[16:53] If I try to run this program in a debug mode, you can see this is a stack of methods invocation.
[16:59] So what is the top method that we have?
[17:02] The method that which entered at the end.
[17:05] So method4() came at the end,
[17:07] that's why it is a top element inside the stack that is maintained by the JVM.
[17:12] So if you want to execute method3(), first you need to complete the method4() execution, because
[17:18] method3() is dependent on the method4().
[17:21] If I click on this step out, then the method4() execution will be completed.
[17:25] That means the top element at the stack will be removed, and you can see right now the top element
[17:32] will be method3().
[17:33] So if anyone asks you how the method invocations works inside Java, please let them know that it follows
[17:39] the stack data structure design principle.
[17:43] I hope this all makes sense to you.
[17:45] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
