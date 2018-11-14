---
layout: post
title: David Edwards / Blog
topic: Elements of Software Design
date: 2018-11-13
---
I recently stumbled upon a book on software design so enthralling that I essentially read the entirety of the
text in one sitting. To be honest, there were a few dry sections perhaps worthy of skimming, but in general,
the author did a fantastic job of capturing my attention. Coincidentally, this is also a topic for which I
have long felt compelled to write about at some point in retirement, but it seems I should now find a
replacement on my bucket list.

[A Philosophy of Software Design](https://www.amazon.com/Philosophy-Software-Design-John-Ousterhout/dp/1732102201),
by John Ousterhout, is a book about the fundamental problem of software design, _problem decomposition_,
which relates to how systems are broken into pieces for the purpose of comprehension. Sounds easy enough, but it turns out to be one of the most perplexing challenges in the software profession.

In software development, _complexity_ is your enemy. And, the appearance of our beloved _technical debt_ is
often attributed to the accrual of complexity over time. This gives us a primal understanding of the origins
of technical debt. Effective problem decomposition is the way we address complexity and build comprehensible
systems, thereby preventing the accumulation of technical debt.

What do we mean by software complexity? In simple terms, complexity relates to the structural properties of a
software system that make it difficult to understand and modify. Structure refers to the pieces and parts and
how they interact with each other, similar to the way you might think of the design of a building.

Considering that virtually all software products have a lifecycle measured in years, often decades in the
enterprise space, the degree of complexity determines how easily engineers, both today and tomorrow, can
comprehend and extend those systems.

The author makes several very insightful statements throughout the book, one of which is this idea that
software engineers should adopt a _strategic programming_ mindset. As opposed to _tactical programming_,
which is primarily focused on developing the next feature, a strategic approach instead shifts attention to
_facilitating future extensions_ of the software. In essence, engineers should improve the structure and
design of a system with each modification. Obviously, features continue to be an important outcome in
strategic programming, but the author suggests that preserving or enhancing the design of the system should be
the first-order concern, as doing so enables future extensions of the software.

The other important observation noted by the author is that
[agile software development](https://en.wikipedia.org/wiki/Agile_software_development) often leads to a
tactical programming mindset, largely because the emphasis of an iteration is oriented around delivering new
features. This observation is quite nuanced because the rationally-minded person would fully agree with the
goal of incremental feature delivery. However, what usually happens as a consequence is that important design
decisions get deferred due to short-term interests, which then leads to the accrual of complexity over time.
And, of course, we already know complexity is your enemy. His suggestion is that engineers should instead
think of iterative development in terms of _increments of abstractions_ rather than increments of features.
This mindset shift embraces the idea of enabling future extensions and leaving the software in a better place
after modifications.

Rather than risk repeating the eloquent words of the author, I would highly encourage anyone directly
involved in the development of software include this book on their reading list.
