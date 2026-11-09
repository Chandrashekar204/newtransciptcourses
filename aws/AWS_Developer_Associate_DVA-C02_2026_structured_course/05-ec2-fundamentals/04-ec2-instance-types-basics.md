# 5.4 — EC2 Instance Types Basics

> Section 5: EC2 Fundamentals

So now, let's talk about the different EC2 instance types. So you have a lot of them, and if you click on this link, you will have great details about them. But they can be combined into these categories, general purpose, compute-optimized, memory-optimized, storage-optimized, accelerated computing, and HPC-optimized. And there is a naming convention in AWS. So for example, M5.2xlarge, m corresponds to the instance class. Five is the generation because over time, AWS is going to improve and release new instance types.

And 2x large is the size within the instance class. You don't need to know them, but if you're curious about them, go to this link and you'll get a lot more information. Well, we'll talk about a few different type of instance types. So you have general purpose, and these are great for diversity of workloads such as web servers or code repositories. They will have a good balance between compute, memory, networking. And so in this course, we'll be using general purpose instances.

We'll be using the t2.micro, which is the three-tier general purpose type of instance. On the website that I just showed you, you will see all the different types of instance that are general purpose. And this is gonna evolve over time, so I won't update this slide, but you can always refer back to the AWS website to check what the instances are in the general purpose type of family. Then we have compute-optimized. And these are instances that are great and optimized for compute intensive tasks.

So what requires a high-level of processor? Well, for example, it could be if you're batch processing some data, if you're doing media transcoding, if you need high-performance web servers, if you're doing high-performance computing, it's called HPC. If you're doing machine learning or if you have a dedicated gaming server. So all these things are tasks that require a very good CPU, a very good compute side. And so EC2 instances do have this kind of particularity.

And for now, all the compute-optimized instances in EC2 are of the C name, so C5, C6, and so on. Next, we have some EC2 instances that are memory-optimized, and they are going to have a really fast performance for the type of workloads that will process large data sets in memory. So memory means RAM. And so the use cases are this is going to be high-performance for relational or non-relational databases that are mostly going to be in memory databases.

Distributed web scale cache stores. So for elastic cache, for example, in-memory databases that are optimized for business intelligence or BI, and applications performing real-time processing of big unstructured data. So in terms of the names for the memory-optimized instances, there's going to be the R series because R stands for RAM, but there's also going to be X1, high memory and Z1. Again, you don't need to remember the name of the instances, but good to know at a high-level.

Okay. And finally, we'll have storage-optimized instances. They're great when you are accessing a lot of data sets on the local storage. And so the use cases for storage optimized instances are going to be high-frequency online transaction processing, so OLTP systems, relational and NoSQL databases. And we'll see those in details when we get to the database sections. Cache for in-memory databases, for example, Redis, data warehousing application, distributed file systems, and the storage-optimized instances in AWS will start with an I, a D or H1, okay?

But again, don't have to remember this. I'm just giving you examples. So what does it mean? Let's compare a few instance types. So for example, for t2.micro, we have one vCPU and one memory, one gigabytes of memory. And if you look, for example, at the r5.16Xlarge, we have 16 VCPU and 512 gigabytes of memory. So we can see there's a lot of more emphasis on the memory. If we compare it, for example, to a c5d.4xlarge, we can see we have 16 vCPU and 32 gigabytes of memory.

So less memory, more CPU, and so on different network performance, different EBS bandwidth and so on. So just to give you a point of comparison, and if you wanted a website to compare all the EC2 instances together, there's one that I really like. It's called EC2Instances.info, and I'll show it to you right now. So I am on the EC2Instances.info website. And as we can see, we have a list of all the instances available in AWS. So really a lot. We also get some information around the Linux on-demand cost, the Linux-reserves cost and so on.

So some cost information. We get information around the memory, the number of vCPU. We can order by name, we can search it. So it's quite handy and I really like this website. And if you go and use AWS, you probably will use this website as well. So that's it for this lecture. I hope you liked it and I will see you in the next lecture.

----------------------------------------
