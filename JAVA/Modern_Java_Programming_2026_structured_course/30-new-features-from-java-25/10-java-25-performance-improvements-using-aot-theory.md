# 30.10 — [JAVA 25] Performance improvements using AOT - Theory

> Section 30: New features from Java 25

[00:00] Java team introduced some performance improvements by using aortic concept as part of Java 24 and 25
[00:09] release.
[00:10] Before I try to explain about these new features, first let me explain you on what is this Aot and
[00:18] how it is going to work.
[00:19] Aot means ahead of time.
[00:21] First, let's try to understand what is traditionally is going to happen when we start a Java application.
[00:28] When I say Java application, it can be a Java class or it can be a spring boot application, or it
[00:33] can be Java based application.
[00:35] For example, here I'm trying to run a Java class by using the Java My app command.
[00:40] Usually this command we can execute after we are done with the compilation by using the Java Sea command.
[00:47] When we are running this command behind the scenes, the JVM is going to start and it is going to read
[00:53] the Java files from the jar files.
[00:56] Because even though you are executing a simple Java class behind the scenes, the Java library.
[01:02] It is going to have a good amount of jar files, so all of them will be loaded from the disk.
[01:08] And in case if you're trying to run spring boot based applications or any other framework based applications
[01:15] in those scenarios, also all the Java related Jar files and framework related Jar files, they will
[01:21] be loaded from the disk.
[01:22] So once the Jar files are loaded from the disk, these jar files, they are going to have thousands
[01:28] of Java classes.
[01:30] All these Java classes will be parsed by the JVM one by one.
[01:35] Once the Java classes are parsed as part of the next step, all these classes will be loaded into the
[01:41] memory of your system or the server.
[01:43] So as part of this step, what is going to happen?
[01:45] All the Java class, they are going to be present inside the bytecode.
[01:48] All this bytecode will be converted into machine code.
[01:52] So this machine code will be dependent on the operating system.
[01:56] If you are using windows the corresponding conversion will happen.
[02:00] Otherwise if it is Mac.
[02:01] Accordingly, the conversion from bytecode to machine code will happen once all the classes are loaded
[02:08] into the memory.
[02:09] The links between the classes.
[02:11] Like we know, inside Java a class can be dependent on another class, so those links will be resolved
[02:18] along with the references.
[02:19] Followed by the JVM is going to run static initializers and towards the end the application is going
[02:25] to start.
[02:26] So this is going to happen every time you try to start your Java class or you try to start your Java
[02:32] application, but with the help of ahead of time approach, what is going to happen is we're going to
[02:38] do the task, like reading jar files from disk and parsing class files and loading class into memory
[02:43] and link classes together.
[02:45] So the step 234, five will only happen once, and it can be reused many times.
[02:52] To get the benefits of this Aot approach.
[02:55] First we need to run that training step.
[02:59] As part of this training step, we are going to run the application once and record what is going to
[03:04] happen as part of this.
[03:05] Step 2345.
[03:08] So whatever we recorded as part of the step two by using this preload and pre linking logic.
[03:14] So all those data will be saved into a cache file.
[03:18] Once we have this cache file ready.
[03:20] After executing this training run from next time onwards when we are trying to start the application,
[03:27] we can give the instructions to the JVM to use this cache file that was prepared in the training phase.
[03:34] So when the JVM is using this cache file, it is not going to execute these two, three, four, five
[03:40] steps one more time.
[03:41] And with that, what is going to happen?
[03:43] The startup time of the application is going to be improved, which results into much faster startup.
[03:49] And the memory footprint of the application is also going to be increased.
[03:53] For example, with this approach, if a Java web application is starting in 3 seconds or 4 seconds.
[04:00] With this Aot, we should be able to start the application within 1 to 2 seconds.
[04:06] So we're going to reduce the startup time by 40 or 50% based upon the complexity of the application
[04:13] and coming to the memory footprint.
[04:14] Let's imagine with this traditional setup, if your application can process 1000 requests per second
[04:22] with a given server setup and Ram setup, whereas when you adopt these Aot approach the same application
[04:30] with the same server configuration, with the same Ram configurations, it may process more number of
[04:35] requests like 1200 or 1300 requests.
[04:38] So this is how we are going to improve the performance of our Java applications or Java classes without
[04:44] making any code changes.
[04:46] The benefits of this Aot we can get by simply executing some small commands.
[04:51] I'm going to show you that demo in few minutes.
[04:54] I know right now you may be learning Java and you are ready to explore the advanced concepts like Spring
[05:00] Boot.
[05:00] You can't see these benefits to a great extent if you are trying to test these out on a single Java
[05:07] class.
[05:07] You will be able to see the benefits of this Aot.
[05:10] When you try to test on a spring boot application or a web application that is developed using Java.
[05:16] Try to understand what I'm doing, what commands I'm running, what are the benefits that we are getting?
[05:20] Once you started building web applications by using Spring Boot or any other framework.
[05:25] At that point of time, you can leverage these Aot features to improve the startup time of your application
[05:31] along with the performance.
[05:32] As I said, as part of the Java 24, a new feature introduced with the name Aot class loading and Linking.
[05:39] By using this new feature, we should be able to perform the ahead of time class loading and linking
[05:46] of a Java Web application.
[05:48] If you want to get performance benefit by using this feature, you need to execute totally three comments.
[05:54] So the first command is you need to run this training run command.
[05:58] As part of this, you are going to record what is going to happen inside your application.
[06:03] The command is Java hyphen xx colon a what mode is equal to record by using these highlighted command
[06:12] I'm trying to give instructions to the JVM.
[06:14] So what is this?
[06:15] These are VM arguments virtual machine arguments.
[06:20] So since the Java code is going to be executed by JVM and giving instructions to the JVM by passing
[06:26] these VM arguments.
[06:27] So the syntax is hyphen x colon and the instruction is Aot mode as record.
[06:33] So during the record phase, whatever analysis that my JVM is doing, I'm telling to store those Aot
[06:41] configurations into a configuration file with the name app dot aot conf.
[06:46] The configuration name can be anything.
[06:49] So this configuration name we can provide to the VM by providing these VM arguments.
[06:55] Hyphen access.
[06:55] Colon Aot configuration.
[06:58] Once we provided these VM arguments around the Aot training or record phase, we need to provide the
[07:06] Jar details.
[07:07] My application jar is present in the form of app jar inside the classpath location.
[07:14] So hyphen cpp means classpath and inside the jar I have a class with the name column dot example dot
[07:21] app.
[07:21] So this class is going to act as an entry class into your Java application.
[07:26] So once this command is executed, JVM is going to watch on how your app is running.
[07:31] And accordingly it is going to record all the classes that are loaded.
[07:35] And it saves all the configurations into this file.
[07:38] As part of the step two, we need to create the cache.
[07:41] To create the cache, we need to mention the Aot mode as create.
[07:46] Along with that, we need to provide the Aot configuration details where we have saved.
[07:50] So since we have saved under the file app dot aot conf the same we need to mention here.
[07:56] And the third VM argument that we need to provide is Aot cache.
[08:00] With this we are telling to the JVM to store the cache inside a cache name.
[08:05] App dot aot followed by we need to provide the jar name which is app dot jar.
[08:10] So when we run this step two by using this, configurations that are created as part of the step one,
[08:17] a cache will be created for our application.
[08:20] The same cache we can reuse whenever we are trying to rerun our application.
[08:25] So as part of the step three, what is going to happen when we are starting the application?
[08:29] Next time we can provide the cache details to the JVM by using these VM argument Aot cache.
[08:36] And to this we can provide the cache name app dot aot.
[08:40] After providing cache details, we can provide the jar name along with the Cpcp means classpath, followed
[08:45] by what is the entry Java class name?
[08:48] So with this, what is going to happen.
[08:50] The JVM, it is not going to perform the class loading class linking class verification loading into
[08:58] memory.
[08:58] So all those steps will be skipped because all those details that are already available inside this
[09:03] cache.
[09:04] So that's why the classes that are going to load instantly, no parsing, no loading, no linking will
[09:09] be done.
[09:10] And with that, your application performance is going to improve drastically.
[09:15] So this is what is happened as part of Java 24.
[09:18] But from Java 25 this process is further simplified.
[09:22] The developers, instead of running the three commands, they can right now run only two commands.
[09:27] So the step one and step two it is clubbed into a single step, followed by there are no changes inside
[09:34] the step three.
[09:35] Let's try to understand what changes are happened inside Java 25.
[09:39] Inside Java 25, a new feature introduced with the name ahead of time command line ergonomics.
[09:45] So as I said before, the cache creation process can be completed with a single command.
[09:51] So we just have to provide to the JVM by using these VM arguments.
[09:56] Hyphen access.
[09:57] Colon aortic cache output is equal to app, dot Aot and there won't be any change around the jar name
[10:04] or class name details.
[10:05] So with this single command behind the scenes, both the training and the cache creation will be taken
[10:10] care by the JVM.
[10:12] And the last step that you need to execute is to leverage this cache that is created in this step,
[10:17] so that the application will start fastly.
[10:20] So what is a VM argument that we need to pass?
[10:22] We need to pass aortic cache followed by.
[10:24] We need to mention the cache name.
[10:26] I hope you are seeing the difference here.
[10:28] The VM argument name is Aot cache output.
[10:31] We are telling to the VM to output the cache, whereas in the second command we're telling to the JVM
[10:36] to leverage the Aot cache with this name while starting the Java application.
[10:41] So what are the benefits that we got with these Java 25 new feature.
[10:45] It is further simplified only one command instead of two to create the cache.
[10:50] No leftover configuration files.
[10:52] And this is going to be efficient and perfect for automation and to integrate inside CI CD pipelines.
[10:59] So when we are trying to create the cache by using Java 25 approach or by using Java 24 approach, only
[11:08] few things are going to be cache.
[11:10] So here I mentioned what are the details that will be cached?
[11:13] The JDK classes like string, ArrayList, HashMap and application classes like the Java classes that
[11:19] are returned by the developer library classes.
[11:23] For example, the classes that we are going to have inside the framework jars like spring, hibernate,
[11:28] and any other classes that are loaded by built in class loaders.
[11:32] All these class details will be cached coming to the class details that are not going to be cached.
[11:37] So any user defined class loader classes.
[11:41] So inside Java we should be able to load some custom classes by using class dot for name method.
[11:48] So if a developer trying to load some classes using class loader functionality, those classes will
[11:54] not be cached.
[11:55] But in real applications, the number of user defined class loader classes will be very limited.
[12:01] So it is not going to be any problem.
[12:04] Apart from these user defined class loader classes.
[12:07] Any assigned classes are old.
[12:09] Bytecode classes are dynamically created classes at runtime.
[12:15] Those classes details will not be cached by the JVM.
[12:18] So whatever cache being calculated inside this cache, these precomputed values will be saved.
[12:25] So what are those pre-computed values?
[12:27] Parsed bytecode resolved references like links between classes.
[12:32] Established verified bytecode, loaded metadata like class details, method details, field details.
[12:40] All these pre-computed details will be stored inside the cache and that's how the performance is going
[12:47] to be improved in order to get the benefits of this Aot cache.
[12:51] You need to make sure that these parameters are identical while you are trying to create the cache as
[12:57] part of the step one.
[12:58] And while you are trying to leverage the cache as part of the step two, both in step one and step two,
[13:05] you need to make sure you are using the same JDK version, same architecture, same operating system,
[13:13] same classpath, and same module configuration.
[13:17] But these values can be different.
[13:19] For example, you can use different garbage collector, different main class extra classpath, different
[13:26] heap size configurations are any different runtime arguments.
[13:30] As I said before, to see the benefits of these Aot feature, you should be testing these by using Spring
[13:37] boot based web application.
[13:39] Behind the scenes Spring Boot is also going to leverage Java as a language.
[13:43] So to test this feature inside a Spring Boot application, you can follow these three commands.
[13:50] I'm going to show you the demo as well by following these three commands.
[13:53] The first one is you need to package your Spring boot application.
[13:57] When you package your Spring Boot application, your entire application will be stored as a jar like
[14:03] app dot jar.
[14:03] If you are building a spring boot application using Maven, the jar will be stored inside that target
[14:08] folder.
[14:09] So once the packaging is completed, you can start your web application by using the Java command and
[14:15] by passing the jar details along with this hyphen jar.
[14:20] Just before this hyphen jar, you should also give the VM arguments, which is Aot cache output, and
[14:26] you can save this cache details into a cache with the name my app dot aot.
[14:31] This name can be anything.
[14:32] As part of this step, you are starting your application and you are making sure you are preparing the
[14:38] cache so that from the next time onwards, when you want to start the same application with the same
[14:43] code, you can leverage the cache so that your application will perform better and start quickly to
[14:49] deploy, or to start your application with the Aot cache.
[14:52] You need to run this command.
[14:54] The only difference is here we need to provide the Aot cache as a VM argument.
[14:59] Along with that, we need to pass the cache detail.
[15:01] Usually inside enterprise applications.
[15:03] The same application code will be deployed multiple times, especially inside the microservices environment.
[15:11] The number of instances of the microservices will be scaled up and scaled down based upon the demand
[15:18] in those scenarios.
[15:19] You can try to prepare the cache of your application by using the step two, so that from the next time
[15:26] onwards, whenever you are trying to scale the same application, you can use the Aot cash so that the
[15:32] application will start quickly and perform in a better manner.
[15:36] I know this is all theory.
[15:37] Let's try to see a demo of this Aot feature by taking an Springboot application.

----------------------------------------
