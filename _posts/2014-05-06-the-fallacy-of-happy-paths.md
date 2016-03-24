---
layout: post
title: David Edwards | Blog
topic: The Fallacy of Happy Paths
date: 2014-05-06
---
In the circles of software projects, it is not uncommon to hear people distinguish between _happy paths_ and _exception paths_ in relation to activities such as development or testing. The unfortunate consequence of drawing such a distinction is that human behavior will tend to establish a bias, typically in favor of happy paths, even though systems and machines have no means of discriminating.

![Happy Path](/images/happy-path.png "Happy Path")

So, this leads us to believe that exception paths are so rare in practice that they somehow deserve to be treated like second class citizens. We promptly cast aside equivalent investments in unit and integration testing with the false notion that the improbability of exception paths somehow implies that the consequence of such events is equally insignificant. However, all of us have seen at some point in our lives the unfolding of catastrophic system failures whose root causes can be traced back to false assumptions about the probability of exceptional events. I would urge developers to reconsider the notion of classifying execution paths and instead verify the correctness of systems under all conditions, happy or exceptional.
