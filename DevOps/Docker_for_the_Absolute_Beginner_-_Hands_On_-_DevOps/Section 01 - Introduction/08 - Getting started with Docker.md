# Getting started with Docker

*Section: Introduction*

1 We will now see how to get started with Docker. 2 Now, the way Docker is packaged 3 today is a little different from the early days. 4 So let's clear that up before we install anything. 5 In the past, Docker came in two editions, 6 the Community Edition and the Enterprise Edition. 7 The Community Edition was the free set of 8 Docker products and the Enterprise Edition was 9 the certified supported container platform that came with 10 enterprise add-ons like image management and image security, 11 and a universal control plane for 12 managing and orchestrating container runtimes.

13 Of course, those came with a price. 14 That split doesn't exist anymore. 15 So back in November 2019, 16 Docker sold the Enterprise Edition to a company called Mirantis, 17 and it's now sold as the Mirantis Container Runtime, 18 that's a separate product from Docker. 19 So when you read older blog posts that mentioned 20 Docker EE or Docker Enterprise Edition, 21 or compare Docker CE versus EE, 22 that's the history.

23 Those terms don't appear on Docker's site anymore. 24 What you will see today is a free open source piece 25 called Docker Engine plus a set of subscription tiers around it. 26 So Docker Engine itself, 27 the CLI you type Docker and the daemon that does the work, 28 Docker D is still free and open source. 29 That's the part you install on a Linux server, 30 and that's what we'll use throughout this course.

31 The subscription side wraps around 32 Docker Desktop and Docker Hub and Docker offers four tiers. 33 You have the personal, pro, team, and business. 34 Personal is free and covers individuals, students, 35 small teams, education, and non-commercial open source. 36 Teams, pro, team, and business are paid. 37 So pro is for individual developers who 38 want more from Docker Desktop and Docker Hub, 39 team for small teams that need collaboration features, 40 and business is for enterprises that need 41 single sign-on, a hardened desktop, 42 and image access management.

43 Worth knowing if you work in a larger company, 44 because Docker Desktop on machines used for 45 commercial work at companies above 46 a certain size needs a paid subscription. 47 So for this course, 48 the free path covers everything we need. 49 The free Docker Engine is available on Linux, Mac, 50 Windows, and on Cloud platforms like AWS or Azure. 51 In the upcoming demo, 52 we'll take a look at how to install and 53 get started with Docker on a Linux system.

54 Now, if you are on Mac or Windows, 55 you have two options, 56 either install a Linux VM using VirtualBox or 57 some virtualization platform and then 58 follow along with the upcoming demo, 59 which is really the easiest way to get started with Docker. 60 The second option is to install 61 Docker Desktop for Mac or Docker Desktop for Windows, 62 which are native applications. 63 So if that is really what you want, 64 then check out the Docker for Mac and 65 the Docker for Windows sections 66 towards the end of this course to get 67 yourself set up and then head back here.

68 So let's now head over to the demo where we'll 69 take a look at how to install Docker on a Linux machine.
