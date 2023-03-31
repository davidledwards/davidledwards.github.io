---
layout: post
title: Blog
topic: Understanding the Various Types of Software Customization
date: 2023-02-23
---
<div class="content" markdown="1">

Original article published [here](https://engineering.vendavo.com/understanding-the-various-types-of-software-customization-ff45092f78ac) as part of the [Vendavo Extensibility Series](https://engineering.vendavo.com/extensibility/home).

This is the first in a series of articles surrounding software customization and the perils of venturing down treacherous paths. It is a meaty subject for sure. Our objective is to focus on the software side of customization, essentially designing better products that enable these kinds of things without incurring the oppressive downsides of traditional approaches.

In an ideal world, there is no customization. Some of our readers may be in violent disagreement right now. And perhaps they should be. However, it raises an important question that requires closer examination — _what exactly do we mean by customization?_

The semantics are critical. Many enterprise software companies serve industries with large customers and complex business processes that require some degree of _customization_.

If you ask five people to define _software customization_, you will almost certainly receive five different answers. The underlying motives of customization are grounded in the reality that enterprises practice their business processes in different ways. Hence, the need for software to adapt is mission critical to success.

_Adaptability_ is the operative word. If you purchase a piece of software, it needs to adapt to your environment in ways that are unique to you. Customizing software is one means of adaptability, but adaptability does not necessarily imply customization. There are other ways of solving the adaptability problem, such as _configuration_ and _extension_.

The term _customization_ deserves a concrete definition. Rather than explaining through the lens of a software practitioner, let’s use an analogy that resonates with virtually everyone — vehicles.

If you purchase a vehicle online, you have an opportunity to customize the final product. Even though we use the term _customize_ in this context, what you’re actually doing is _configuring_ the vehicle by making a finite set of decisions with a finite set of choices. These choices are very intentional on the part of the designers and considered well in advance. In contrast, the designers will not allow you to make arbitrary modifications of the internal workings, such as the engine, transmission, or computers. Doing so would introduce all sorts of quality control challenges and operational complexities.

Let’s continue with the vehicle analogy to explain another kind of customization. After purchasing the vehicle, you drop by the local bicycle shop to _extend_ the utility of the vehicle by mounting a rack on the top rails. Even though a third-party produced the bicycle rack, by conforming to a rail specification published by the vehicle designers, it happens to fit nice and snug. This means you can shop among many third-party suppliers to find the rack that is right for you.

We briefly mentioned two forms of customization — _configuration_ and _extension_. Let’s look at them more closely in the context of software.

_Configuration_ → A finite set of choices that control the behavior of the software.

The software is fully aware of the choices and will modify its behavior based on the configuration. In principle, all configuration combinations can be tested and verified during development.

Examples:

- Choose small, medium, or large icons
- White labeling
- Approval workflows

_Extension_ → A specific behavior of the software with an infinite set of choices.

The behavior at an abstract level is known to the software, but the implementation itself is unknown. The implementation is supplied by a party other than the software designers. Done properly, the software architecture imposes tight constraints that preserve the integrity of the core.

Examples:

- Domain-specific languages
- Bring your own AI model
- Exit points and service provider interfaces

In the next article, we’ll talk about another type of customization that happens more often than not, an insidious type that leads to all sorts of unfortunate tradeoffs.

</div>
