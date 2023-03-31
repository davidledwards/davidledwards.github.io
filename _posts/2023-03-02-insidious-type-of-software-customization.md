---
layout: post
title: Blog
topic: An Insidious Type of Software Customization
date: 2023-03-02
---
<div class="content" markdown="1">

Original article published [here](https://engineering.vendavo.com/an-insidious-type-of-software-customization-8dd0ada28c16) as part of the [Vendavo Extensibility Series](https://engineering.vendavo.com/extensibility/home).

We briefly explained the idea of _configuration_ and _extension_ as acceptable forms of software adaptability in the [prior post on software customization](/blog/2023/02/23/understanding-types-of-software-customization). The key point to emphasize is _adaptability_ of the software — customization is simply a means of achieving that objective.

A basic principle of software design, which naturally lends itself to both configuration and extension, is this idea that the internal mechanics are protected by interfaces. This is a good thing for sure because it enables software designers to build and evolve high quality products.

Continuing with the vehicle analogy from our prior post, the majority of drivers are not concerned with what exists under the hood or behind the dashboard, nor should they. Our interaction with the vehicle happens through interfaces — steering wheels, gas pedals, brake pedals, shifting paddles, touch screens, and so on. Many manufacturers will go so far as to void the warranty if you do things like muck around with the engine or the onboard computers. It doesn’t mean we can’t do those things, but we have to understand the tradeoffs.

And so, this brings us to another type of customization, called _modification_. This style tends to be quite common despite the unfortunate set of future tradeoffs.

The general idea behind software modification goes something like this:

Crack through the outer shell
Expose access to internal state
Change or augment behavior
This might seem like an expedient thing to do under certain circumstances, but such acts almost always come with unintended consequences. When we modify software in unnatural ways, the result is something unique and special for a customer.

Consider what normally happens concurrent to modification. The product team is diligently working on the next release, and it just so happens that a key improvement planned for that release is a complete rewrite of a critical piece of software that cuts the execution time in half. All automated regression tests are passing, so the team decides to move forward with the release. Suddenly, those unique modifications no longer work. What the heck happened?

This is not a case of inadequate testing on the part of the product team — as mentioned, all regression tests were passing. Instead, this is the unintended consequence of accessing and modifying the internals of the product, which happened to change as part of the release. Since the product team has no visibility to modifications done outside the normal development process, it can’t possibly verify that the sum of all modifications will continue to work correctly. Nor should they since the modifications should have never happened in the first place.

A basic, time-honored principle of good software design is _information hiding_. Imagine a box. On the outside is an _interface_ that defines (and restricts) what you can do with the box. On the inside is all the machinery conveniently hidden from view. This is like software — we don’t need to know what’s inside the box so long as the box does what it’s supposed to do. However, if the box is opened and the machinery is modified, then it may no longer work as expected.

We see these kinds of interfaces in the physical world all the time. When a steering wheel is rotated left, the vehicle turns left. When a gas pedal is pressed, the vehicle accelerates. When the brake pedal is pressed, the vehicle stops. All of these are examples of interfaces, or contracts, between you and the vehicle. We don’t really know how the internal steering mechanism works, but as long as the vehicle turns left when we rotate left, life is good.

In the next article, we’ll explore the underlying motivations that lead to software modification.

</div>
