---
layout: post
title: David Edwards / Blog
topic: Deploying Open Source Projects
date: 2013-04-10
---
Over the past year, I’ve spent a fair amount of personal time studying the [Scala](http://www.scala-lang.org) programming
language, a statically-typed and functional language that runs on the JVM.

An effective means of learning a new language is oftentimes as simple as writing small programs or libraries with well-defined
boundaries. I’ve shared in a previous [post](http://loopfor.com/2012/12/17/a-scala-api-and-cli-for-zookeeper.html) my desire
to build a better command line program for ZooKeeper. This work led to developing a more intuitive and functional Scala-based
API over the ZooKeeper client library. Additionally, I factored out the option parsing code into its own project, primarily
because of a need for simple option parsing in other areas.

All of these projects are listed on my [Github page](https://github.com/davidledwards). Outside the scope of learning Scala, but
a necessary step in facilitating the use of open source contributions, is deploying the artifacts of those projects to a central
location. So, this led to an interesting and sometimes painful exercise in preparing the projects for deployment to the Central
Maven Repository via [Sonatype](http://www.sonatype.org). The gains were worth the effort, though.

In the end, a successful deployment boils down to the practice of good software engineering discipline, as well as the inclusion
of comprehensive documentation, which makes your contribution more accessible to others.
