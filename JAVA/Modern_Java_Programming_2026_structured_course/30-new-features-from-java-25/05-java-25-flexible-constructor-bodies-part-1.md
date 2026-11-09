# 30.5 — [JAVA 25] Flexible Constructor Bodies - Part 1

> Section 30: New features from Java 25

[00:00] As part of Java 25 release, a new enhancement around the constructors is introduced.
[00:06] This enhancement name is Flexible Constructor Bodies.
[00:10] To explain you about these new enhancement or new feature.
[00:14] Let me directly jump into the code because this is a complex enhancement and we can't understand it
[00:20] without looking at the code.
[00:22] I created a package with the name flex constructor.
[00:25] Inside the sub package we have these four classes.
[00:29] I'm going to explain couple of problems and how these problems can be resolved by using the Flexible
[00:35] constructor bodies feature.
[00:37] So to show you the problems, I need to switch back to the older releases of Java.
[00:42] So let me go to the settings and under the projects I'm going to select the Java 21 version because
[00:50] it is an LTS version.
[00:51] And similarly under the modules, I'm going to select the language level as 21 with the record patterns
[00:58] pattern matching first switch.
[01:00] So let me apply and click okay.
[01:03] So first let's try to understand what do we have inside these vehicle class.
[01:07] So vehicle class is a simple class.
[01:10] It has a constructor which is going to accept a parameter speed.
[01:14] If this speed value is less than zero then this class it is going to throw illegal argument exception.
[01:21] Otherwise it is going to simply assign the given speed value to the instance field that we have inside
[01:28] this class.
[01:29] So this is a simple class.
[01:30] So this class it is going to act as a parent class.
[01:33] So let's look for the subclass of this class.
[01:36] So the subclass is car by the way you can get all this code from the GitHub repo.
[01:41] Inside this car class I'm trying to extend vehicle.
[01:44] This car class also has a constructor which is accepting a speed value.
[01:48] So by passing the same speed value, it is trying to invoke the super constructor.
[01:53] Because inside the constructor of a subclass, always the super statement should be the very first statement.
[01:58] Otherwise we are going to get a compilation error.
[02:00] For example, if I comment this code, I'm getting a compilation error from the Java saying that there
[02:06] is no constructor available inside the vehicle parent class, because by default the compiler it is
[02:13] going to add super without any arguments.
[02:16] That means it is going to call a no argument constructor inside the parent class.
[02:21] Since my parent class does not have any no argument constructor.
[02:25] I'm getting this compilation error, so this should give a confirmation to you that always the very
[02:30] first statement inside the constructor of a subclass is super.
[02:34] So even if the developer is not invoking the super constructor.
[02:38] Behind the scenes, the compiler is going to add a default super constructor invocation.
[02:44] But with this setup, which we are having from the last 30 years inside Java, we have some problems.
[02:50] If you see the problem with this setup is I'm trying to pass the speed variable directly as a very first
[02:56] statement to the parent class.
[02:59] Inside the parent class, they are doing the validations and if these validations are passed, then
[03:04] only the parent class object will be created.
[03:07] Otherwise we are going to get an illegal argument exception in the similar lines inside the subclass
[03:14] constructor.
[03:14] Also, once the parent class constructor is created by executing the super logic.
[03:20] We're doing another validation, which is if the speed value is greater than 200, we are throwing another
[03:26] exception.
[03:26] Are you seeing the problem here?
[03:28] Instead of failing fast, we are failing slowly.
[03:32] Let's imagine I have sent the speed value as 250.
[03:36] In this scenario, the vehicle object will be created, but the car object will not be created because
[03:43] the speed is greater than 250 and we are throwing an illegal argument exception.
[03:47] But with this kind of setup, there is going to be some performance damage.
[03:51] Let's imagine inside the vehicle constructor you have some heavy logic which is going to take some few
[03:58] milliseconds time to execute.
[04:00] So in this kind of scenario you are definitely going to have some performance problems.
[04:04] And at the same time you are not failing fast.
[04:07] Maybe to handle these kind of scenario efficiently all these days.
[04:11] Developers, what they used to do is they used to create a static method inside the subclass.
[04:18] For example, here I created a subclass with the name verify speed.
[04:22] If the speed value is greater than 200, we are throwing this illegal argument exception.
[04:28] Otherwise, this method it is going to simply return the speed value by leveraging the static method.
[04:33] They can get rid of these validations and while invoking the super constructor, they can invoke the
[04:41] static method along with the input speed value.
[04:44] So with this setup, what is going to happen?
[04:46] Before calling the super constructor, we are making sure we are doing enough validations inside the
[04:53] subclass.
[04:53] But what about the superclass validations?
[04:57] So here inside the superclass also it is trying to perform some validation.
[05:01] Maybe developers, they can further optimize these by moving these logic into the static method that
[05:09] we have introduced in the subclass.
[05:10] Maybe here they can add one more if condition where they check if the speed value is less than zero.
[05:17] They are going to throw this illegalargumentexception otherwise.
[05:20] The later one is going to be thrown.
[05:23] So this code is working perfectly and handle our problem perfectly.
[05:27] But this may not be a solution 100% of the times.
[05:32] For example, I may want to do some initialization of the variables just before the super invocation,
[05:38] or I may want to do some complex validations to handle all these kind of scenarios.
[05:43] Now, as part of the Java 25, what Java team they have done is they started accepting some business
[05:49] logic just above the super keyword or this keyword.
[05:54] Before I try to show you the solution by using the Java 25 feature.
[05:58] Let me show you another problem that we typically face before Java 25.
[06:03] For the same I have other two classes, so the classes are account and saving account.
[06:08] So first let me open the account.
[06:11] So account is a parent class where it has a default constructor.
[06:15] From this default constructor it is trying to invoke the check method available inside this class.
[06:21] This check method is an empty method.
[06:23] You can write some logic as well, since our explanation has nothing to do with the logic present inside
[06:29] the check method.
[06:30] I left this method blank intentionally.
[06:32] Let's open the child class of this parent class.
[06:35] The child class is savings account.
[06:37] Inside the child class we have a field with the name account number.
[06:41] Anyone who want to invoke this class, they have to pass a number.
[06:45] The same number we are going to assign by using this.
[06:48] This dot account number is equal to number and this subclass.
[06:51] It is also overriding the check method present inside the parent class.
[06:56] So inside the check method we are checking if the account number dot length is equal to zero.
[07:02] We're throwing a runtime exception which is invalid account here.
[07:06] Also we have a super default constructor invocation.
[07:09] Even if I delete these, I'm not going to get any issue because behind the scenes the compiler is going
[07:14] to add the default super constructor invocation logic.
[07:19] So that's why we're not getting any compilation error with this setup.
[07:22] We have a problem.
[07:23] If you closely observe.
[07:25] Let's imagine someone is trying to create the constructor of the saving account by passing a valid account
[07:32] number.
[07:32] So with that, what is going to happen?
[07:34] This constructor is going to be invoked.
[07:37] But before this logic is going to be executed, the parent constructor will be invoked from the parent
[07:44] constructor.
[07:45] We are invoking the check method present inside this class, but from the parent class if you try to
[07:50] invoke the check method, since the subclass is also having the same check method Overrided, it is
[07:56] going to execute the logic present inside the subclass.
[07:59] And with that, what is going to happen?
[08:01] This account number?
[08:02] It is going to have null because we are had to do this assignment.
[08:06] Before this assignment itself, the super constructor is invoked from the super constructor.
[08:12] The check method is invoked.
[08:14] So null dot length we are going to get null pointer exception instead of this runtime exception.
[08:19] Maybe what I can do is I'll try to mention a main method saying that.
[08:25] Public static void main.
[08:28] And from this main method I'll try to create the object of savings account.
[08:33] I'm passing a valid account number.
[08:35] If I execute this program, I'm going to get a null pointer exception.
[08:39] But before that seems my build is failing.
[08:43] Maybe I'll go to the Hello World program and delete this entire code.
[08:48] Don't worry, I'm going to add this later and checking into the GitHub repo.
[08:52] So let me do the build here.
[08:54] Also, I'm getting a compilation error since we have shifted to the Java 24.
[08:59] Let me remove that and do the build.
[09:03] I'm getting a problem again.
[09:06] Let me fix this problem.
[09:08] Let me do the build again.
[09:09] This time the build is successful.
[09:11] Now if I try to execute this main method, I should get a null pointer exception.
[09:17] Yes, we got a null pointer exception.
[09:19] So are you seeing the problem here?
[09:21] Though this code looks perfect, but we are facing the problem just because we are not able to initialize
[09:28] the child class variables.
[09:31] Just before invoking the super keyword, we know by default the compiler is going to add this super
[09:38] constructor invocation.
[09:39] But if I try to move this initialization logic just above super, I'm getting a compilation error because
[09:47] the Java compiler is not going to accept any Java statements about the super constructor invocation
[09:53] are the same class constructor invocation by using the this keyword to solve these kind of problems
[09:58] as part of the Java 25, the Java team, they made some adjustments to the Java compiler to allow some
[10:05] statements inside the constructor about this and super invocations, so that enhancement is called as
[10:12] flexible constructor bodies, because right now inside the Java constructor bodies, there has been
[10:18] given some flexibility to the developers to execute some meaningful logic about the super and these
[10:23] constructor invocations.
[10:25] Inside the next lecture, let's try to understand how to solve these problems by using these new enhancement
[10:31] from the Java 25.

----------------------------------------
