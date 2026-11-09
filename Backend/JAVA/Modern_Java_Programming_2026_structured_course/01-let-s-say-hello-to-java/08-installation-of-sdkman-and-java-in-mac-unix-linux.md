# 1.8 — Installation of SDKMAN & Java in mac, Unix, Linux

> Section 1: Let's Say Hello to Java

[00:00] Now is the exciting time to install Java or JDK inside our local system.
[00:05] As we discussed previously, we have various options to install and setup Java, but I will go with
[00:11] Amazon Corretto and I would recommend you also installing the same.
[00:15] The reason is whatever JDK provided by these Amazon corridor.
[00:19] It's very easy to install and it is open source.
[00:22] We don't have to pay any money, and it is being used by thousands of real enterprise organizations
[00:28] because at the end of the day, all bigger organizations, they are using AWS cloud to deploy their
[00:34] code behind the scenes.
[00:35] They will end up using these Amazon Corretto provided JDK.
[00:39] If you come to this website, AWS, Amazon.com, you have an option to download various versions of
[00:46] JDK.
[00:47] Here we have links to download JDK 25, 21, 17, 11 and eight.
[00:52] Why?
[00:52] We are seeing only these versions, but not the other versions, because these are the LTS versions,
[00:58] and Amazon also recommends you to install and setup LTS versions.
[01:03] As of today, Java 25 is the most recent LTS version the same?
[01:07] I'm going to install by the time you're seeing this video.
[01:10] If you are seeing another latest LTS version, feel free to install the same here.
[01:15] As soon as I click on this download Krita 25 I will be landed onto this web page.
[01:21] In this page we have options to download the JDK based upon our operating system.
[01:26] So for Linux these are the links.
[01:28] Similarly for windows these are the links.
[01:31] Whereas for the Mac these are the links.
[01:33] Inside this lecture I'm going to explain you on how to set up these Amazon Corretto provided JDK in
[01:39] Mac OS.
[01:40] The same steps you can follow for Linux and Unix as well for windows installation.
[01:45] I'm going to explain the same in the next lecture, even though if you are using windows, don't try
[01:50] to skip this lecture.
[01:51] I recommend you watching this entire lecture, because I'm going to show you a few of the best practices
[01:57] and the tips that you can follow while installing and setting up the JDK.
[02:02] So here I have an option to download JDK.
[02:05] I can either download using the package format or compressed tar format, so it's up to me which format
[02:12] I want to download.
[02:13] Similarly for Linux and Windows.
[02:15] Also we have links, but I'm not going to set up the JDK by manually downloading them and installing
[02:21] them instead.
[02:22] There is a better and alternative way that everyone inside the industry uses.
[02:27] So that approach is by using SDK.
[02:30] By using SDK man, we should be able to install JDK by simply running some commands.
[02:36] We don't have to manually download them, install them, and more importantly, we don't have to set
[02:40] up the Javahome environment variable inside our local system.
[02:45] Usually, once the JDK is installed, we need to set up an Javahome environment variable because by
[02:51] setting up this environment variable, we should be able to run that Java code from anywhere inside
[02:57] our system.
[02:57] Otherwise, we need to go to the exact location where we install the JDK, and from that location only
[03:03] we should be able to run the Java programs.
[03:06] So since it is an inconvenience to the developers, and since usually developers tries to run the Java
[03:11] code from wherever they want inside the system, it is always recommended to set up the Javahome environment
[03:18] variable inside our systems.
[03:20] But when we use this SDK man, everything is going to be taken care by this.
[03:23] Behind the scenes.
[03:24] It is going to install the JDK.
[03:25] It is going to set up the required environment variables.
[03:28] The website is SDK man.io here if you can go to the docs.
[03:33] So first we need to install these SDK man for the Mac OS, I need to follow these instructions.
[03:39] Whereas for the windows we have these instructions which I'm going to explain in the next lecture.
[03:45] For now let me focus on Mac installation.
[03:48] Like I said, please don't go away.
[03:50] I'm going to share some important information around the SDK man, which I'm not going to discuss again
[03:56] in the windows installation.
[03:57] So this is going to be super quick by using these two commands.
[04:00] First I need to install the SDK man inside my system.
[04:03] The first command is this one.
[04:05] Let me copy this.
[04:06] And from my terminal I'm trying to execute this command.
[04:09] Since I already install SDK.
[04:11] Man, I'm getting these confirmation message in your case, since you are installing the SDK man for
[04:17] the first time, it is going to take some time to download and set up.
[04:20] Once we are done with the first command, I'm going to run the second command as well.
[04:24] After the second command is executed, we can confirm if the SDK and installation is complete or not
[04:30] by typing SDK space version command.
[04:33] And for this command, if you are getting some output, that gives a confirmation that the SDK man installation
[04:39] is complete.
[04:39] Next, in order to install Java by using SD command, we have to type the command SDK list Java.
[04:47] So please make sure you are giving space between these words.
[04:50] As soon as I press enter, it is going to give me all the vendor options along with the version details.
[04:57] So there is a vendor Corretto which is provided by the Amazon under Corretto.
[05:02] These are all the versions provided, and for each version there will be an identifier.
[05:08] For example, if I'm looking to install the JDK 25 provided by Corretto, I need to copy this identifier.
[05:15] Similarly, you will be able to see many other vendors.
[05:19] So this is the great advantage of SDK.
[05:23] You don't have to visit all different vendors website to install JDK, so all the vendors details are
[05:30] available here.
[05:30] For example, if you are looking to install JDK 25 provided by Oracle, you just have to copy these
[05:37] identifier.
[05:37] So once you selected the required identifier, you need to type Q which is going to exit the SDK list.
[05:46] So please make sure you are typing capital Q.
[05:49] Next I need to type SDK space install space Java and the identifier.
[05:56] The identifier is 25 hyphen Am.
[06:00] So as soon as I press enter the JDK is going to be installed, since inside my system it is already
[06:06] installed.
[06:06] I am getting this message.
[06:08] So once the installation is completed, you can try to restart your terminal and if needed try to restart
[06:15] your system.
[06:16] Also, once the terminal is restarted you can try to execute Java hyphen version.
[06:22] For this command you should get an message something like open JDK version 25.
[06:27] So this should give a confirmation that what version is installed right now inside your system.
[06:32] If you're not able to see this output, please try restarting your system.
[06:36] And if you're still not able to see the expected output, take help from the ChatGPT around the issue
[06:42] that you are facing.
[06:44] Otherwise, if you still need help, you can always post me your question in the Q&amp;A.
[06:48] Do you see how simple it is to install JDK by using SD command?
[06:52] Let me show you more features of SDK man inside this website.
[06:56] If you go to these SDK by using these SDK man, apart from Java, you should be able to install lot
[07:03] many SDKs like for example, if you are looking to install Spring Boot, there is some details around
[07:11] Spring Boot.
[07:11] By following this link you should be able to install Spring Boot.
[07:15] Similarly, if you are looking for Kotlin are spark.
[07:19] Kayla.
[07:19] Most of the SDK are supported by SDK man.
[07:22] If you install this SDK man, you should be able to install any of the languages and frameworks inside
[07:28] your local system.
[07:29] That's why majority of developers inside the industry they use SDK man.
[07:33] So now let's go to these dogs and click on these uses.
[07:38] So I'll show you more power off SDK.
[07:40] As of now we installed that 25 JDK.
[07:43] Let me go to this offline mode and run this command SDK offline enable.
[07:49] So when I execute this command the offline mode will be enabled.
[07:53] Now if I try to execute the command like SDK list Java, it is going to show me what are the list of
[07:59] JDK that are installed inside my system by SDK.
[08:04] So these are all the JDK that I have installed by using SDK.
[08:07] Man 25 hyphen Amazon 23, Amazon 22, Amazon 21, Amazon 17.
[08:13] Graal.
[08:14] So Graalvm is JDK provided by Oracle.
[08:17] And I also have 11 version from Amazon.
[08:20] So these arrow mark indicates what I'm currently right now using in my system.
[08:25] Whereas this asterisk symbol indicates these are the versions that are installed inside my system.
[08:31] If you don't enable these offline mode then the SDK man, it is going to show you all the JDK vendors
[08:37] available in the web in case if you want to.

----------------------------------------
