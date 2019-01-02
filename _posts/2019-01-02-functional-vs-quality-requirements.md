---
layout: post
title: David Edwards / Blog
topic: Functional vs Quality Requirements
date: 2019-01-02
---
The photograph below is a stunning view of the [Taipei 101](https://en.wikipedia.org/wiki/Taipei_101), a
skyscraper located in the heart of Taiwan. During a business trip to Asia in 2006, I had an opportunity to
tour the building and learn more about the structural attributes not evident to the casual observer.

<img src="/images/taipei-101.jpg" width="70%"/>

Since Taiwan sits squarely on the [Ring of Fire](https://en.wikipedia.org/wiki/Ring_of_Fire), the design of
such a skyscraper would need to withstand frequent and sometimes violent earthquakes as well as strong winds
that accompany typhoons. The architects decided to incorporate a
[seismic damper](https://en.wikipedia.org/wiki/Tuned_mass_damper) which is essentially a very heavy spherical
object suspended near the top of the building. A damper counteracts the forces of mechanical vibrations caused
by high winds and earthquakes, thus preventing the building from swaying or even encountering a complete
structural failure. Interestingly, during construction of the building in 2002, a time in which the damper had
already been installed, it survived a 6.8-magnitude earthquake without incurring any damage.

Why do I tell this story?

Much of what we observe when looking at a building are the _functional_ characteristics, such as how we might
move about the building using elevators and stairwells, the manner in which space is divided to accommodate
tenants, the location of entries and exits, and so on and so forth. What often goes unnoticed, though, are
more subtle but important features, such as redundant power systems, security systems, intelligent elevators
that optimize traffic flow, and even systems designed to avoid structural failure when earthquakes occur.

Analogous to the physical world, software systems also have these so-called _quality_ (or nonfunctional)
requirements. As a point of clarification, I tend to avoid the term _nonfunctional_ despite its prevalent use
because it does not adequately capture the essence of quality, and further, it implies that these attributes
are not functional. Nonetheless, the terms _quality_ and _nonfunctional_ are pretty much interchangeable.

The distinction between a functional requirement and a quality requirement follows...

_Functional_ requirements describe what a system should **do** (a capability).

* A user should be able to set target prices.
* A user should be able to define custom rules.
* A user should be able to find products using image search.

_Quality_ requirements describe what a system should **be** (a property).

* A system should be available 99.9% of the time.
* A price lookup should complete in less than 50ms.
* A system should be free of all medium-to-critical security vulnerabilities.

The primary purpose of this blogpost is to emphasize the importance of capturing quality requirements in
addition to functional requirements.

Why?

... because quality requirements influence the choices we make in software design and architecture. To
illustrate this point, a highly-available system targeting 99.99% uptime (52 min/year of downtime) would
likely have a much different and more expensive architecture profile than a system requiring only 99% uptime
(88 hours/year of downtime).

The subtle yet salient insight in this example is that a concrete understanding of quality requirements will
help product teams avoid the dreaded over- or under-engineering of systems. For example, if the target market
for an application could tolerate 99% uptime, but the engineering team designed a system to achieve 99.99%
uptime, then there is a good chance the application could have gone to market sooner with a less expensive
solution. Likewise, designing a system for 99% uptime when the market unilaterally demands 99.99% could result
in potentially disastrous consequences.

Bear in mind that quality requirements often change with the passing of time. In the prior example, early
adopters of a new product may accept 99% uptime in exchange for the benefits of early access, but as the
product matures and penetrates a larger swath of the market, expectations of uptime may ratchet up to 99.99%.
Product teams need to recognize when these shifts in quality requirements occur and be prepared to respond
accordingly, which might mean rewriting parts of the system.

There is usually a necessary but healthy friction that exists between the business--which argues for
_doing the right things_ (functional)--and product engineering--which strives to _do things right_ (quality).
Balance is critical. If time-to-market is paramount, then relaxing quality requirements may be in order. But,
if that is done at the expense of mortgaging future product agility, then the scales of balance ought to be
questioned.

Despite what may seem to challenge conventional wisdom, rewriting portions of a software system is perfectly
acceptable so long as the potential for those future investments are well understood when compromises are
made. Consider the fact that many consumer-facing startups consciously do things that would make any
self-respecting engineer feel dirty, but keep in mind that those decisions are done in the context of
capturing market share with complete awareness that time will be spent rewriting parts of the system in the
future.

One way in which engineering teams can insulate themselves from the inevitable software refactoring that
occurs due to the accrual of technical debt is by embracing _evolvability_ as a quality attribute. The
fundamental idea is that if a team knows that portions of a system will change over time, then they should
design that system to facilitate change.

The crucial takeaway is that Product and Engineering should be discussing _quality_ requirements along with
functional requirements. It is a conversation for which both parties should fully comprehend the associated
tradeoffs. While Product would typically represent the functional dimension, Engineering should be eliciting
quality attributes based on the needs of the business.
