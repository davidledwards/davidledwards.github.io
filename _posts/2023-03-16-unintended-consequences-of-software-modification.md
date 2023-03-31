---
layout: post
title: Blog
topic: Unintended Consequences of Software Modification
date: 2023-03-16
---
<div class="content" markdown="1">

Original article published [here](https://engineering.vendavo.com/unintended-consequences-of-software-modification-f19b3ca8878a) as part of the [Vendavo Extensibility Series](https://engineering.vendavo.com/extensibility/home).

The most recent article on software customization brought attention to an [underlying motivation](/blog/2023/03/10/motivations-for-software-customization) that often leads to software _modification_ as opposed to other product-friendly approaches, such as _configuration_ and _extension_. That motivation is _time_, specifically constraints on time imposed by implicit or explicit promises to customers. This does not imply that organizations necessarily resort to modification when pressed for time, as it depends largely on history and culture, but it does tell us that those engaging in this behavior are very often driven by promises and timelines.

One important distinction to underscore is that sometimes the _promise_ is not necessarily constrained by time but rather its general applicability to the product itself. For example, if a feature is unique only to a single customer, the product team may not have a justifiable business case that would warrant the investment required to develop such a feature. Imagine building a unique feature for 100 different customers. The product would quickly become unwieldy and unmanageable.

As good as our intentions might be, software modification usually leads to downstream problems that negatively impact the business. To be clear, we’re not talking about companies whose primary business is developing custom software; we’re talking about companies whose core business is building and selling SaaS products.

Let’s explore some of our top picks in the category of unintended consequences.

**Future product releases may fail**

If a product team does not have visibility to software modifications, it is impossible to guarantee that any such modifications will not fail at some point in the future. A product team has an obligation to preserve the syntax and semantics of external interfaces, such as APIs, but they have no such obligation when it comes to internal changes. It is not uncommon for a team to continuously change internal structures and behaviors as the product evolves. We spoke about this in prior articles — modifying software means changing something about the internal apparatus. If the product team is unaware of those changes, then the probability of failure dramatically increases.

**Modifications need maintenance and support just like products**

There is really no such thing as source code that lives in a static state. Static software decays over time and eventually becomes a liability. If software is your business, then the software is constantly changing and evolving. Even so, there are all sorts of external forces that require maintenance and support, such as technology retirement, security flaws, and so on. Software modifications are usually done as part of a project implementation, so the teams making those changes are not typically maintaining and supporting that code once the project ends.

**Erosion of quality**

The notion of quality erosion can surface in a variety of ways. One of the most obvious examples is poorly tested code that manifests in the form of failure. It could be a failed job, loss of data, UI errors, and so on. Software modifications made during project implementations almost never face the equivalent rigor of normal engineering processes that one would expect as part of product development. The primary reason is how we measure success — product teams are driven by quality and correctness whereas project teams are usually focused on time and budget. Another illustration of quality erosion is performance degradation caused by unexpected computational loads competing for the same set of finite resources. A classic example is the seemingly innocuous act of attaching triggers to database tables.

**Handoffs lead to significant knowledge loss**

When software is modified during a project implementation, the resulting source code and its essential knowledge is often handed to another organization for support and maintenance. As much as we try to maximize the capture and transfer of knowledge, the harsh reality is that much of it drops to the floor. The team supporting the code is not the team that made the modifications. This starts to become a huge problem especially as the number and complexity of modifications accrue over time.

**Product teams end up diagnosing problems**

When failures occur in software modifications, such as when a new product release is deployed, it may not be obvious where the problem exists. From the customer point of view, a failure is a failure, so the nuance of origin is an internal point of distinction only. At the end of the day, the software needs to be fixed. What tends to happen is that the time-consuming effort of diagnosis trickles down to product teams, which draws capacity away from doing other things. From a pragmatic point of view, this gravitational pull towards product makes sense — without proper diagnosis, it would be hard to determine if the problem was in the core product or the software modification.

There are certainly other unintended consequences that we may have missed, but central to all of them is that the institutional practice of software modification has a real and measurable impact on the business. Modification is a form of _variance_ or _entropy_, and in the discipline of software engineering, we do everything we can to minimize variance because it inevitably leads to complexity, and that can degrade both quality and customer satisfaction.

In the next article, we will be outlining a set of principles aimed at guiding how we recommend designing products with customization in mind. Understandably, these kinds of philosophical and behavioral changes take time to embrace. The first step is anchoring our thinking around a core set of principles that begin to shape future decisions.

</div>
