# 4.27 — How to define constant final static variables

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] As of now, we have created the static variables inside the Car and Employee classes.
[00:06] But right now we are facing a problem, which is we are able to change the values of the static variables
[00:13] at later point of time inside the Java execution.
[00:16] And this sometimes may create serious problems because knowingly or unknowingly, other developers may
[00:23] change the values inside the static variables and it may create some issues inside your Java application.
[00:30] So how to avoid this scenario is by making your static variable as final.
[00:36] So just after the static we can type a ' new ' keyword which is final.
[00:41] Whenever we are using this final, we are telling to the Java and JVM.
[00:46] Please, please make sure no one is changing this value initially that I have provided, which is 4.
[00:53] Now
[00:53] if I go to the CarMain.java, you'll be seeing a compilation error that I cannot assign a new value
[01:02] to the final variable, which is numberOfWheels.
[01:05] This way we are trying to avoid the scenarios of changing the static variable values.
[01:11] If someone want to really change it, they need to stop the execution,
[01:15] they need to change the value and post that they need to rerun the program.
[01:19] So that's the beauty of final keyword.
[01:21] Whenever we define a variable with the help of final, we call such variables as constant
[01:27] variables or constant fields. Because the value that we store inside these fields or variables.
[01:33] They are going to be constant forever, and we cannot change the values. Inside java,
[01:39] whenever we are trying to create the constant fields, we need to follow a naming convention.
[01:45] Instead of camel case, we should follow the snake case style.
[01:48] So what is a snake case style?
[01:50] Inside the snake case style, each word has to be separated with the help of underscore, and after
[01:56] that, each and every letter can be converted to a lower case or uppercase.
[02:02] Inside Java, the standard is to have all the letters in the uppercase format.
[02:06] That's why let me change this value to number N0_OF_WHEELS.
[02:14] So wheels
[02:15] Also I'm going to keep it in complete capital letters.
[02:19] So this is the format that we need to follow whenever we are trying to create the static and final variables.
[02:27] Let me do the same inside the Employee.java also.
[02:30] So here also I don't have a scenario where this Employee name is going to change at runtime at later
[02:37] point of time.
[02:38] If you really have a scenario where your static variable needs to be changed at multiple times, then
[02:44] you should be fine without using the final.
[02:47] But the scenarios that we have, which is EmployerName and numberOf Wheels in both the scenarios,
[02:52] we want these values to be never changed.
[02:54] So that's why here also I'm going to mention final keyword and I'll change this field name by following
[03:00] the snake case.
[03:01] I'll just mention EMPLOYER_NAME and the value is going to be Google.
[03:07] So if you see here under CarMain.Java, I'm getting an error now because the field name is changed
[03:13] to NUMBER_OF_WHEELS.
[03:15] So the same I have to use and I have to remove this line because since right now our static variable
[03:21] is final, we cannot change the initialized value at later point of time.
[03:26] That's why I'm going to delete these
[03:28] and also I'm going to delete this statement as well.
[03:30] Now let me go to the EmployeeMain here
[03:32] also we are going to get a compilation error because we change the employeeName variable.
[03:37] So the correct variable name is EMPLOYER_NAME.
[03:41] With this we can try to execute the program
[03:44] once you can see I'm getting the same output which is Google under the CarMain
[03:48] also I'm going to get the same output which is 4.
[03:51] This way we can make our static fields as final.
[03:55] For your reference, I have mentioned all the points that we have discussed inside this slide.
[04:00] So whenever you have some questions around how to declare a static variable as a constant field, then
[04:06] please refer to this slide.
[04:08] Please note that we should always follow the snake case inside the Java whenever we are creating a constant
[04:15] field.
[04:15] I hope this is clear.
[04:16] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
