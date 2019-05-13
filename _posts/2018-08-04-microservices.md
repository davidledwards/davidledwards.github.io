---
layout: post
title: David Edwards / Blog
topic: Microservices
date: 2018-08-04
---
The notion of evolvability in the current landscape and frenzied pace of computing is a compelling architectural property that enables product development organizations to respond more quickly to customer and market demands.

Looking across the enterprise landscape, the most common architectural style we see in software systems is some form of a _monolith_. This is not unusual, particularly for startups or established companies developing new products, both of which have a desire to move fast. A startup also has the distinct advantage of having no legacy product that might encumber rapid progress.

In the domain of software architecture, there is something called an [architectural quantum](https://www.oreilly.com/library/view/building-evolutionary-architectures/9781491986356/ch04.html), which is an independently deployable component encapsulating all structural dependencies necessary to function. I use the term component in a general sense, which could be an application or a service, but the key point is that the architecture quantum draws a boundary around something that can be deployed standalone.

In concrete terms, what we consider to be an architectural quantum depends entirely on the architectural style. Let me give an example.

Imagine we design a modular system composed of applications and services. The fact that the system is modular does not necessarily imply that the architectural quantum is the module itself–individual applications and services. If the applications and services are coupled in a way that makes independent deployment impossible, then the architectural quantum is actually the entire system. We just described a _monolithic_ architecture.

A [microservices](https://en.wikipedia.org/wiki/Microservices) architecture, by contrast, is one in which the architectural quantum is the service, the boundary of which is notably smaller than the aggregate system. Any useful system is typically composed of many services working together, but in a microservices architectural style, each service is designed in such a way that it can be deployed independent of other services. Microservices enable and promote _evolvability_ because an individual service is allowed to change without impacting other parts of the system.

A monolithic system is not inherently evil in any way. It might be the best architecture for the problem at hand, such as finding product-market fit. If you plan to throw away lots of code or heavily refactor a system during the journey to product-market fit, making investments in evolvable architectures, like microservices, might be putting the cart before the horse. However, once a product has gained adoption and the number of customers and users continues to expand, and there is a growing backlog of feature enhancements, the choice of architecture suddenly becomes important. A monolithic architecture may no longer be sustainable for delivering new features in a timely manner.

As the size of the system grows, so does the complexity of couplings and interactions between all the various components, making change much more challenging and costly. Remember, the architectural quantum is the entire system, so a single change requires a complete redeployment. Depending on the complexity of couplings between components, it gets increasingly difficult to verify that a change will not have adverse side effects in other parts of the system. Even though all monolithic systems are not created equal–ranging from well-organized and modular to a giant ball of mud–the nature of monolithic architectures allows tighter couplings to creep into the software. And, they always do. The gravitational pull of a monolithic system grows over time and it becomes increasingly harder to break away.

Microservices have become increasingly popular in the software industry especially as infrastructure and tooling has matured, enabling what was operationally challenging for most organizations. The idea of deploying dozens of services, as opposed to a single application, does indeed elevate the operational complexity. But, with virtualized infrastructure and container-orchestration systems, coupled with modern-day deployment automation tooling, those operational challenges are no longer insurmountable.

Ultimately, what we are seeking is faster delivery of innovation and increased responsiveness to market needs. Our ability to move quickly and efficiently is not accidental, but rather the result of intentional efforts in evolving how we build and deliver products.
