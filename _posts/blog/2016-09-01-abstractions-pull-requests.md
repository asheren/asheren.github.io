---
layout: post
title: 'Abstractions: Anatomy of a Great Pull Request'
date: '2016-09-01'
author: Allison McMillan
share: true
tags:
- software development
- conferences
- learning
- community
- abstractions
---

Starting to come towards the end of the conference, [Sean Griffin](https://twitter.com/sgrif){:target="_blank"} spoke about the “Anatomy of a Great Pull Request”. I’m gonna be honest and say that a lot of this stuff seems sort of like common sense to me but it was good information nonetheless. I actually often keep a checklist for when I open a PR to make sure i’m providing the right amount of information to make it easy for anyone looking over my PR to approve it, so I got some great nuggets in this talk to add to that list.

First, when you’re looking to contribute to an open source project, Sean recommends following this process:
1. Read the contribution file
2. Have tests
3. Follow the style guide
4. Write code you’re proud of

Okay, so now into PRs. PRs are actually NOT about code. Make sure to keep the size reasonable. No one has time to review a PR with 10,000 changed lines of code. Then, don’t assume context. Make sure to link to the docs, link to any related sections, and even link to other links or code. When you’re contributing to a large open source project, convince the folks in charge why the problem matters, again, give context to the issue. Then think about how many users will be affected by the fix? how complex is the fix? and is there an easy work around for the issue?

After that, show that your change is the best solution. Explain why you wrote the code the way you did. And remember that features are easy to add but hard to remove. You can also give context in the commit message. Pro tip: if you’re confused about what a piece of code is doing, use git blame to read the commit message from that piece of code (also why you should write good commit messages). As you’re coding a solution, you can also write longer commit messages in order to alleviate the need to put comments the code. But remember, if you squash your commits, amend the commit message.

Finally, remember that your third pull request is when you start to make an impact because it takes time to get to know a codebase, a reviewer, for a reviewer to get to know you, etc. And remember to be nice. Not everything can be merged. Maintainers are working hard to have a clean codebase and sometimes it sucks when they say the PR you worked on actually won’t get merged in. You can be sad, but be nice and the key is empathy.
