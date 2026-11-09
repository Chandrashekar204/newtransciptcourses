# 15.7 — Override hashCode() & equals() methods

> Section 15: Unmasking Java's Superclass(java.lang.Object) Secrets

[00:00] Let's try to overwrite the hashCode() and equals() method based upon our custom requirements.
[00:06] First, I'll try to overwrite the hashCode() method because it is very easy for the same
[00:11] I'm going to the Person class.
[00:13] Inside this Person class, we can overwrite the hashCode() method at the end.
[00:19] So first I can write @Override annotation.
[00:22] Below this I'm going to type public int followed by hashCode().
[00:28] And inside this hashCode() method I'm going to write some logic.
[00:31] We know that default behavior of hash code is to calculate the hash code value based upon the memory
[00:37] location.
[00:38] But right now we don't want the hash code calculation based upon the memory location.
[00:43] Instead, we want JVM to consider four input data elements which are name, age, gender, and SSN.
[00:52] My Person class may have many other instance fields like it can have city and country as well.
[00:58] We can't use a city or country to identify whether a person as a unique person or not.
[01:04] We should be relying on these four parameters like name, age, gender, and SSN.
[01:10] By using the combination of these four elements, I want to identify whether a person is a unique person
[01:17] or a different person.
[01:18] So that's why I'm going to consider these four elements to calculate the hash code.
[01:23] So to calculate the hash code we don't have to worry much.
[01:26] Instead, we can simply use the Objects class.
[01:31] And inside the Objects class we have the hash() method which is going to accept any number of elements
[01:37] of input data.
[01:39] Let me pass the input data.
[01:41] The first input data is name, followed by age followed by gender.
[01:46] And at last I'm going to pass the SSN.
[01:48] So the output from this hash() method we want to return from this method.
[01:53] That's why I'm mentioning the return keyword.
[01:55] So with this we are going to calculate the hash code value for a Person object based upon these four
[02:03] values.
[02:03] Now let me try to execute this program which is HashCodeEqualsDemo.
[02:08] If I try to execute this program this time, I should get the same hash code value
[02:13] because for these two different objects the content is same.
[02:16] So I'm trying to execute this program and you'll be able to see the same hash code value.
[02:21] If you try to execute this program any number of times, you're going to get the same hash code value.
[02:27] So this is one of the rule that you need to take care while overriding the hash code.
[02:32] If you are providing the same executing or running environment, your program should always give the
[02:38] same hash code value.
[02:39] So let me try to execute this program one more time.
[02:42] This time also, you can see I'm getting the same hash code value.
[02:44] This time I'm going to change one of the input data.
[02:48] Maybe instead of 56I can keep the SSN as 55 at the end for the person two.
[02:54] So if I try to execute this program, you can see I'm getting the different hash code values.
[03:00] So this is the power of hash code.
[03:02] So let me roll back to the same SSN.
[03:05] But as of now you can see we are getting the output from the equals() method is false because we are at
[03:11] to overwrite the equals() method.
[03:13] So let's try to overwrite the equals() method as well for the same
[03:16] first let me mention @Override annotation followed by public boolean is the return type followed by equals()
[03:25] is the method name and this method it is going to accept an object with the parameter name
[03:31] I'm going to keep it as o, followed by
[03:34] we can write our own custom business logic inside the equals() method.
[03:38] So whenever you are trying to override the equals() method, there are many scenarios that you need to
[03:43] handle.
[03:44] Especially the edge scenarios
[03:46] or the negative scenarios.
[03:48] The very first scenario that you need to handle is whenever someone is trying to invoke the equals() method,
[03:53] they can pass the same object.
[03:55] For example, here I'm trying to invoke the equals() method on top of p1.
[04:00] I will be able to pass the same p1 as a second object as well.
[04:04] So in this scenario, we straight away want to return the true value because the same object is passed
[04:11] as two different objects for the equals() method.
[04:14] But our equals() method should not be a dumb.
[04:16] It should be able to detect if the same object is passed as a method input parameter
[04:22] also.
[04:23] Then in such scenarios it should always return the true.
[04:26] It don't have to look into the content, because even if you look into the content of these two different
[04:31] objects, we're always going to get the output as true, because we have the same single object being
[04:37] referred as two different objects.
[04:39] So that's why the very first condition that we need to write is with the help of if condition
[04:44] I'm going to check if this is equal to is equal o
[04:48] so with the help of this, I'm trying to refer to the current object where the equals() method is
[04:54] invoked, followed by the second object which is passed as an method input parameter.
[04:59] So
[05:00] if this is true, that means if the memory location of both these two objects is same, I'm trying to
[05:06] return true.
[05:08] So these are very first condition that you need to handle.
[05:11] The next condition that you need to handle is, what if someone is passing a null object as an input to
[05:18] your method?
[05:18] So if you try to compare the null object to content, you're always going to get the output as false.
[05:24] That's why I'm going to write a direct logic, which is o == null.
[05:31] Then in such scenario I want to return the output as false, because even if you try to compare the
[05:39] null object with the this object, you're always going to get the output as false.
[05:43] The next condition you should also take care is you should check whether the two objects belong to the
[05:50] same class or not.
[05:51] If they are different to the two different classes, then you don't have to compare them.
[05:56] You can straight away return the false as an output.
[06:00] For example, here I can write an or condition.
[06:04] After this or condition, I can invoke the getClass() method available inside the same class.
[06:11] Like whenever I'm invoking this getClass(), I'm trying to invoke the getClass() method using the this
[06:17] object.
[06:17] So if the return type of this getClass() method is not equal to the return type of the o.getClass(),
[06:26] then in such scenario
[06:28] also, I want to return the output as false because whenever this is becoming true, that means the
[06:33] class of this object and the class of object o is different.
[06:38] And with that, it should be pretty clear.
[06:40] We are not trying to compare the same objects, so that's why I'm trying to return straight away
[06:46] false.
[06:47] So if these special conditions not satisfied, then only I want to execute my actual logic of comparison.
[06:57] So before I try to write the actual comparison logic, first I need to typecast these Object o
[07:04] to the Person object.
[07:06] Because when I try to compare the data present inside this object, definitely I want the other object
[07:13] also to be as a Person object.
[07:15] That's why let me try to do the downcasting by writing a code which is Person
[07:21] Person is equal to and within the parentheses I'm going to mention person followed by
[07:27] I'm going to mention o.
[07:29] So with this I'm trying to do the downcasting and I'm not going to check with the instance of operator.
[07:34] The reason is this code is going to be executed only if the O class and this class is same.
[07:41] Otherwise this if condition that we have written it is going to be satisfied and the output false is
[07:47] going to be returned.
[07:48] At last, I can try to do the actual comparison by writing a code, which is if age is equal to is equal
[07:57] to person.getAge().
[08:00] So when I refer to the age, I'm going to get the current object age value and the target object is
[08:07] value
[08:07] I'm trying to refer with the help of person.getAge().
[08:11] After the age comparision, I'm going to mention the logical and operator followed by
[08:16] I'm going to compare the gender values with the help of equality operator.
[08:21] Post that I can mention person.getGender() and after this I can mention logical and operator.
[08:28] And now I can try to compare the SSN values with the equality operator followed by person.getSsn()
[08:37] and at last I can try to compare the name values, but name is a String object.
[08:43] We should not use the equality operator.
[08:45] Instead we should use the equals() method.
[08:49] So whenever you are trying to compare the content of two different String objects, you can use equals()
[08:56] method available inside the String.
[08:58] So to this equals() method you can pass the other String which is person.getName().
[09:06] If all these conditions are satisfied, we are going to get the output as true.
[09:11] Instead of invoking the equals() method which is present inside the String object, we can also invoke
[09:18] the equalsUtility() method available inside the Objects class.
[09:22] So you can see to this equals() method I can pass two different objects.
[09:27] One is the name followed by person.getName().
[09:33] So this also perfectly fine.
[09:35] Before I try to execute this class, let me change this p1 to p2.
[09:40] This time you can see we are getting the output as true, even if we try to change the one of the input
[09:46] data, like here.
[09:47] I'm trying to change this to 55.
[09:49] I'm going to get the output as false.
[09:51] And even the hash codes are also going to be different.
[09:54] I hope you understand on how to overwrite the hashCode() and equals() method.
[09:59] So all
[10:00] override these methods.
[10:01] Whenever you have custom requirements to compare two different objects, and to calculate the hash code
[10:07] based upon a given input data.
[10:09] And also, please note that whenever you are trying to override one of these method, you should also
[10:14] override another method as well.
[10:16] And at the same time, you should also make sure you are considering the same input data like here
[10:22] I have considered the four input parameters very similarly the same four input parameters
[10:27] you should also consider inside the equals() method.
[10:30] Otherwise you are going to get the unexpected results whenever you are trying to store your person related
[10:36] objects inside a HashMap or HashSet data structures.
[10:41] So this rule also we discussed in the previous lectures.
[10:44] So please make a note of it.
[10:46] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
