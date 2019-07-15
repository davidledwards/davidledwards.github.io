---
layout: post
title: Blog
topic: The Paradoxical Nature of Software
date: 2018-04-22
---
<div class="content" markdown="1">
#### Software is a strange thing

Companies rightfully classify the software they create as intellectual property. Those trade secrets, which originate in the form of source code, are compiled and packaged into products and solutions that fulfill some buyer need in the markets for which they compete. In the purest sense, software is the materialization of knowledge.

It seems pretty clear from this perspective that software is an **asset** to companies.

The unfortunate reality is that software can also be a **liability**.

How can this be true? Imagine a fresh loaf of bread resting on the shelf at your local grocery. The owner knows that a potential shopper will purchase the loaf of bread so long as it remains fresh. Hence, she views the loaf as an _asset_. However, once the date of expiration passes, her chances of selling the bread dwindle to zero. That same loaf of bread is now a _liability_.

Software sort of works in the same way. It decays over time for a variety of reasons, shifting what was once an _asset_ into a _liability_.

#### Let me tell you a story...

In the early 1990s, I spent a number of years building middleware for a health care software company that was moving to a client-server architecture. At the time, there were very few commercial options, and even so, most of them were prohibitively expensive. So, the company developed its own middleware software and was considered a pioneer among health care technology companies. This was clearly an _asset_ to the company.

But, then something happened. The open source movement in the latter part of that decade ushered in a plethora of free middleware options, which consequently drove down the cost of commercial offerings. Almost overnight, that same middleware became a _liability_.

#### Liability of software pertains to a cost-benefit inversion

The _benefits_ of building proprietary middleware in the early 1990s outweighed the _costs_ of developing and maintaining the software. When that relationship is inverted, i.e. the costs outweigh the benefits, the asset becomes a _liability_. This is one of the primary reasons companies open source what many might consider intellectual property. They understand that by allowing the community to drive direction and development of said software, the liability is removed from their balance sheet.

In virtually all cases, the software in question is not a core competency of the business. As you can imagine, most open source projects are oriented around technology–web servers, application frameworks, databases, messaging systems, development tools, and so on. This commoditization of technology is a form of software decay, inverting the cost-benefit relationship and shifting likeminded intellectual property from _asset_ to _liability_.

#### What is meant by liability?

When you suddenly realize that the _benefits_ of any give piece of software are overshadowed by the _costs_ associated with maintenance, you have a _liability_ on your hands. The time and money that would otherwise be directed towards market-differentiating development is instead being spent on the maintenance of software that no longer yields the expected benefits. This is the reason companies no longer build middleware systems today, an example which may seem intuitively obvious, but in the 1990s, this was not so evident.

The big challenge for most organizations is detecting when and where the liability exists in the software. Our natural tendency is to protect past and future investments because of the inherent belief that software is always considered an _asset_.

#### To minimize liability is to actively throw away code

Yes, you read that correctly. Tossing code in the bin can be a good thing. This sounds counterintuitive and perhaps borderline heresy.

The point here, of course, is not to espouse the gratuitous disposal of code for the sake of reducing liability, but rather to eradicate portions of software that are primarily only increasing maintenance costs.

In the late 1990s, the general consensus of the software industry was that the annual cost of a single line of code was $4. I have no idea what that cost might be today, but I doubt the number has decreased. In principle, reducing the size of the code base reduces the cost of maintenance.

#### Design for disposability

The important lesson in all of this is that we should write code to be **disposable**.

This means designing modular architectures where components can be easily replaced. We have 50 years of empirical evidence in the computing industry suggesting that software does indeed decay as time passes. By embracing this fundamental truth, the most prudent thing we can do is design software systems with the expectation that portions will be thrown away in the future.
</div>
