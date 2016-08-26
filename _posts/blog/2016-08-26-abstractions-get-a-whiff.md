---
layout: post
title: 'Abstractions: Get a Whiff Of This'
date: '2016-08-26'
author: Allison McMillan
tags:
- software development
- conferences
- learning
- community
- abstractions
---

Friday morning started for me with [Sandi’s](https://twitter.com/sandimetz){:target="_blank"} talk on code smells and refactoring entitled [“Get a Whiff of This”](https://speakerdeck.com/skmetz/get-a-whiff-of-this){:target="_blank"}. Sandi started by talking about a bunch of different code smells starting with bloaters. Bloaters include long methods, large classes, data clumps, long parameter lists, and primitive obsession. They are basically things that do not need to be that big. The next code smell type is tool abusers. this includes switch statements (conditionals), refused bequest (inheritance-related), alternative classes with different interfaces, and temporary fields. Tool abusers means that these things can be beneficial but these code smells misuse them. Then we have change preventers which are things that make your code  really difficult to chance in the future like divergent change (things that should be the same but are different), shotgun surgery, and parallel inheritance hierarchies. Next are the dispensable or the things you can do without which includes lazy class, speculative generality (adding something to a feature before it’s requested), data class, and duplicated code. And finally we have couplers which glue objects together. These are things like feature envy (sending more messages to another object than to yourself), inappropriate intimacy (sending messages from private methods), method chaining, and middle man.

Then we moved into discussing refactoring. When refactoring, you want to alter the arrangement of the code without changing the behavior. The nice thing about code smells is that every code smell has a recipe for fixing it.

From here, i’ll honestly refer you again to [the slides](https://speakerdeck.com/skmetz/get-a-whiff-of-this){:target="_blank"} because Sandi’s examples are always excellent and are documented so clearly visually. This is always the point in her talks where I fin it MUCH more valuable to put down the pen, stop taking notes, and just watch the magic happen.

I will say at the end she did mention a few tools for looking for code smells in your code, the main one being [reek](https://github.com/troessner/reek){:target="_blank"}.
