# Introduction to Jenkinsfile

*Section: Jenkins Pipeline - Jenkinsfile*

Instructor: Hello and welcome back. In this video, we're going to learn how a Jenkins pipeline looks like. And of course, we're going to learn what is a Jenkins pipeline. Well, let me tell you that everything that I told you in the previous video, I mean, building the entire workflow is a complicated task. But Jenkins actually allows you to easily do this. And to do this, we have something that is called Jenkins Pipeline, normally known as Jenkins as code, pipeline as code.

Well, and this is just a simple example but probably you are already used to this kind of code because you've done a lot of DSL and probably you can find this familiar. So, okay, this is how a pipeline looks like. It's super simple. You define a pipeline and then you start defining stages. Remember, a stage is nothing else but a step of your workflow. So for example, you say stage, your build stage, and then you do what you wanna do in that stage.

Stage test and here you do whatever you wanna do there. Third stage, deploy, and then you do whatever you wanna do there. So it's super simple to build a pipeline. So, here we have an important point, and that is that in Jenkins, we've got two types of pipelines. We have the declarative pipeline and the scripted pipeline, as you can see here. And there is a lot of difference between these two because normally declarative pipeline is super good for people who don't know too much about code.

I mean too much about Java or about Ruby or about programming languages. Normally for SysAdmins or people that do not develop applications. So this is like a template, and you can define all of your steps in here, and it's super simple to do. But in the other hand, we've got scripted pipeline. And the scripted pipeline is actually a little bit more complicated because it's actually written on Groovy.

So you need to define every single thing on Groovy, which is something like Java. And if you don't know Groovy, and you don't even know Java, so this is going to be super complicated for you because you need to start learning Groovy and Java and probably you don't wanna do that. So, we're gonna be talking about this declarative pipeline because it's super simple to use. We only need to follow this structuring here to create stages and then inside of the stages, we can do whatever we want using any programming language or any Bash or Ansible or Python.

So as I told you, we're going to be using a lot of the declarative pipeline in here. You're going to be learning a lot of this and it's up to you if you wanna learn the scripted pipeline, but don't worry because both of this actually work for the same thing. So it actually depends on you what you wanna choose. I'll see you in the next lesson.
