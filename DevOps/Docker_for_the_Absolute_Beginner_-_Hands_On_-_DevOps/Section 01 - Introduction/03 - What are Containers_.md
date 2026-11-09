# What are Containers?

*Section: Introduction*

1 So what are containers? Containers are completely isolated environments. 2 They can have their own processes or services, their own network interfaces, 3 their own mounts, just like virtual machines, except they all share the same OS kernel. 4 We will look at what that means in a bit, but it's also important to note 5 that containers are not new with Docker. 6 Containers have existed for about 10 years now, 7 and some of the different types of containers are LXC, LXD, LXCFS, and so on.

8 Now, here's the thing that's actually changed since the early days. 9 Docker started out using LXC under the hood, 10 but Docker moved away from LXC back in version 0.9.0, and that was around 2014, 11 and switched to its own library called libcontainer. 12 libcontainer later became runc, which is the reference implementation 13 of the OCI runtime specification. 14 So OCI stands for Open Container Initiative, 15 and it's the open standard that defines how container runtimes 16 and image formats should work.

17 So today, when Docker runs a container, it's actually going through containerd 18 and runc, not LXC, LXD, or LXCFS, 19 which are still around as separate Linux container technologies, 20 but Docker itself doesn't use them anymore. 21 Now, setting up these low-level container environments is hard, 22 and that is where Docker offers a high-level tool 23 with several powerful functionalities, making it really easy for end users like us.

24 And this is how Docker became so popular.
