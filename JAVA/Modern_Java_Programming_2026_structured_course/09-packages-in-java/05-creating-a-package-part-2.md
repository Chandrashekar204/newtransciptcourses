# 9.5 — Creating a package - Part 2

> Section 9: packages in Java

[00:00] Since we are into the new section, I have created a project with the name section9.
[00:06] Inside this project only, we are going to make all the changes related to the packages.
[00:11] So for any issues or for any questions about the code that we are going to discuss inside this section,
[00:16] please refer to this project inside the GitHub repo.
[00:20] As of now, you can see it is an empty Java project because under the source folder we don't have any
[00:27] Java classes in all the previous sections we used to directly right click on these and go to the new
[00:33] and we used to select the Java class option.
[00:36] But from now onwards we are going to follow the production standards, which is first we are going to
[00:42] create a package.
[00:43] And inside the package we are going to create the Java classes.
[00:47] So here inside this menu instead of Java class, please select the package option post that you should
[00:53] be able to provide the name to your package.
[00:56] Here I'm going to mention com.eazybytes.model.
[01:02] Inside this package only, I'm going to create all the Pojo classes or all the entity classes using
[01:08] which I can transfer the data from UI to backend and from backend to UI.
[01:14] So let me create this package by pressing enter.
[01:16] As soon as I press enter, you can see I have a package with the name com.eazybytes.com.
[01:23] If you go and check your Java project inside your folder, you're going to have this package name in
[01:30] the form of folders only.
[01:31] Let me right click on this and select the option which is open in finder.
[01:37] So for mac it will be Finder.
[01:39] For windows users it will be Folder Explorer.
[01:43] So based upon your operating system you can select the corresponding option.
[01:47] So here as soon as I click Finder I'll be taken to the folder location where I'm mentioning this project.
[01:53] So here you can see I have a project with the name section9.
[01:56] And inside this we have an src folder.
[01:59] And inside the src folder we have a folder with the name com
[02:04] and inside that we have another folder with the name eazybytes.
[02:07] And inside the eazybytes folder we have another folder which is model.
[02:11] This way the package is going to be maintained as a folder sub folder.
[02:16] So the more number of words that you are going to mention after the dot, the more nested folders or
[02:22] the sub folders are going to be created behind the scenes.
[02:26] So as of now we have mentioned only three words like com.eazybytes.model.
[02:31] That's why we have three different folders which are maintained in the nested format based upon the
[02:37] package name that we have provided.
[02:39] So now I have the package name ready.
[02:41] As the next step, I'm going to create a Java class inside this package so you can right click on this
[02:48] package.
[02:48] Select the new Java class option.
[02:50] So the class name that I'm going to give here is Employee.
[02:54] So as soon as I press enter you can see the package statement automatically populated.
[03:00] Because I'm trying to create the Java class inside this package only
[03:04] that's why these statements are automatically populated by the IntelliJ Idea.
[03:09] For some reason, if this statement is not available, then you're going to get an compilation error
[03:15] which is missing package statement.
[03:18] Like we are trying to create a Java class inside this package, but we don't have any package declaration.
[03:25] That's why we are getting these missing package statement compilation error.
[03:29] To resolve this we need to mention package space and what is the package name?
[03:34] And at last we need to mention the semicolon.
[03:36] We need to mention the exact same package name.
[03:39] For example, instead of model, if I mention something different name like Service, I'm going to get
[03:45] again a compilation error because I have mentioned the package name as com.eazybytes.service.
[03:51] But right now my class is present inside the package which is com.eazybytes.model.
[03:57] So to resolve this issue we need to make sure the package name always matching with the folder of the
[04:03] package where it is present.
[04:04] I hope you are clear with the steps.
[04:06] My humble request is please create multiple packages like maybe you can create a service package and
[04:13] a utility package with the name like com.eazybytes.service and com.eazybytes.utility.
[04:20] So once you have created these packages you can try to create classes like EmployeeService and EmployeeUtility
[04:25] under the corresponding package.
[04:28] So that will give some practice to you around the packages.
[04:32] I hope it is all clear to you.
[04:33] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
