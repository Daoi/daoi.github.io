---
layout: post
title:  "Homework Four: AWS"
subtitle: Cloud + Microservices
date:   2021-02-18 12:00:00 -0500
categories: Microservices Homework
permalink: /Homework-Four/
---

#### Screenshots of AWS Amplify App

### AWS Auth
![Amplify Account Creation/Auth](/images/AmplifyLogin.png)
### AWS Auth Email Verification
![Amplify Auth Verification email](/images/AmplifyLogin2.png)
### AWS Auth 2fa
![Amplify Login 2fa](/images/AmplifyLogin3.png)
### AWS Build Dashboard
![Amplify Console Build Status](/images/AmplifyConsole.png)
### AWS Deploy Dashboard
![Amplify Console Deploy Status](/images/AmplifyConsole2.png)
### AWS Build Console(In progress of build)  
![Amplify Build Console](/images/ModifyRepo.png)
### AWS Building
![Amplify Build Console Front end](/images/ModifyRepo2.png)
### AWS Building
![Amplify Build Console Back end](/images/ModifyRepo3.png)
### AWS Finished Building
![Amplify Build Console Finished](/images/ModifyRepo4.png)
### AWS Finished Deploying
![Amplify Deployment Finished](/images/ModifyRepo5.png)
### AWS Finished
![Amplify Deployment Result](/images/NotesApp.png)

#### How does the cloud aid microservices?

Microservices and the cloud go well together because microservices independent/scalable nature can take advantage of benefits offered by the cloud and services like AWS. AWS allows you to automatically spin up resources as needed in regions that are close to where they're needed. For example if your login/auth services are microservices you can host them on AWS and allow amazon's could services to handle scaling up and down your service as its needed. If you tried this with a monolithic app it would be a lot more difficult to scale as instead of just starting up a portion of your function you'd likely need to start up the whole thing, which probably doesn't make sense if the only issue is authentication. Similarly, microservices independent nature makes them likely easier to deploy and host and works well with cloud containers. AWS for example has setups for containers/ec. If you want to update one service you can simply just use code deploy/pipeling to push the update when its ready for product and only affect part of your services. If you need to spin up a new instance of a service containers allow you to do this more quickly compared to full virtual machine. While VMs virtualize the entire hardware stack, containers try to virtualize at the OS level. This allows your program to run in a light weight environment that only requires the files needed to run, as opposed to needing to virtualize an entire guest OS ontop of the servers OS.

Since Microservices are also have complete control of their data layers and function you can take advantage of the clouds ability to configure each service as needed. For example using different DB types such as NoSQL or PostgreSQL, different load balance configurations or even different server operating systems/configurations. All of this is made easy and provided for you by cloud services like AWS. While some of these benefits can be taken advantage of Monolithic applications, Microservice architecture allows you to fully utilize the benefits of cloud computing. 







