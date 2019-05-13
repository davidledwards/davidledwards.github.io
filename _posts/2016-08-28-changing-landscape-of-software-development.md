---
layout: post
title: David Edwards / Blog
topic: The Changing Landscape of Software Development
date: 2016-08-28
---
I stumbled upon a series of [blog posts](http://blog.cognitect.com/blog/?tag=NewNormal+Series) (series starts [here](http://blog.cognitect.com/?offset=1457011971947&tag=NewNormal+Series)) a few months ago that really ought to be mandatory reading for anyone in the business of developing software. While these posts from [Michael Nygard](http://www.michaelnygard.com/) may appear to be written with the software practitioner in mind, I can assure you that his writing is quite approachable, and therefore, digestible in most cases by virtually anyone in the value chain of producing software.

The main thesis of this series, titled _The New Normal_, is that if IT companies wish to remain relevant and competitive in the current landscape, they will need to fundamentally change how they build and deliver software. The economics of software have changed so dramatically in recent years that new tools and techniques make it possible to do what was once considered impossible.

He starts the series by talking about failure in systems and how we should embrace it rather than prevent it. This is not a new idea, but many IT organizations are still stuck in a world where they spend countless amounts of money making infrastructure highly available, only to be disappointed when catastrophic failures inevitably happen. Resiliency, or what he affectionately calls _[antifragility](https://en.wikipedia.org/wiki/Antifragile)_, is a property of the software architecture, not the infrastructure.

He then goes on to talk about the inherently conflicting incentives of engineering and operations, in which engineering is asked by the business to produce a steady stream of new features, whereas operations is conditioned to keep systems stable. The conventional wisdom of traditional IT organizations is that in order to deliver stable applications they must somehow limit the amount of change. It turns out this rationale is completely wrong. It may seem counterintuitive, but the most effective means of minimizing risk is to in fact maximize change.

Perhaps one of the most insightful assertions in the entire series was the idea that source code should not necessarily be viewed as an asset, but instead as a liability. And further, that we should start treating code as disposable. These statements may seem shocking or perhaps even heretical to many, especially since we tend to think of previously written code as something that can be reused, and thus, save money and increase productivity. And while that may be true, the essential point he makes is that code is akin to inventory and requires maintenance, so the more that sits on the shelf, the more money we spend on preservation. Even more, software decays over time, resulting in the accrual of technical debt that must eventually be paid down.

Later in the series, Nygard talks about the importance of team-scale autonomy as a critical component of moving fast and being responsive. The underpinnings of such autonomy include, among other building blocks, an adaptive and evolutionary architecture, isolated failure domains, and behaviors and processes that enable continuous delivery.

If this series is not on your reading list, then you will almost certainly be missing out on some important ideas that just might change the way you think about software design in the future.
