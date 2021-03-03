---
layout: post
title:  "Homework Six"
subtitle: Docker Part 1
date:   2021-03-3 12:00:00 -0500
categories: Microservices Homework
permalink: /Homework-Six/
---

#### Docker Photos


### Retrieve Container Image
![Retrieve Container Image](/images/docker1.png)
### Downloading Container Image
![Downloading Container Image](/images/docker2.png)
### Build the image
![Build the image](/images/docker3.png)
### Building Image
![Building Image](/images/docker4.png)
### Start container instance based on image
![Start container instance based on image](/images/docker5.png)
### Finished  
![Finished](/images/docker6.png)
### Task Manager/Resource Usage
![Task Manager/Resource Usage](/images/docker7.png)
### Second Docker Process
![Second Docker Process](/images/docker8.png)


#### Docker vs the Host

The container engine(Docker) for the recnetly created container is running directly inside the OS as any normal program or service would run. However, the container itself is isolated from the rest of the machine. This is done through concepts originating from the linux os kernel. Linux OS kenerls provide Namespaces and controlgroups, as well as allowing commands like chroot(to change the root directory of a process). The container image also provides the container with its own filesystem, and it is the only filesystem it has access too so it must contain all of its needed files/binaries. 

Namespaces allow things like PIDs being reusable and contained. For example, pid 9 could be the host systems file service while pid 9 could also be a containers file service at the same time. While PIDs normally are unique identifiers for a process, in this case they're still unique due to being in different namespaces. 

Cgroups allow us to allocate resource usage/access such as limiting the memory a processes or container is allowed to use. 

Chroot (Change root) does what it sounds like. It creates a new root directory for a process. Since a root is the origination point, if you change the root directory to be different from the actual root of the OS you're on you essentially create a new isolated branch (When combined with other technologies). This allows us to prevent processes from accessing the file system(s) outside of their own chroot branch/tree.
 
 When we combine all of these, we get an isolated standalone container. 

 The host operating system is aware of the processes to some degree through the container's engine but the container itself doesn't know about other processes running. It is unable to interact with other processes on the host outside of its engine. 





