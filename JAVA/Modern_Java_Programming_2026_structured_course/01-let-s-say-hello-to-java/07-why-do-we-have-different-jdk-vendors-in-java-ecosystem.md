# 1.7 — Why do we have different JDK vendors in Java ecosystem

> Section 1: Let's Say Hello to Java

[00:00] Now inside this lecture, let's try to understand why we have different JDK vendors available inside
[00:07] the Java ecosystem.
[00:09] So what is JDK?
[00:10] JDK means Java Development Kit.
[00:13] Whenever we want to develop Java based applications, or whenever we want to run Java code inside any
[00:19] production server or inside any local system, we need to make sure we are installing these JDK inside
[00:25] a particular system.
[00:26] But when we try to install the JDK or Java inside any system, we have various options.
[00:32] The very first and the most commonly used approach is with the help of Oracle.
[00:36] We can go to the Oracle website.
[00:38] We can install the Java with the help of instructions provided on the Oracle website.
[00:43] Similarly, we can also set up and install JDK from other vendors as well.
[00:47] So there is a very good history that you need to be aware before you try to install JDK or Java inside
[00:53] your local system.
[00:55] Like I said before, somewhere in 2010 Oracle acquired Sun Microsystems when Sun Microsystems introduced
[01:04] Java in 1995.
[01:06] From day one, Java is free for everyone, which means it is an open source programming language.
[01:12] No one has to pay any money to install and use Java inside their software applications.
[01:19] But when Oracle acquired Java, they tried to commercialize it.
[01:23] That means only people who can pay money to Oracle, they can only use Java.
[01:28] Because Oracle sees an opportunity to generate some revenue with the help of Java.
[01:34] But everyone in the industry, they didn't agree with the Oracle approach on commercializing the Java
[01:41] language.
[01:42] So there is lot of opposition came from the Java community and many bigger organizations.
[01:48] Since there is a conflict on both sides, like from one side Oracle team, they are trying to commercialize
[01:53] Java and the other side Java community and many other famous organizations.
[01:58] They are trying to oppose that decision.
[02:00] So with this conflict in, new developments happen.
[02:04] So let's try to understand what are those.
[02:06] The very first JDK vendor that I want to discuss here is open JDK.
[02:10] Open JDK community is responsible to build a new features of Java programming language.
[02:17] So inside this open JDK there are good amount of open source developers available.
[02:22] So this open source community developers along with the Oracle, they are going to build newer versions
[02:28] of Java regularly every six months.
[02:31] That means this open source community, along with Oracle, they are going to release a new version
[02:36] of Java every six months.
[02:38] But this open JDK community, they are not going to worry about providing various features to the enterprise
[02:46] organizations.
[02:47] They're not going to provide the JDK binaries to install inside a production server, or to install
[02:52] inside a system.
[02:53] They're simply going to build the source code that is required for the newer version of Java.
[03:00] So with that, the job of open JDK is going to be complete.
[03:04] And these open JDK is also responsible to define the specifications on how a Java language should work
[03:12] on how a Java language should execute.
[03:15] So based upon all those specifications and requirements and the suggestions received from the developer
[03:21] community, every six months we are going to get a new Java version.
[03:24] It can be a Non-lts version or an LTS version, but by using these open JDK source code companies are
[03:31] any developer.
[03:31] They cannot install or setup Java inside their local system.
[03:35] So that's where we have Oracle JDK come into picture.
[03:39] So Oracle Team, what they are going to do is with the help of the source code that is developed by
[03:44] the open JDK team, they are going to generate the binaries.
[03:48] Are they going to provide the JDK installations to the organizations and the developers who want to
[03:54] use a particular Java version.
[03:56] And on top of that, Oracle is also going to enhance the open JDK version by doing some optimizations
[04:03] in terms of performance and in terms of stability and security.
[04:07] So since it is going to do a lot of work, Oracle JDK is not going to be free for production usage.
[04:13] As a developer, I can install Oracle JDK inside my local system and I can use it happily.
[04:19] I don't have to pay any money, but if the same Oracle JDK.
[04:23] If an organization want to use inside their production server, they have to pay the money to the Oracle
[04:29] JDK.
[04:29] Because Oracle team, they are putting lot of efforts in building and providing a stable and faster
[04:35] running JDK version of OpenJDK.
[04:38] Here, if you see Oracle came with an approach that developers can use Oracle JDK for free inside their
[04:44] local systems.
[04:45] But in the scenarios where a particular organization trying to develop Java based web application,
[04:51] then in that scenario, the organization is liable to pay some license fee to the Oracle based upon
[04:59] how many developers are using Oracle JDK inside the organization.
[05:03] Since there is a lot of money involved with Oracle JDK approach, there is.
[05:07] Another vendor came into picture which is adopting JDK under the name of adopt.
[05:13] A working group has been formed by many famous organizations.
[05:18] So what they are going to do is they are going to do the same job of Oracle, like with the help of
[05:23] Java source code provided by the open JDK.
[05:26] These adopt JDK people.
[05:28] Also, they are going to generate the binaries and JDK installations for various operating systems.
[05:34] On top of that, they are also going to do some optimizations that are required for the enterprise organizations
[05:40] and apart from these adopt JDK, there are many other JDK providers also available.
[05:46] The other famous JDK vendors are from Amazon.
[05:49] We have Amazon Corretto.
[05:50] We also have Azure Red hat IBM.
[05:53] So there are many JDK vendors came into picture just because Oracle is trying to commercialize Java.
[05:59] But as of today, Java still is open source and we can use at free of cost.
[06:05] So here you may have a question which is if you have so many flavors of JDK, don't you think my Java
[06:12] program is going to behave differently in different different JDK?
[06:16] It's a very valid question, and I want to give an assurance to you, regardless of which JDK you install
[06:23] inside your local system, the Java program is going to run very similarly, and the output you are
[06:29] going to get is going to be same.
[06:31] How it is going to be possible is, like I said before, open JDK is responsible to define specifications
[06:38] for Java programming language.
[06:40] So these specifications we can also call them as TCK.
[06:44] So what is TCK Technology Certification Kit.
[06:47] So any JDK provider who are trying to generate the JDK binaries from the open JDK source code, they
[06:54] need to make sure they're not changing the source code of Java.
[06:57] Instead, they can do some optimizations on how fast a Java program is running.
[07:02] But if I give a Java statement like System.out.println, it has to work very similarly inside all the
[07:08] JDK and the output has to be same.
[07:11] The only thing that can deviate is the amount of time it is taking to execute a particular Java statement.
[07:17] Oracle team.
[07:18] They can do more optimizations on the Java source code, and they can sell their JDK to the enterprise
[07:24] organizations.
[07:24] Claiming that my Java code is going to work very fastly compared to the other JDK provider.
[07:30] So this way there is a competition came into picture.
[07:33] Many organizations, they are trying to sell these JDK by optimizing them to the enterprise organizations.
[07:40] Let me share you more details around these different JDK vendors of Java.
[07:45] This is the website of open JDK.
[07:47] The website is open jdk.org.
[07:50] As I said before, open JDK is a Java community where we are going to have a mix of open source Java
[07:56] developers, Java Champions, and in fact there will be few members from Oracle and other prominent
[08:02] companies.
[08:03] They are also going to play a part inside these open JDK community, while taking decisions on what
[08:10] features needs to be released in the upcoming releases.
[08:13] We can assume these open JDK is a place to collaborate on an open source implementation of the Java
[08:21] platform, standard, Edition and related projects, but you can't download or set up JDK from this
[08:28] website.
[08:29] As I said before, these community they only going to provide the source code of the Java based upon
[08:35] this source code.
[08:36] The other vendors they are going to prepare the binaries are the installations for the Java.
[08:40] I'll show you a few of the other vendors as well in a few seconds.
[08:43] Here there is a option to download, but this will redirect you to the other website after the open
[08:49] JDK.
[08:50] The next important prominent vendor inside Java ecosystem is Oracle.
[08:56] So if you go to the website oracle.com/java here you're going to have an option of downloading the Java.
[09:03] As of today you'll be able to download these versions.
[09:07] But regardless of which version of Java that you see inside this page, don't worry, as long as you
[09:13] learn the concepts of Java Basics of Java, you should be able to easily cope up with the new features
[09:19] of a specific Java version.
[09:21] Always try to use LTS versions in real projects, but if you are exploring Java and if you're trying
[09:28] to learn the new features inside Java, then you're always welcome to install and set up Non-lts Java
[09:34] version.
[09:34] The next vendor that we have is adoption.
[09:38] Adoption is a group which is formed by a group of companies.
[09:41] So if you can scroll on this website, they clearly highlighted they are offering high performance,
[09:46] cross-platform open source Java runtime binaries that are enterprise ready and Java SDK certified.
[09:55] Any enterprise organization are real Java projects.
[09:58] People.
[09:59] They should be able to download these JDK and use it without paying any money here.
[10:05] Also, they clearly highlighted prebuilt open JDK binaries for free.
[10:10] If you click on this About Us and open this our members web page, you will be able to see who are the
[10:17] members of this group.
[10:19] So these are the members and the strategic members.
[10:21] We have famous companies like Microsoft, IBM, Google, Alibaba, Azul.
[10:27] Under the enterprise members, we have Red hat, Bloomberg, and under the participant members we have
[10:33] these two companies.
[10:34] This is also a very good community.
[10:36] You can safely download JDK from this website as well.
[10:40] The next famous vendor that we have is AWS.
[10:43] We know AWS is a cloud company which is owned by Amazon.
[10:47] Amazon also provides JDK binaries and installations with the name Amazon Corretto.
[10:53] I recommend using these Amazon Corretto if your organization is deploying the Java code inside AWS servers
[11:02] or infrastructure.
[11:03] Because these corretto JDK, obviously it is optimized better for the Amazon platform and Amazon infrastructure.
[11:12] So here they clearly highlighted Amazon Corretto is a no cost to multiplatform production ready distribution
[11:18] of open JDK.
[11:19] So Corretto comes with long term support that will include performance enhancements and security fixes.
[11:27] Please read the information on this page for more details.
[11:30] So you have links to download the JDK as well after AWS.
[11:34] The next famous vendor is Azul.
[11:37] Azul is a vendor who focus more on performance inside industry.
[11:42] There are certain enterprise organizations who they require a lot of performance.
[11:47] Inside Java, for example, the organizations who runs the stock market trading platforms are bank platforms.
[11:55] They need high performance because the volume of the transactions that they are going to handle on day
[12:00] to day basis is very high, and even a nanosecond or a millisecond delay, it is going to cause them
[12:07] a lot.
[12:08] So for such clients, agile is a better option or choice because agile focus more on the performance
[12:15] inside this website.
[12:16] If you can scroll down at the center, they have the open JDK.
[12:20] By using this open JDK, they are trying to provide two different products with the name Agile Platform
[12:26] Core.
[12:27] So if some company uses this product, they are claiming they're going to have 70% of savings compared
[12:34] to the Oracle Java.
[12:36] Whereas on the other side we have other products with the name Agile Platform Prime.
[12:41] If someone uses this product, they are going to save 20% in the cloud cost.
[12:46] So apart from the performance improvement the organizations, they should be able to save some money
[12:51] around the cloud cost or around the licensing.
[12:55] This way there are good amount of vendors inside the industry, but I try to show you the important
[12:59] vendors.
[13:00] The reason why I'm emphasizing about all these vendors and the history of Java is inside interviews.
[13:06] You're going to have good amount of questions around this concept.
[13:10] You can expect questions like what is an LTS and Non-lts version?
[13:14] Why do we have various vendors?
[13:16] What's the difference between OpenJDK and Oracle JDK?
[13:21] So these kind of questions you can expect inside the interviews with the discussion that we have done
[13:26] so far, I'm assuming you have better knowledge to answer all those questions in the next lecture.
[13:31] Let's try to download Java and set up inside our local system.

----------------------------------------
