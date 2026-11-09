# 26.18 — Demo of Streams groupingBy() and partitioningBy() method

> Section 26: [JAVA 8] Streams API

[00:00] Inside this lecture, let's try to understand the other type of methods that we can use whenever we
[00:07] are trying to leverage collect() terminal operation.
[00:10] The very first method that I want to explain here is, groupingBy() method.
[00:14] Whenever you have a requirement where you want to group your elements based upon some criteria, in
[00:21] all such scenarios you can use the groupingBy() method.
[00:25] So this grouping by method is also available inside the collectors.
[00:29] So you're going to use this groupingBy() method whenever you want to collect your elements from a stream
[00:35] based upon some grouping criteria.
[00:38] So when the elements are grouped based upon some criteria, then obviously the output result has to
[00:44] be stored in a Map instance. Like you can see here
[00:47] first I have a product list.
[00:49] Later on using this product list object, I'm trying to invoke the stream() method.
[00:54] After the stream() method, I'm trying to invoke that terminal operation which is collect(), and to this
[00:59] collect(), I'm trying to pass the input which is Collectors.groupingBy() and to these groupingBy()
[01:04] method.
[01:04] I need to tell how the grouping has to be done.
[01:07] The same I'm trying to convey with the help of this method reference, where I want to group the products
[01:12] based upon their price.
[01:14] When this group is going to happen based upon the price, then obviously the key inside my Map it has
[01:20] to be integer, whereas a value can be list of product because there can be multiple products with the
[01:26] same price.
[01:27] So using these grouping by is very simple.
[01:30] If you are familiar with the SQL queries inside the SQL queries
[01:34] also, there is a class with the name group by.
[01:36] If you want to group your records based upon certain criteria inside SQL, we are going to use this
[01:41] group by.
[01:42] So this groupingBy() method is also going to work very similarly.
[01:46] The next method that we are going to explore is partitionBy().
[01:50] Sometimes we want to partition the stream of object elements based upon a given Predicate.
[01:57] For example, if I have 1000 different employee objects, I want to partition them into two groups based
[02:03] upon a criteria like if a given employee is a permanent employee or not.
[02:07] With that, all my employee objects are going to be partitioned into two groups, one representing the
[02:12] permanent employees and the other one representing the contract employees.
[02:16] So in all such requirements, where you want to collect your elements after performing some partition,
[02:22] then you can use these partitionBy() method.
[02:24] So this method also you can use along with the collect() terminal operation. Like you can see here to this
[02:30] collect() method I'm trying to pass the input which is Collectors.partitionBy().
[02:35] And I'm trying to pass a lambda expression on how to partition my products.
[02:40] So basically what I'm trying to do here is, I'm telling to my partitionBy() method, please partition
[02:46] my products based upon the predicate that I'm trying to pass.
[02:49] So here the predicate that I'm trying to pass is if the product price is greater than $1,000, then
[02:55] considered that under the partition
[02:57] true.
[02:57] Whereas all the elements which have the price less than or equal to $1,000, all such elements are going
[03:04] to be considered under the false partition, because for a predicate, the output at max can be true
[03:10] and false.
[03:10] That's why whenever you use this partition by, you're always going to get a HashMap with a boolean
[03:16] as key.
[03:17] And this HashMap it is going to have at max two elements, one with the true and the other one is with
[03:23] the false.
[03:24] So against your key you're going to store that list of products the same we are trying to catch with
[03:29] the help of Map here.
[03:30] Let's see the demo of these two methods very quickly inside IntelliJ.
[03:35] Here, let me create a new class with the name StreamGroupingByDemo.
[03:42] Inside this class,
[03:43] first I'm going to create the main() method, followed by
[03:46] I want to create a List object that is holding various product elements.
[03:50] We already have such code here, so let me copy this entire code and paste it here for that.
[03:56] What I'm going to do is, I'm going to get a Stream object with the help of productList by invoking the
[04:03] stream() method, followed by I'm going to invoke the collect() method, to this collect() method
[04:08] I'm going to pass the input with the help of Collectors.groupingBy().
[04:13] So whenever we are invoking these groupingBy() method, we need to tell how to group the products or
[04:19] how to group the elements when the collection is going to happen.
[04:23] So here, since I want to group the elements based upon the price of the product, I'm going to mention
[04:29] the same with the help of Product::getPrice().
[04:31] .
[04:32] Now on the left hand side, I'm going to catch the output with the help of Map of
[04:38] the key is going to be of type integer comma list of products.
[04:44] So inside list angle brackets I'm going to mention product followed by is equal to.
[04:50] With this I'm assuming we are done creating these logic, but here I'm getting a compilation error because
[04:57] I have not given any name to my Map.
[04:59] So let me
[05:00] Give the Map name as groupingByPriceMap.
[05:05] So these are variable name.
[05:06] So if I try to print out the same map onto the console, you will be able to see all the products.
[05:13] They'll be grouped based upon the price of the product.
[05:15] So if I execute this you can see under 800.
[05:19] I have various products, but we're not able to see the product details.
[05:23] Maybe what we can do is, we can go to the product class and try to implement the toString() method.
[05:30] So to implement the toString() method, I'm going to select toString() here and select both of the fields
[05:36] and click okay.
[05:37] Now if I try to execute this class this time I should get some decent output.
[05:43] So under 800 we have Mi, under 1200 we have Apple, under 600 we have Nokia, under 1000
[05:51] we have multiple products like Samsung, BlackBerry.
[05:55] And similarly we also have one place under $1,000.
[05:58] But coming to the $1,500, we have the costliest product, which is Apple Pro Max.
[06:05] I hope you are clear how the grouping by is going to work very similarly.
[06:08] Let's see the demo off partitionBy() the same
[06:11] I'm going to copy this class and rename this to StreamPartitioning.
[06:17] So I'll just mention partitioning as the name here.
[06:22] So the class name became StreamPartitioningByDemo.
[06:25] So inside this instead of invoking the groupBy I'm going to invoke the partitioningBy and to this
[06:32] partitioningBy
[06:33] we need to pass a lambda expression by adhering to the Predicate functional interface.
[06:38] So first I'll take the input parameter with the name product, followed by I'm going to write a condition
[06:45] which is if product get to price is greater than $1,000, then consider it as a true.
[06:53] Otherwise consider it as false.
[06:54] So I'm getting a compilation error because here we need to mention the key as boolean.
[07:00] With that you can see the compilation error is resolved.
[07:02] I'll rename this name also to PartitioningByPriceMap.
[07:07] So let me type partitioningByPriceMap.
[07:10] I'll take the same and and give as an input to this println() method.
[07:14] So if I execute this time you can see under false I have all the product details which has the price
[07:20] less than or equal to 1000.
[07:22] But coming to that true, you will be having products which has greater than 1000 like Apple and Apple
[07:30] Pro Max.
[07:31] So this way you can always try to partitioning your collection elements while you are trying to collect
[07:37] them with the help of collector terminal operation.
[07:40] I hope this makes sense to you.
[07:42] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
