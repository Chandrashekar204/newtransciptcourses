# 23.1 — Java Networking Fundamentals: Internet, Networks, and Core Java API Overview

> Section 23: Mastering Java Network Programming: Sockets, NIO, and Modern Frameworks

Kind: captions Language: en Welcome to the first lecture on networking in Java. In this series of videos you'll be learning about the basics of networking. You're probably watching this video on the internet. Wikipedia describes the internet as a global system of interconnected computer networks. It's a network of networks, consisting of private, public, academic, business, and government networks, some of which are local and some that are global.

The Internet provides a vast range of information resources and services. In addition to web browsing, social media, email, gaming, and countless other applications rely on networking. Java has had support for networking since its first version. Like many of the other topics in this course the Java language continues to change to keep up with the latest technologies and programming paradigms. In this section I'll start out with the original java dot net package and what types it provides.

This includes types for low level programming which work with sockets and addresses. It also includes higher level types that hide or manage connection level details. I'll also be using this section to introduce you to some exciting new changes. My file IO section of the course mentioned channels but grew a bit long to do much else so I'll include a formal introduction of channels here. Channels offer a much more robust way of communicating between interconnected devices, and there are several channels we can use for network communications.

In addition JDK 11 also saw the inclusion of the java.net.http package. This includes support for html 2.0 as well as builder patterns to create instances of types specifically used for internet communication. In addition this package also gives us the Web Socket type. Unlike HTTP clients Web Sockets establish persistent connections between the browser and server enabling bi directional communication. I'll be covering this type and why it's significant but before we jump into code I'll start with a review of networking terminology.

So let's do that in the next video.

----------------------------------------
