---
layout: post
title: 'Abstractions: Elixir Session'
date: '2016-08-23'
author: Allison McMillan
tags:
- software development
- conferences
- learning
- community
- abstractions
---

This past week, I had the pleasure of attending Abstractions. Sold out at 1500, it wasn’t a language specific conference which enabled me to attend lots of different sessions and topics. The people were great, the conference was packed and the organizers did a fantastic job! As a caveat, again, these are all notes from the talks I attended so my apologies advance if some write-ups are more clear than others.

### The first of many


The first talk I went to was one by [Jose Valim](https://twitter.com/josevalim?lang=en){:target="_blank"} on [Exploring Elixir](http://elixir-lang.org/){:target="_blank"}. I haven’t had a chance to play around with elixir at all yet but had heard a lot about Elixir and phoenix and know a fair amount of companies that are starting to move in this direction. I figured this would be a great intro into some of the key terms and vocabulary used. Part of the focus was on the fact that Elixir is great for building concurrent applications. Concurrency means a bunch of processes that are isolated and every time they change information, the process needs to send that information. In Elixir, every process has a supervisor so that what is going on in one process doesn’t affect the other process. Processes can be things like stats, mailers, etc. that package and run our code. They can also be started and stopped. Processes have supervisors and both are packing into applications. Then the message passing is how the processes communicate.

Jose used the elixir REPL (which is like IRB) to show us a few things. He talked about how things are named obviously which is helpful and that you can run an observer that will then show you all the information you’re looking for. Opening up the tools for discovering all of this information, you can look at nodes and even use the UI to kill nodes in order to see what will happen. For example, when you kill a node, the pool will notice something is wrong and will start a new process. These applications give us visibility into the state, introspection and monitoring abilities, and make it each to break aspects into components. All of this means Elixir applications are concurrent, allow developers to fail fast, and fault tolerant.

He mentioned the goals of the language were compatibility, accessibility, and productivity. Compatibility means that you can call Erlang from elixir, for example, without an issue. Accessibility means there will be a tool for making more tools of the same kind, like writing tests or a library that writes queries using Elixir. Productivity means that everyone has a good programming experience resulting in priorities like good error messages, documentation, good tooling ([Exunit](http://elixir-lang.org/docs/stable/ex_unit/ExUnit.html){:target="_blank"}, [Mix](http://elixir-lang.org/getting-started/mix-otp/introduction-to-mix.html){:target="_blank"}, and iex were mentioned specifically), and hex package management.

From there, we did a quick demo app. Here are some highlights. You can clear error messages in tests. Documentation is write-in markdown. The framework can take documentation and write a test for it. [Alchemist]( http://www.alchemist-elixir.org/){:target="_blank"} is a toolkit for writing code (demonstrating the types of tools that are starting to exist in the community). Finally, to get started with Elixir go through the [“getting started” guide](http://elixir-lang.org/getting-started/introduction.html){:target="_blank"}.

