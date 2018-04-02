---
layout: post
date: 2018-04-02 09:00
title: Understanding XPages Part 5
tags: xpages jsf
published: false
---
## Faces-Config.xml and Dependency Injection
Hopefully this isn't a new term for you, but here is a brief explanation in case it is. Beans often rely on one another. Your `MyStuff` bean needs your `User` bean; your `User` bean needs your `UserService` bean. Outside of JSF, we would pass these dependencies through the constructor, but that isn't an option due to the zero-argument requirement. So JSF provides another mechanism for initializing beans in faces-config.xml - the managed property. (Side note: newer versions of JSF move this out of faces-config and into class annotations.)

<!-- more -->

[Here is an example faces-config](/faces-config-example-1/). It declares 4 beans, one in each scope. Let's suppose our ProjectService bean has a method `findProjectById(String id)` which does a lookup to the Project table, but the location of the table 

[Part 1](/Understanding-XPages-part-1)
[Part 2](/Understanding-XPages-part-2)
[Part 3](/Understanding-XPages-part-3)
[Part 4](/Understanding-XPages-part-4)