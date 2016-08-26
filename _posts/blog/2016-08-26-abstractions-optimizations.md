---
layout: post
title: "Abstractions: Optimizations You Shouldn't Know About"
date: '2016-08-26'
author: Allison McMillan
tags:
- software development
- conferences
- learning
- community
- abstractions
---

My next Friday talk was [Aaron Patterson’s](https://twitter.com/tenderlove){:target="_blank"} on “Optimizations You Shouldn’t Know About” and sure enough everything he mentioned was new to me! I don’t think the slides are up yet for this talk either which makes it particularly difficult. See, I think aaron’s talks are great and I always learn A TON, but Aaron talks really fast and goes through stuff at lightning speed. I often end up writing down words or pieces of concepts to google and learn more about later. So here is a collection of random words, phrases, and partial concepts that I learned during aaron’s talk.

Peephole optimization is where you remove useless instructions. Wikipedia says “peephole optimization is a kind of optimization performed over a very small set of instructions in a segment of generated code. It works by recognizing sets of instructions that can be replaced by shorter or faster sets of instructions.”

Case/when byte code is generates a hidden hash and dispatches something but this only happens in certain scenarios.

When looking for optimizations, you want to find the call site. In ruby, the call site is the “.”. For example, in ```hello.world!``` the call site is ```.```. In ```x=foo(Object.new)``` there are two call sites. The ```.``` in ```Object.new``` and an implicit call site on the left of ```foo``` because it is ```self.foo```. Call sites are everywhere.

Ruby VM recap which is important for call site caching. You see the instructions and the stack. Stack-based where the byte code is stored as an array or arrays. In this, you see the operator and the operand. So if the instruction is ```push 6``` and the stack is ```6```, the operator is ```push``` and the operand is ```6```.

Find-method- looking for the method, if it’s not found, then it moves up the stack to find it. Method lookup is an O(n) operation because you BenchMark to check out the speed. The more ancestors there are, the slower the call.

There are also ways to speed up method calls. For example you can cache things that never change. The call cache is a data structure that contains the method lookup and is stored inline with byte code. This is called an inline cache.

Somehow this leads you to be able to look at a hash where they key is the class serial number and the value is the method.

You can tell if the cache is missing by doing ```p Ruby(M.stat)```. If it’s global, the method state should never change.

There can also be runtime breakage, which is where a singleton class access breaks it. The cache  also typically misses new classes or modules.

The session also briefly covered monomorphic, polymorphic, and metamorphic cases. These terms related to the number of types at a call site.

Aaron then touched on measurement of these things saying you need to measure the impact of the cache by measuring the impact of the call sites that are polymorphic and you can do this by logging the method caches.

Finally, in summary, Aaron said that you should only optimize cod that matters and everyone should use polymorphism for better optimization.

Hopefully this summary at least exposed you to some new words and concepts. I’ll let google take it from here.
