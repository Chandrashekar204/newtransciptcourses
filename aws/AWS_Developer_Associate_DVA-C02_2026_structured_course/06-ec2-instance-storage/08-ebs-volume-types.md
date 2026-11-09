# 6.8 — EBS Volume Types

> Section 6: EC2 Instance Storage

So now let's talk about EBS volumes, and there are different volume types. They come in six different types today, and we can group them in several categories. The first one is gp2/gp3, which is a general-purpose SSD volume that will balance price and performance for a wide variety of workloads. And this is something we've been using so far in this course. Then we have io1 and io2 Block Express. They're highest-performance SSD volumes that will be used for mission-critical low-latency and high-throughput workloads.

Then we have st1 volumes, and they're low-cost HGD volume designed for frequently accessed, throughput-intensive workloads. We have sc1 volume, which are going to be the lowest-cost HDD volume, and they will be designed for less frequently accessed workloads. Now, how do you define an EBS volume? Well, you can have several factors, for example, size, throughputs, and IOPS, which means IO operations per second. And obviously when in doubt, always consult the documentation.

Now, for your EC2 instances, only gp2 and gp3 and io1 and io2 can be used as boot volumes. That means where the root OS is going to be running. So let's do a deeper dive into the different EBS volume types. The first one is the general-purpose or GP SSD. So we have the cost-effective storage and low latency. They can be used as system boots volumes, virtual desktops, development and test environments, medium-sized databases, and transactional workloads.

We have the gp3 type of volume, which gives you a baseline of 3,000 IOPS and a throughput of 125 megabytes per second. And you can increase the IOPS up to 80,000 and the throughput up to 2,000 megabytes per second independently. The gp2 volume will give you small gp2 volumes that can burst up to 3,000 IOPS, and there is the size and the IOPS capacity that are linked. So as you increase the size of your gp2 volume, the IOPS will increase, and the max IOPS you can ever get is 16,000.

So in gp3, you can set them independently. In gp2, they are linked together. You get three IOPS per gigabytes. That means that at 5,300-something gigabytes, we are at the max IOPS. Next, we get the provision IOPS SSD. So this is when you have a critical business application with sustained IOPS performance or applications that will need more than 80,000 IOPS. This is great for very good database workloads that will be sensitive to storage performance and constancy.

So we have the io1 volume where you get a max IOPS of 64,000. PIOPS is provision IOPS. 64,000 for natural EC2 instances and 32,000 for others. And you can increase the IOPS independently from the storage size with a ratio of about 50 to 1. And the io2 Block Express volumes give you sub-millisecond latency, give you a much greater IOPS max capacity, so 206,000 IOPS with a ratio of 1000 IOPS per gigabyte maximum. Also, they support EBS multi-attach feature.

So now let's quickly touch upon st1 and sc1. So they cannot be a boot volume. This only be for the previous types of volumes. You can get the size up to 16 terabytes. And we get two kinds of volumes here. We have the throughput-optimized HDD, so st1, which is great for big data, data warehousing, and log processing, which gives you a max output of 500 megabytes per second and a max IOPS of 500. And then for cold HDD, so sc1, this is for archive data, so data that is infrequently accessed.

And this is when you would use it, when you need to have the lowest possible cost. Here, the max throughput is 250 megabytes per second and the max IOPS is 250 as well. Now, you don't have to remember all these details going into the exam. You just need to understand the differences at a high level of all these volumes. So the general-purpose SSD versus the provision IOPS SSD in case you need a database versus some st1 and sc1 in case you need to have high throughput and lowest cost.

And so you can find a summary of all I said in this link right here, okay, which is a screenshot I just took you. So don't need to remember the details again, but remember that if you want to get also over 32,000 IOPS, you need EC2 Nitro with io1 or io2. And that will be it for this lecture. So I hope you liked it, and I will see you in the next lecture.

----------------------------------------
