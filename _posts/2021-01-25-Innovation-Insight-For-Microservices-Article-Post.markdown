---
layout: post
title:  "Homework One: Innovation Insight for Microservices Article"
subtitle: Homework One
date:   2021-01-25 15:36:29 -0500
categories: Microservices Homework
permalink: /Homework-one/
---

#### Main Take Away
MSA(`Microservice Architecture`) has several benefits when used in the right sitatuion, but knowing the right situation is key to gaining any of the benefits. While MSA can improve the ability to constantly evolve your product through continous development, allow you to easily scale up or down dependning on need, and make your development systems more agile it can also add unneeded complexity, training and technical cost, and requires large shifts in the development process from more traditional systems. 

If your bussiness for example has very static traffic, you won't gain much benefit from scalability. However, perhaps you could benefit from the reduced chance of collisions and breaking when you add new features if you use MSA. MSA is typicall used in MASA applications(`mesh app/service architecture`) where the back end is composed of many services and the front end is made up of interface components or apps. 

When you use MSA and this style of application adding new features is as simple as adding a new service to the back end and an interface component to allow access to that service for users. While services may interact, MSA tends to reduce dependency and conflict. In a monotholic application, when you add new features its very easy to become entangled with other features usability or conflict. Further, its difficult to find what the cuase of conflcits can be because you have a giant code base to sort through, as opposed to a small isolated service. 

However, if you don't often add new features, then you might just be adding complexity for no reason. MSA requires many constraints to ensure that the components remian granular and independent. If your application doesn't frequently add new features and keep up with an ever evolving demand from customers, you may not benefit from the this granularity. Instead, it would be better to stick to more traditional schedules of updating to save yourself the work and investment required to switch to a MSA style of devops. 

Its also possible for an application to use a combination of different architectural styles. Gartner came up with 3 based on granularity, `macroservice, miniservice, and microservice` from least agile to most. Macroservices are used to interact with monolithic applications, miniservices are a sort of inbetween of micro and macroservices, with a more relaxed scope and constraints than a miniservice but might handle multiple responsiblities. 

![Microservices vs Monolithic](/images/monolithic-vs-microservices.png)


#### When to use? 
Microservices seem to go well with companies that provide services that have large userbases and high numbers of people using the service at once. Microservices allow the company's application to easily scale up at busy hours, perhaps after work or on the weekends, holidays, etc, and scale down when people aren't using the website such as late night. Perhaps they can scale up one region during its late night, but scale up in another region which might be midday. The flexibility provided by MSA could potentially save a ton of money, diverting resources only to where they're needed. These companies also tend to have large competitors meaning the ability to easily update and add new features also becomes important, another benefit provided by MSA. Companies like streaming services (music or tv) and social media are obvious use cases. 

However, if your website remains mostly the same and is perhaps rarely under heavy load, something like miniservices might be more benefical. Maybe you'll occasionally have busy periods or add a feature or two a year. Things like online banking seem to fit in well here. The reduced complexity can help reduce the already high demands of security in such applications, but also provides the ability to be somewhat flexible and still compete with other services in the markets through continuous development, though to a lesser degree. 


