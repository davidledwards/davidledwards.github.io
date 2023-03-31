---
layout: post
title: Blog
topic: Underlying Motivations for Customizing Software via Modification
date: 2023-03-10
---
<div class="content" markdown="1">

Original article published [here](https://engineering.vendavo.com/underlying-motivations-for-customizing-software-via-modification-70c12753dcbd) as part of the [Vendavo Extensibility Series](https://engineering.vendavo.com/extensibility/home).

In the prior installment on software customization, we talked about [modification as a particularly insidious kind of software adaptability](/blog/2023/03/02/insidious-type-of-software-customization). If you have not read this article, we would suggest taking a few minutes to familiarize yourself with the concept of modification.

At the core, _modification_ violates the fundamental principle of information hiding, a time-honored pillar of modular software design that improves comprehension, facilitates test automation, and promotes the evolvability of systems. Without strict adherence to a discipline of information hiding, software systems become increasingly unmaintainable as they grow in size and complexity.

It turns out that we have much better ways of making software adaptable to customer environments without compromising the principle of information hiding, namely techniques like _configuration_ and _extension_. However, these mechanisms demand proper analysis and development by product and engineering teams because each requires some degree of generalization to make them applicable to a broad range of customers.

If these techniques are indeed superior, then why do organizations resort to software modification? The underlying reason usually boils down to _time_. And this typically stems from an explicit or an implicit promise. A promise itself is not necessarily the problem, but rather the manner in which that promise is fulfilled. The means of fulfillment depends largely on the prevailing culture and historical behavior.

Let’s examine both ends of fulfillment.

On one end of the spectrum, an organization may be predisposed to doing whatever it takes to make a customer happy. And that often leads to customizing software via _modification_ due to time constraints attached to an implementation project. While the motivations may be well-intentioned, the end result is almost always an unhappy customer grappling with quality problems.

On the other end of the spectrum, an organization may be inclined to engineer every capability into the product itself. And that usually means that any kind of customization is done around the edges via architectural approaches like _configuration_ or _extension_. The implication is that the absence of any desired capability in the product would not be placed in the critical path of an implementation project but rather incorporated into the product roadmap.

Along that spectrum, you can see the existential dilemma that is largely predetermined based on history and culture. You either:

- Move fast and please every customer at the expense of quality; or
- Move deliberately and please most customers at the expense of speed.

The former describes what we typically characterize as a services-centric company whereas the latter denotes one that is product-centric. In reality, most companies find themselves oscillating around in the middle of this spectrum as opposed to being rigidly anchored on either end. Vendavo, in particular, has been on an aggressive journey in recent years to shift our gravity towards the product end of the scale.

In the next article, we’ll discuss some of the unintended consequences of software modification. These are the real and often hidden costs associated with customization that extend well beyond project implementations.

</div>
