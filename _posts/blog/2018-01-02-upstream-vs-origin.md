---
layout: post
title: "Upstream vs. Origin"
date: '2018-01-02'
author: Allison McMillan
share: true
tags:
- open source
- upstream
- origin
- learning
- tricks and tips
---

Upstream vs. origin. There are lots of things that are scary or intimidating about contributing to open source. One of my goals for this year is to be less afraid and utilize open source to increase my skillset and sharpen the knife, if you will. This past week I paired with Adam Cuppy and one of the first things we talked about was upstream vs. origin. See, I've always been a little confused about upstream vs. origin because it seems to me that the only time you ever really use upstream is when contributing to open source. In my regular day to day workflow as a developer, I use origin, branches, etc. so I'm pretty comfortable with git but WHAT THE HECK is upstream and if I do it wrong, will I mess up someone's entire repo? Will they hate me forever?! The good news is no!!

When we're looking at upstream and origin, we're basically just looking at working with 2 different remote origins, one origin and one upstream. Upstream is the original repo. When you commit to open source, you often fork the repo and then clone that repo locally, so you need to set 2 remote origins. You need ot set upstream to the original repo so that you can rebase and make sure to keep up to date with any changes that happen there. And then you also need ot set origin which is your fork of the repo. Setting the origin to your fork is just like a regular workflow… you want to set the origin so that when you push, pull, commit, etc. you're doing so from your copy of the repo. And now here's the best part… you will always have pull access but not push access to upstream. It only ever acts as the root so we can make sure to be keeping up with the MOST recently updated version of THEIR master. This also means that because you don't have push access, you really can't F anything up.

Just knowing all of this information makes me so much more comfortable with the idea of contributing to oepn source and gives me a much better understanding of both upstream and origin and why we use both remote origins when contributing to open source.
