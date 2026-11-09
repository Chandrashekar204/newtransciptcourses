# Containers vs VMs

*Section: Introduction*

1 Now, let us look at the difference between virtual machines and containers, 2 something that we tend to do, 3 especially those from a virtualization background. 4 In the case of Docker, 5 we have the underlying hardware infrastructure, 6 and then the OS, 7 and then the Docker software itself installed on the OS. 8 Docker then manages the containers that 9 run with libraries and dependencies alone.

10 In the case of virtual machines, 11 we have the hypervisor like the ESX on the hardware, 12 and then the virtual machines on them, 13 and each virtual machine has its own OS inside it, 14 and then the dependencies, and then the application. 15 The overhead causes higher utilization of 16 underlying resources as there are 17 multiple virtual operating systems and kernels running. 18 Virtual machines also consume higher disk space as 19 each VM is heavy and is usually in gigabytes in size, 20 whereas Docker containers are lightweight 21 and are usually in megabytes in size.

22 This lets Docker containers boot up faster, 23 usually in a matter of seconds, 24 whereas VMs, as we know, 25 take minutes to boot up because they need 26 to boot up the entire operating system. 27 It is also important to note that Docker has 28 less isolation as more resources are 29 shared between the containers like the kernel, 30 whereas VMs have complete isolation from each other. 31 Now, since VMs don't rely on the underlying OS or kernel, 32 you can run different types of applications built on 33 different OSs such as Linux-based or 34 Windows-based apps on the same hypervisor.

35 Now, those are some of the differences between the two. 36 Now, having said that, it's not an either 37 container or virtual machine situation. 38 It's containers and virtual machines. 39 When you have large environments with thousands of 40 applications, containers running on thousands of Docker hosts, 41 you will often see containers provision on virtual Docker hosts. 42 That way, we can use the advantages of both technologies.

43 We get the benefits of virtualization to easily 44 provision or decommission Docker hosts as required, 45 and at the same time, 46 you make use of the benefits of 47 Docker to easily provision 48 applications and quickly scale them as required. 49 Remember that in this case, 50 we will not be provisioning that many virtual machines 51 as we might have before because earlier, 52 we provisioned a virtual machine for each application.

53 Now, you might provision a virtual machine 54 for hundreds or thousands of containers.
