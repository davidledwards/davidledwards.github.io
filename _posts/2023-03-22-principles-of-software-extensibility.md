---
layout: post
title: Blog
topic: Principles of Software Extensibility
date: 2023-03-22
---
<div class="content" markdown="1">

Original article published [here](https://engineering.vendavo.com/principles-of-software-extensibility-ba9cd1d31aaf) as part of the [Vendavo Extensibility Series](https://engineering.vendavo.com/extensibility/home).

In the prior post on customization, we briefly explored some of the [unintended consequences of customizing software via modification](/blog/2023/03/16/unintended-consequences-of-software-modification). There is a very real and debilitating cost to variance and entropy that comes with the practice of modifying software. It has downstream effects that begin to erode quality and make changes increasingly more expensive.

We know for certain that enterprise customers need software systems that can adapt to their business processes. This requirement seems indisputable, yet the manner in which products are designed for adaptability has a profound impact on future speed and agility. Extensible architecture is arguably the best path forward because it protects the evolvability and quality of the products themselves.

This series of posts on software customization ends with the publication of extensibility principles aimed at capturing a core set of beliefs that ideally serve as a guide when designing extensible products. We encourage everyone to take a few minutes to read and absorb these principles.

**Product extension points are business decisions**

The nontrivial cost associated with the development, evolution, and support of APIs for any product requires thoughtful consideration and design with respect to existing workflows. The creation of novel extension points must be carefully considered by business stakeholders and product managers.

**Products should be open to extension but closed to modification**

The essence of the open-closed principle is that products should support the addition of bespoke behaviors without requiring access to or modification of internal state, such as source code and databases. A well-designed product adheres to the principle of information hiding which seeks to make all internal details invisible to external parties and preserves its ability to evolve independently of extensions.

**Products must not expect the presence of any extension**

A product must stand on its own without the introduction of any particular extension. Otherwise, a strong coupling of this sort would imply that any such extension should be part of the core product.

**Extensions must always interact with products through APIs**

Extensions must depend on abstractions rather than implementation details. Abstractions are modeled through APIs and fundamentally serve as a long-term stable contract between the product and its consumers. Any dependence of an extension on internal product details, such as databases and schemas, is a direct violation of the fundamental principle of information hiding and doing so would impose constraints on the ability to support, maintain and evolve the product.

**Design for backward compatibility**

The evolution of API design should be strictly backward compatible with prior generations in order to ensure that both the product and its extensions can evolve independently. API deprecation policies can be used to complement backward compatibility goals by establishing norms and expectations around the lifecycle of older generations of APIs.

**Products must always be responsible for protecting the core**

Since APIs are the points of interaction with extensions and other types of consumers, the product is wholly responsible for not only authenticating and authorizing requests but also proper validation of all input parameters. The existence of any complementary security and validation logic in an extension does not in any way waive the responsibility of the product.

**Standard API and security technologies are preferred**

Products should always prefer the use of industry standards when exposing operations and data to external parties. Standardization affords the reuse and leverage of established approaches, accrued knowledge, and existing libraries, all of which reduces the probability of incorrect implementations. Further, the development of any given extension should also adhere to any applicable company-wide standards and policies.

**Widely used extensions should be integrated with the core product**

The broad adoption of any given extension by a wide group of customers should be considered for inclusion as a configurable, core capability in the product. Doing so follows the natural path of evolution to a point where critical mass triggers a decision to move development of said capability into the main product lifecycle.

**API design should always assume use by third parties**

The design of extensibility APIs should always assume that the development and deployment of extensions are orchestrated by untrusted, third parties, such as partners and integrators. None of the aforementioned principles should be relaxed in any way for internal organizations.

Before we close, it is worth elaborating a bit more on one principle in particular — _product extension points are business decisions_.

The reason for spotlighting this first principle is that extension points are not meant to be a crutch for old behaviors. We are not simply moving insidious kinds of customization from one group to another. Quite the contrary. The intention of an extension point is to model a general problem where the implementation of that problem could have an infinite number of solutions. If a problem cannot be generalized, then it should not be a candidate for extensibility.

We trust that these posts have been informative and insightful. We now have a set of principles that can orient product design behavior going forward. As with anything in life, these principles should be seen as living things that can and will change over time.

</div>
