---
layout: post
title: Blog
topic: CTO Perspective - The Folly of AI Producing Lots of Code
date: 2024-09-09
---
<div class="content" markdown="1">

I was prompted to write this article after listening to a recent radio advertisement from IBM touting its [watsonx Code Assistant](https://www.ibm.com/products/watsonx-code-assistant) technology. Something troubling in the voice-over caught my attention. The gist of the pitch was that companies will need to **write lots of code** and that Code Assistant could help.

To be fair, the narrative of generating large quantities of code with greater velocity is not exclusive to IBM. These claims are being pushed in some shape or form by every technology company with LLM-based coding assistants. Whether or not those claims can be validated, usually in the form of productivity improvement, is not really what weighs on my mind. On that note, there seems to be a growing contingent of software engineers repudiating some of the productivity assertions made during the early days of generative AI, but that is a topic to explore another day.

What gives me heartburn is this notion of *writing lots of code*. If we put aside generative AI for just a moment, think about that statement in the context of humans. A software engineer writing lots of code is not necessarily making productive contributions. In fact, there is plenty of evidence over the past four or five decades indicating quite the opposite. Emphasizing the generation of more code may unwittingly prioritize *output* over *outcome*.

Suppose we accept the premise that coding assistants will not only *write lots of code* on our behalf but also that the volume of code is perceived as a good thing. The problem is that all code requires maintenance, and that means added cost to the business. We can think of the cost of maintenance as being directly proportional to the size of the code base. More code in inventory means higher operating costs. I previously wrote about the [paradoxical nature of software](/blog/2018/04/22/paradoxical-nature-of-software) being both an *asset* and a *liability*, which was inspired by [this post](https://www.cognitect.com/blog/2016/3/17/the-new-normal-protected-asset-or-disposable-inventory) from Michael Nygard. My immediate concern with the marketing of generative AI tools is that our code bases will grow significantly faster than our ability to maintain them.

Rather than *writing lots of code*, what we really need from AI-based coding assistants is to **solve problems faster**. In other words, prioritize *outcome* over *output*. This does not imply that such tools should not be generating code, just that the primary objective is solving a problem rather producing code. The best AI tools will be those that can reason about the structure and meaning of code, and then take *reductive* steps, such as refactoring to simplify and eliminate code while preserving correctness.

Yes, actually reduce the size of the code base!

</div>
