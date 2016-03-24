---
layout: post
title: David Edwards | Blog
topic: A Scala API and CLI for ZooKeeper
date: 2012-12-17
---
Part of my efforts in learning Scala have led to the development of a functional API over
[ZooKeeper](https://zookeeper.apache.org), as well as a much improved CLI, both of which I am sharing today. The source is
located in [GitHub](https://github.com/davidledwards/zookeeper) and licensed under ALv2.

If you happen to know something about ZooKeeper, it’s essentially a distributed, fault-tolerant configuration system used
primarily for coordination among a network of processes. At the core of the system is an implementation of the atomic broadcast
protocol, which provides a means for data replication by ensuring a total ordering of all events at each replica. ZooKeeper is
being used increasingly in open source projects to improve the reliability of distributed systems by eliminating single point
failures. One notable example is Apache Hadoop HDFS, which has long suffered from the lack of fault-tolerance in the NameNode.

It turns out that the Java API for ZooKeeper is quite awful to work with despite the fact that the system itself seems to
function very well. Of course, this is one man’s opinion, though I think most of my colleagues would agree with that assessment.
Perhaps I’ll elaborate more on what I feel is wrong with the API, but not in this post. In any manner, my primary goal was to
fix many of these problems by building a more intuitive and functional interface on top of the original API.

I would also encourage you to look at the new command line program that was built using this new Scala API. The new CLI was
designed to replace `zkCli`, an application assembled with the ZooKeeper distribution that is practically unusable. The new CLI
provides some nifty capabilities, such as TAB completion of paths to quickly navigate the node space, support for relative
paths, recursive listing of nodes, and several other aesthetically pleasing features. I think you will find it much more
enjoyable to use.

Bear in mind that this is still work in progress, though both the API and CLI appear to be quite stable. The API project is
nearing completion with a significant amount of ScalaDoc, but would benefit from additional documentation and plenty of code
examples. The CLI project could use some refactoring to eliminate a bit of redundancy, but for the most part, it works quite
well.
