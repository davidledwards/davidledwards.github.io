---
layout: post
title: Blog
topic: An Approachable Explanation of APIs
date: 2023-08-02
---
<div class="content" markdown="1">

Original article published [here](https://medium.com/@david.l.edwards/an-approachable-explanation-of-apis-7ca33157d34a).

The term API, or *Application Programming Interface*, is used quite liberally across the software industry, but there is often a lot of confusion surrounding its strategic importance and precisely what actions should be taken by product teams. Everyone sort of knows that they should be developing APIs, but they tend to lack a compelling business case and a strong cultural affinity that one could argue stems from simply not fully comprehending the potential.

At a fundamental level, software is doing nothing more than performing a series of state transitions, albeit usually in a nontrivial and sophisticated way. Think of state transitions as steps in a workflow—create a quote, add an item, change the discount, and so on. Software ensures that those transitions occur in an orderly and correct way. Those same state transitions, in aggregate, represent the intellectual property of a company, presumably done so in a way that is novel and differentiable in relation to competitors.

We generally think about products in terms of their UI, or *user interface*, because they are visual and oriented around human interaction. You can think of the UI as a means of orchestrating the underlying state transitions through workflows. Even though humans interact through the user interface, all that pomp and circumstance essentially boils down to moving bits through various states until something useful happens.

So, rather than refer to state transitions, which leans a bit technical, let’s instead use the term *system* that is an embodiment of those state transitions.

The point of distinguishing between systems and the UIs that orchestrate them is that the real intellectual property is often embedded in the former. This does not imply that UIs are not novel in their own way, but when you think about many of the unique and sophisticated things that companies solve through software, the bulk of that intellectual property is embodied in the system, not the UI. The UI is simply a way for humans to interact with those novel algorithms.

At this point, the concept of APIs should begin to make more sense. While UIs are designed for *humans*, APIs are designed for *machines*. Both forms interact with an underlying system, and that system carries out a series of meaningful state transitions that eventually do something useful. However, the needs of a human differ from the needs of a machine. APIs are abstractions over the possible state transitions inside a system, whereas UIs are workflows over those state transitions.

One useful way of reasoning about the relationship between UIs and APIs is that UIs could, in theory, be constructed on top of APIs. In practice, though, most products are not designed in this manner. Instead, there tends to be a singular focus on the UI because, more often than not, the initial audience is the human. A consequence of this design ethos is that UIs are usually interwoven with the system, meaning that there is no abstraction in the form of APIs that separate the UI from the system itself. As products evolve, APIs tend to be retrofitted into a system to accommodate the requirements of a new kind of actor, *machines*.

A convenient way of thinking about APIs is that they represent the points of connection with a system. An example is your outdoor water spigot. It is a connection point with the water supply, where water flows when the spigot is opened and stops when closed. None of us particularly care how the water flows, just that it does what we expect it to do. The things we attach to the spigot are analogous to UIs—sprinklers, power washers, and so on.

A term you may encounter when describing some types of software companies is *API-First*. Roughly speaking, it encompasses a design philosophy that starts by modeling features and capabilities as APIs before doing any work on UIs. These companies place a significant premium on APIs because they consider them to be very strategic, usually for business reasons but not always. In some cases, it is driven by a sense of architecture dogma, meaning that it is simply the best way to build evolvable software systems.

An important question to ask is *why build APIs*? Aside from architecture dogma, is there a legitimate business need for machines to connect and interact with products? It would seem that the answer is quite obvious and perhaps relegated to the ashes of settled arguments, but many companies struggle to fully appreciate their strategic importance. Developing APIs and bringing them to market does not require anyone to necessarily embrace an API-first culture, but it does require a shift in product thinking.

On a strategic level, APIs…

* Create stickiness—the deeper the integration of products with customer ecosystems, the harder it becomes to remove them.
* Create scale—by enabling partners and third-party developers to integrate, customize, and build new products.
* Create opportunity for growth—machine integration opens up new value for customers and partners.
* Create new ways to innovate—by expanding the channels of development beyond traditional product teams.

The fundamental shift in mindset around APIs is the elevation of their importance on par with UIs. In principle, APIs are no different than UIs when it comes to making decisions of priority and where to invest time and resources. The key point to convey is that APIs are intentional, not accidental. They are not byproducts of development, but rather the *product* of development.

Drawing a parallel to UIs, similar kinds of supporting resources are required for APIs. Documentation is a prime example—partners and third-party developers need ways to learn about the interfaces and how to invoke them properly. And, in the same way that users authenticate through UIs and are constrained in what they can do based on permissions, APIs must have similar authentication mechanisms that restrict the things machines can do. APIs also need to monitor usage similar to how one might track human usage patterns in UIs.

An ideal structural configuration for developing and delivering APIs, particularly when multiple products are involved, is to think in terms of products and platform. Each product team is responsible for defining and building APIs, which intuitively makes sense because each inherently understands their respective domain. A platform team would play a critical role in driving consistency across products by defining policies, standards, and guidelines using a federated form of governance, and then, most importantly, codifying those cross-cutting concerns in the platform itself.

In essence, a platform team owns and operates opinionated infrastructure for hosting APIs developed by individual product teams. The platform would presumably standardize authentication, monitoring, rate-limiting, auto-scaling, and so on. And, in exchange for conforming to an opinionated platform, product teams can then focus on designing and delivering APIs for their respective domains.

</div>
