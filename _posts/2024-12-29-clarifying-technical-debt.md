---
layout: post
title: Blog
topic: 'Clarifying Technical Debt'
date: 2024-12-29
---
<div class="content" markdown="1">

In the field of software, _technical debt_ is a widely used phrase in the lexicon of practitioners to categorize all kinds of technical problems that are presumably leading to some sort of negative impact on the business. Technical issues can manifest themselves in many ways, e.g. lower productvity, lost sales, poor product experience, and customer churn.

[Ward Cunningham](https://en.wikipedia.org/wiki/Ward_Cunningham) coined this phrase in 1992 when characterizing the inherent tradeoff of shipping products early, essentially accepting _debt_ in exchange for faster delivery. The presumption was that such debt, similar to its financial counterpart, should be repaid sooner rather later, otherwise the future cost of servicing that debt increases.

The analogy to financial debt is undoubtedly useful because, if nothing else, it creates a shared vocabulary between the software engineering discipline and other areas of the business. However, _technical debt_ on the surface is rather nebuluous, as it encompasses such a broad spectrum of technical problems. This lack of specificity invites confusion and often erodes trust outside the circles of engineering.

A fitting comparison would perhaps be akin to saying that a product has _feature_ debt. Conceptually, we understand the essence of this statement, but what exactly does it mean? Is the absence of capability _X_ leading to a reduction in wins? Is a poor user experience in workflow _Y_ leading to heightened levels of customer churn?

Take notice of the prior examples: both of them associate a product issue with a business problem. This degree of clarity mobilizes teams to be intentional about where to invest their finite resources, discussing tradeoffs of doing this versus that. It turns out that _technical debt_ should be tackled in precisely the same way.

A simple yet powerful mental model is to think about software products in terms of features _(what it does)_ and qualities _(what it is)_. This earlier [post](/blog/2019/01/02/functional-vs-quality-requirements) delves into greater detail regarding the distinction between features and qualities.

A critical observation at one point in my career was that all technical debt is associated with the deterioration of one or more software _qualities_. Think of [software qualities](https://en.wikipedia.org/wiki/List_of_system_quality_attributes) as measurable properties of a system: scalability, availability, maintainability, and so on. The key insight from this observation is that technical debt can and should be reframed as quality problems that are negatively impacting the business.

A common planning strategy adopted by many product teams is to allocate some percentage of development capacity to technical debt. This is often, though not always, the result of a compromise reached between product and engineering. The salient word is _compromise_, as such agreements usually point to a deeper problem of distrust stemming from a lack of clarity or a lack of transparency. To be clear, a decision to allocate a fixed percentage of time to address quality improvement is not necessarily a bad idea so long as there is clarity about how those investments will positively impact the business.

An unfortunate consequence of clumping quality issues into the nebulous bucket of _technical debt_ is that organizations outside of software engineering, product management included, are free to interpret as they wish. It is not uncommon for people to equate technical debt with _"the engineers made a bunch of mistakes or bad decisions"_. While that certainly may be true in some cases, it is quite typical to see shortcuts taken during various stages of product development, conscious or not, that ultimately need to be addressed at some point in the future. If you were building a new product and time-to-market was critical, would you insist on extreme scalability for the MVP? _Of course not_. If that product is eventually adopted on a massive scale, will you need to redesign the backend? _Probably so_. A sound technical decision today may indeed be technical debt tomorrow.

I would strongly encourage software organizations to eliminate _technical debt_ from their vocabulary--particularly when it comes to planning--in exchange for clearly articulated quality improvements connected to business outcomes. A few necessary things will happen.

First, organizations will need to decide which software quality attributes are most important to the business. At a minimum, this exercise is a forcing function to clarify what is truly important. Second, those vital few quality attributes must be measured in order to be improved, otherwise teams are simply acting on speculation. Third, discussions begin to shift away from servicing the black box of never-ending technical debt to thoughtful investments in technology improvement that drive better business outcomes.

A practical suggestion is to work backwards starting from business objectives to determine which quality attributes will have the greatest impact. For example, if an objective is being more responsive to market changes by increasing the speed and agility of development, then you probably need to take a closer look at build and deployment automation, and even things like maintainability of the source code.

In a nutshell, decide what product qualities truly matter to the business and measure them. If any of those measures show signs of regression, determine if and when to invest in technology or process improvements.

</div>
