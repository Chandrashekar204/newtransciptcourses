# Docker on MAC

*Section: Docker on Mac & Windows*

1 We now look at Docker on Mac. 2 Docker on Mac is similar to Docker on Windows. 3 The way you run Docker on a Mac is with Docker Desktop, 4 a single GUI app you install, 5 and Docker takes care of everything underneath. 6 With Docker Desktop, we rely on Apple's native hypervisor. 7 During installation, Docker Desktop automatically creates 8 a Linux system underneath using Apple's native virtualization, 9 with Docker running on that Linux system.

10 The exact virtualization technology depends on your Mac. 11 On Intel Macs, Docker Desktop historically used HyperKit, 12 an XHive-based lightweight hypervisor. 13 That path is now deprecated, 14 and current builds use Apple's virtualization framework here too. 15 On Apple Silicon Macs, the M1, M2, M3, and M4 chips, 16 Docker Desktop uses the same Apple virtualization framework 17 with an optional faster backend called Docker VMM 18 that's tuned for these chips.

19 Apple Silicon brings native ARM64 support along with it. 20 Most popular images on Docker Hub now publish multi-arc manifests 21 with both AMD64 and ARM64 variants, 22 so most things just work without any extra effort. 23 If you specifically need a 64-bit Intel image on an Apple Silicon Mac, 24 you can force the platform to Linux slash AMD64 25 when you run the container. 26 That now runs through Rosetta 2 translation fast and far better 27 than the QEMU emulation Docker used here in the past.

28 The system requirements have moved on too. 29 Docker Desktop's support policy is the current macOS release 30 plus the two most recent at this writing. 31 That means macOS Tahoe 26, macOS Sequoia 15, and macOS Sonoma 14. 32 Anything older, like Ventura or Monterey, is unsupported. 33 For hardware, you'll want at least 4GB of RAM, 34 though 8GB or more is recommended. 35 One more thing worth knowing.

36 Docker Desktop now requires a paid subscription 37 for commercial use inside organizations 38 with more than 250 employees 39 or more than $10 million in annual revenue. 40 It's free for personal use, students, education, 41 and non-commercial open source. 42 The underlying Docker engine on Linux servers stays free. 43 The licensing only applies to the desktop app on Mac and Windows. 44 Finally, remember that all of this is to be able to run 45 Linux containers on Mac.

46 There are no Mac-based images or containers. 47 Docker on Mac always runs Linux containers 48 just inside a small Linux VM that Docker Desktop manages for you. 49 That's it for Docker on Mac. 50 Next, we'll do the same walkthrough for Docker on Windows.
