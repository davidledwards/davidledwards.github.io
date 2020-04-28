---
layout: post
title: Blog
topic: The Diminishing Importance of Releases
date: 2020-04-28
---
<div class="content" markdown="1">
One of the notable carryovers from the days of building on-premises enterprise software is the concept of a **release**. I would argue that widely held beliefs regarding the importance of a release are rooted in tradition and require rethinking in the age of cloud-native software products.

In a very general sense, a release is essentially a bundle of software artifacts that, when installed and configured, provide a set of features and capabilities to users. Each subsequent release often includes new features that distinguish itself from the prior release, ideally in a value-differentiating manner, thus creating a reason to upgrade whether done by carrot or by stick.

And so, we have become accustomed to associating the availability of new features with a release. In other words, the release is the mechanism by which features are distributed to users. It makes complete sense especially in the context of software that gets bundled and shipped by one set of actors, then deployed and configured by another.

As companies move from long cycles of waterfall-style development so prevalent in the age of on-premises software towards shorter cycles of continuous delivery in the age of true software-as-a-service, the historical significance of _the release_ begins to break down.

Most users care little or nothing about software releases. What they care about is the availability of features that provide value. When is the last time you checked the version of Gmail or Office 365? Do you really care? Likely not. Are you aware that Google and Microsoft are releasing new versions of these products many times per day? Does that make you think differently about these products? Of course not.

In a world of always-on software products, it turns out that a release is arguably important only to engineering and operations teams, not customers and users. I know, I know, some of you will vehemently disagree with this assertion, but please read on.

You can think of a release simply as a unit of deployment, hence its importance to engineering and operations. In a world of continuous delivery, or even the holy grail of continuous deployment, releases are often much more frequent and usually contain small increments of change. It could be a small bug fix, a performance improvement, a slight tweak to the UI to work with the latest version of Safari, or even something more visible to users.

A release in the context of software products with long development cycles can be seen as an accumulation of many changes, hundreds or perhaps thousands, that in aggregate are comprised of only a handful of features important to users. This is the reason the release was so important to suppliers and customers. It was a convenient means of referring to the bundle of anticipated features. Something like, _version 10 will ship with this widget and that widget_.

When the cadence of releases becomes much more frequent, the accrual of change tends to zero. Most of those changes are unimportant to users in the sense that they would necessitate awareness. It is only when important features become available that customers and users should be informed.

All of this is leading up to the central argument that we should discontinue the use of releases as the mechanism for introducing new features to users. In essence, the deployment of software should be entirely decoupled from enabling the features that accrue through those releases.

The availability or enablement of features should instead be orchestrated through software apparatuses, for example, using logical switches or other similar predicate-based mechanisms.

What are some of the benefits of this decoupling?

First, enterprise customers usually want controls that enable new features for end users. In a software-as-a-service delivery model with multi-tenant deployments, releases no longer work as an appropriate gating mechanism. A higher-order abstraction, like software switches, becomes necessary to provide adequate controls.

Second, imagine you have a new feature in development that is not yet available to customers and users. Software-based controls can be used to grant access to the QA team or perhaps even a limited set of early-adopter customers. This has some seriously attractive advantages for engineering and operations teams. It allows a single production environment to serve multiple constituents–normal users, early adopters, and internal QA teams–reducing both cost and complexity to the service provider.

Third, product teams operating in a mode of continuous integration and continuous delivery no longer need to maintain long-lived feature branches. They simply develop the feature incrementally, continuously committing changes that get deployed into production, and accumulating to a point where the feature is eventually enabled for customers and users.

The shift away from _the release_ as the machinery for enabling features towards software-based mechanisms will certainly require additional work for product and engineering teams. However, the long-term benefits should be abundantly clear. The continued tight coupling between release and feature availability will inevitably hinder efforts aimed at optimizing the continuous delivery of software.
</div>
