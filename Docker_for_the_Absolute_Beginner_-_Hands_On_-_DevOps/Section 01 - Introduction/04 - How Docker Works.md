# How Docker Works

*Section: Introduction*

1 To understand how Docker works, let us revisit some basic concepts of operating systems first. 2 If you look at operating systems like Ubuntu, Fedora, OpenSUSE, or AlmaLinux, and the rest, they all 3 consist of two things. 4 An OS kernel and a set of software. 5 The OS kernel is responsible for interacting with the underlying hardware. 6 The kernel remains the same, which is Linux in this case. 7 It's the software above it that makes the operating systems different.

8 This software may consist of a different user interface, drivers, compilers, file managers, 9 developer tools, and so on. 10 You have a common Linux kernel shared across OSes and some custom software that differentiates 11 operating systems from each other. 12 We said earlier that Docker containers share the underlying kernel. 13 What does that mean? Sharing the kernel. 14 Let's say we have a system with an Ubuntu OS with Docker installed on it.

15 Docker can run any flavor of OS on top of it as long as they are all based on the same kernel, in this case Linux. 16 So if the underlying OS is Ubuntu, Docker can run a container based on another distribution like 17 Debian, Fedora, OpenSUSE, or AlmaLinux. 18 Each Docker container only has the additional software that we just talked about that makes these 19 operating systems different. 20 And Docker uses the underlying kernel of the Docker host, which works with all operating systems involved.

21 So what is an OS that does not share the same kernel as these? Windows. 22 So you won't be able to run a Windows-based container on a Docker host with Linux on it. 23 For that, you will need a Docker on a Windows server. 24 Now, it is this when I say that most of my students go, hey, hold on, that's not true. 25 They install Docker on Windows. 26 They run a container based on Linux and go, see, it's possible.

27 Well, when you install Docker on Windows and run a Linux container on Windows, you're not really 28 running a Linux container on Windows. 29 Windows runs a Linux container on a Linux virtual machine under the host. 30 So it's really a Linux container on a Linux virtual machine on a Windows machine. 31 So we'll discuss more about this on the Docker on Windows or Mac lessons later in this course.

32 Now you might ask, isn't that a disadvantage then? 33 Well, not being able to run another kernel on the OS. 34 Well, the answer is no, because unlike hypervisors, Docker is not meant to virtualize and run 35 different operating systems and kernels on the same hardware. 36 The main purpose of Docker is to package and containerize applications and to ship them and to run 37 them anywhere, anytime, as many times as you want.
