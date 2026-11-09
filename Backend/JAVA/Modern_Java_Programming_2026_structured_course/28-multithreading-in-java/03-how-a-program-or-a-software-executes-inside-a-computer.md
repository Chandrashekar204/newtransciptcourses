# 28.3 — How a program or a software executes inside a computer

> Section 28: MultiThreading in Java

[00:00] Inside this lecture, let's go back to the basics and try to understand how a software or a program
[00:07] is going to execute behind the scenes inside a computer.
[00:11] So let's try to understand the same.
[00:13] Like you can see here inside a computer at the very low level we'll be having the hardware.
[00:19] So as part of this hardware we'll be having CPU.
[00:23] CPU is responsible to execute instructions or to perform any calculations that a software or a program
[00:30] required.
[00:31] So basically CPU is going to provide computing power to a program or a software to execute a specific
[00:39] set of instructions.
[00:40] Similarly, we'll be having Ram.
[00:42] Ram is going to provide a memory location, which can be used to save some data and retrieve the same
[00:49] whenever required, very fastly.
[00:51] And similarly, we'll be having hard disk, which is capable of storing any amount of data like 1TB
[00:57] or 2TB.
[00:58] We can store any amount of data inside a hard disk, but Ram memory is very limited.
[01:03] It will usually have 16 GB, eight GB or 32 GB Ram.
[01:08] So whatever data that a program or a software needs to access very quickly all such data, it is going
[01:15] to be saved inside Ram.
[01:17] And whenever the program or a software is closed, whatever data that we stored inside the Ram related
[01:24] to that program, our software is going to get deleted.
[01:27] Similarly, hardware also is going to provide other capabilities, like it is also going to have network
[01:34] related drivers, which is going to help in performing input and output operations.
[01:39] Like if you want to watch a movie inside Netflix or inside Hotstar.
[01:45] So in all such scenarios, the video needs to be streamed from the remote server.
[01:50] So based upon the data that is being streamed from the remote server, the same is going to be downloaded
[01:55] by your computer.
[01:56] And whatever video that has been downloaded, you will be able to see inside your browser or inside
[02:02] your media player.
[02:04] After the hardware on top of it, we are going to have operating system.
[02:08] Can we start using a computer without operating system?
[02:12] Off course not.
[02:13] With hardware alone
[02:14] the computer is going to be useless.
[02:17] By installing an operating system on top of the hardware, we will be able to perform lot many actions
[02:24] inside a computer.
[02:25] So what is an operating system?
[02:27] It is a software that manages hardware resources and provides services for other computer programs.
[02:34] So basically operating system, it is going to abstracts the hardware and provides a consistent interface
[02:40] for applications to run on different types of hardware resources.
[02:45] So now think like we have a proper computer with a proper hardware and operating system.
[02:50] As a next step, we will start using this computer.
[02:53] For example, if I want to open a Chrome browser, I will be able to do that
[02:58] and similarly, if I want to open a PDF, I'll be able to do that.
[03:01] Similarly, if I want to read an email, I'll be able to open the outlook with the help of the Outlook
[03:07] Software or Outlook program.
[03:09] I'll be able to read the emails.
[03:11] I'll be able to send the emails.
[03:13] Similarly, we will be able to invoke so many softwares or programs based upon our needs.
[03:19] Like you can see here.
[03:20] On top of my operating system, there are so many processors are running based upon the type of softwares
[03:27] or programs that I'm trying to run.
[03:29] So here you can see, seems one user tried to open all these softwares like a chrome, pdf reader,
[03:36] email, intelliJ, ppt, zoom, Safari, notion, Dropbox.
[03:42] So for each of the software or the program that you're going to invoke inside your computer, a dedicated
[03:49] process is going to be created by operating system.
[03:53] So we can say a process is a program in execution.
[03:57] It is an independent unit that runs in its own memory space.
[04:02] So basically, whenever you are trying to use a software like Chrome, when you open the Chrome browser
[04:07] behind the scenes operating system, it is going to create a process for the Chrome browser alone.
[04:13] So for this process of Chrome browser, the operating system, it is going to allocate some CPU resources,
[04:19] some Ram memory and similarly some disk memory.
[04:23] So whatever hardware resources needed by my process of Chrome.
[04:27] So all those will be assigned by the operating system to the process of Chrome.
[04:32] It is very important to understand that each process has its own address space and system resources.
[04:37] So whatever address, space or resources assigned to the Chrome, it cannot be shared or used by other
[04:44] processes like Intel, Edge or Safari.
[04:47] I hope you are clear about the process.
[04:49] Now let's try to understand what is a thread ? Before I try to explain you about what is a thread from
[04:54] operating system perspective, let me ask you a question.
[04:57] If you open a Chrome browser,
[05:00] are you going to perform
[05:01] only one action
[05:02] always ?
[05:03] Off course not
[05:04] you'll be opening multiple tabs inside your Chrome browser.
[05:07] In one tab, you might have open the Gmail.
[05:10] In another tab, you might have opened the Netflix where a video is being played.
[05:14] In another tab, you might have opened YouTube, where also a video is being played, and inside another
[05:20] tab of your chrome you might have open the WhatsApp where you are trying to chat with your friend.
[05:26] So if you see within a software or within a program or within a process, you're trying to perform multiple
[05:33] tasks.
[05:34] So to handle all these tasks efficiently or parallelly or simultaneously, threats are going to be created
[05:42] within process.
[05:43] So what is a thread ?
[05:44] A thread is a smallest unit of execution within a process.
[05:49] Multiple threats can exist within a single process, handling the various activities of the software
[05:55] or the program that you are trying to run within a process.
[05:59] So all these threats, they are going to be created by the softwares.
[06:03] For example, inside the business logic of Chrome software, someone might have written the code to
[06:10] create a new thread whenever a new tab is being opened by the end user.
[06:14] So these threads at the end of the day, they are going to request the operating system to provide some
[06:20] resources like CPU time or Ram memory.
[06:24] So based upon these requests, operating system can provide the hardware resources.
[06:29] So all the threads that we are going to create within a process, they are going to share the same memory
[06:34] space allowing for the efficient communication.
[06:37] So the main purpose of creating threads is they are very lightweight compared to the process.
[06:43] And they can run concurrently behind the scenes.
[06:46] Let me share more details about threads, how threads are going to be created within the process.
[06:52] Like you can see here, I have a process of chrome.
[06:56] So inside this process of Chrome there will be multiple threads, will be created like T1, T2, T3,
[07:03] T4, t5.
[07:04] So all these threads, they are going to be created based upon the actions performed by the end user
[07:10] on the Chrome browser.
[07:12] So each of the thread is going to give some responsibility to execute a sequence of instructions within
[07:19] a process.
[07:20] So when a thread it wants to execute some instructions, at the end of the day it needs the CPU computing
[07:27] power.
[07:27] So how it is going to get the CPU computing power?
[07:30] The thread will ask the operating system to give some CPU time of a CPU core, and based upon the time
[07:38] provided by the CPU core to a specific thread, it is going to execute all the instructions.
[07:44] You may have a question here, which is what is a CPU core?
[07:47] CPU core is a main hardware component available inside the CPU, which is responsible to execute the
[07:55] instructions
[07:56] that requires computing power. Back in the days of 1990s
[08:00] in those times, computers, they only used to have a single CPU core, but the modern laptops and systems
[08:07] that we are trying to use, they are having four cores, eight cores, 12 cores.
[08:12] Many times you might have heard, like someone claiming that that my computer is a octa core processor
[08:19] or a quad core processor.
[08:20] So what do they mean?
[08:21] That means their computer have four cores or eight cores.
[08:25] So when a thread request operating system for a CPU time, it is going to assign the CPU time for a
[08:32] limited time like fraction of seconds
[08:35] or it can be one second or it can be two seconds five seconds 10s.
[08:38] So based upon the demand from your thread, the CPU time is going to be assigned by the operating system.
[08:44] Like we discussed within a process, we can create multiple threads, enabling concurrent execution
[08:50] of various tasks and enhancing CPU resource utilization and ultimately boosting the throughput.
[08:58] So let's try to understand this statement by taking the example.
[09:01] Think like you launched a Google Chrome.
[09:04] The operating system generates a process for this Chrome.
[09:07] And within that process task like showing a web page, downloading a file, playing a video on YouTube,
[09:13] WhatsApp chatting they can all occur simultaneously due to separate threads.
[09:18] Suppose think like this T4 thread is capable of playing a video on YouTube in one of the Chrome tab,
[09:25] so as soon as the playing of the video is completed, then this T4 is not going to require any CPU time,
[09:33] or it is not going to require any hardware resources.
[09:36] So in all such scenarios, the T4, it is going to sit ideally, and it is not going to ask any time
[09:42] to the operating system for the hardware resources. Maybe after half an hour if the end user came to
[09:47] the same tab and he's trying to play the another video inside the YouTube.
[09:52] Then again, the thread will try to request the operating system for the CPU time or for the any other
[09:58] hardware resources
[09:59] it requires.
[09:59] I can also confirm all this theory by showing an information inside my system.
[10:05] Inside my Mac
[10:06] I opened a program with the name Activity Monitor.
[10:10] If you are using windows operating system, you will be able to see the same kind of information inside
[10:16] your task explorer.
[10:17] So if you see here under this activity monitor, I selected the memory which will give me the summary
[10:24] around which processes are using my Ram memory and how many threads are created for each of the process.
[10:30] You can see inside my system I have processes like IntelliJ Idea, PowerPoint, outlook, subline,
[10:37] OneDrive, Safari.
[10:39] So there are many processes running and each of these processes, they have multiple threads created
[10:46] inside them based upon their own requirements.
[10:49] So this should give a confirmation to you that all these processes, they are relying on threads behind
[10:55] the scenes to execute multiple tasks simultaneously or parallelly.
[11:00] So if you see my IntelliJ Idea, it is using right now 2.53 GB Ram memory.
[11:05] Similarly PowerPoint it is using 442 MB.
[11:08] I can also go to the CPU tab, where we'll be able to see how much CPU time is being used by each of
[11:16] the process.
[11:17] For example, this Microsoft PowerPoint, it has used CPU time of one hour, 48 minutes zero seven seconds
[11:27] with the threads 52.
[11:29] So this way always behind the scenes operating system.
[11:32] It is going to manage the processes and within the processors multiple threads are going to be created.
[11:38] So all these threads, they are going to work with the operating system to get the hardware time like
[11:44] CPU time or Ram memory.
[11:46] So based upon thread requirements, the same is going to be requested to the operating system.
[11:51] And if there is a free availability of the resource, then obviously operating system will be more than
[11:57] happy to provide such hardware resources.
[11:59] But if you are trying to run too many programs or too many softwares inside your system, then obviously
[12:05] sometimes you may feel some slowness inside your system.
[12:08] Why that slowness is happening, because the operating system does not have enough resources to assign
[12:14] to your software.
[12:15] That's why sometimes softwares they'll hang or they will behave very slowly.
[12:20] I hope you're clear how a program or a software executes inside a computer.
[12:24] The same kind of explanation is also applicable for a Java program as well, because at the end of the
[12:30] day, Java program is also a software or it is also a program which needs some hardware resources to
[12:37] execute the instructions that we have mentioned as part of the Java program.
[12:42] I'm assuming you are enjoying this discussion.
[12:44] Let's continue this discussion in the next lecture as well.
[12:47] Thank you,
[12:48] bye.

----------------------------------------
