# 2.4 — Installing OpenJDK 17 on Ubuntu Linux: A Step-by-Step Terminal Guide

> Section 2: Java Development Environment Setup

Kind: captions Language: en In this video, we're going to install the Open JDK version 17, on Ubuntu 22.04. If you are on Windows or macOS, then check out the relevant videos for your operating system. So we want to start by opening up applications, by clicking here, and selecting Terminal, note that my screen may look slightly different to yours. Just click Activity in the top left of the screen. Click in the search box, and type Terminal, and press ENTER.

This opens up a new terminal window. Firstly, we want to check if Java is already installed on your computer. Type java -version If you get a message similar to this, it means Java is not installed. You may get a message with an older version of Java, you have previously installed. In both cases, continue on and type the following sudo apt update ENTER You may, or may not be prompted to enter a password here. If you are prompted, enter your password to continue.

Give that a moment to complete. Next we want to download and install the JDK. Type the following in the Terminal window sudo apt install -y openjdk-17-jdk This will take a while to download and install. I'll fast forward and come back once its done. Ok thats completed. Type java -version And as you can see, its showing Java 17.0.4 which is correct. Type exit, to exit the terminal. The JDK installation is complete. Next we want to go to the next video and install IntelliJ. See you in the next video.

----------------------------------------
