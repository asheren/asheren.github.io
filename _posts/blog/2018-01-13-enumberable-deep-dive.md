---
layout: post
title: "Enumerable Deep Dive"
date: '2018-01-13'
author: Allison McMillan
share: true
tags:
- enumerable
- learning
- refresher
---


Related to my post from Ruby Conf. I've been working on trying to fill in some of those knowledge gaps I have. I created a cirriculum for myself to keep myself on track, and enlisted a few friends to keep me accountable, answer questions, and review pieces of code. So far, so good! I'll share the things I've been working on as I go along (hint: one is a really awesome code confidence mapper which will probably take me forever to "complete" with my current time constraints but it's still REALLY fun to work on). Part of this week's challenge was a deep dive in to enumerable, one of the most useful classes in Ruby. While I "know" enumberable methods, understand what they do, and write them as a developer, I didn't feel like I understood the methods inside and out. While this may be basic for some folks, it's helpful for me (and maybe others?) to recap what I've learned (or refreshed).

As a sidenote, I found a super helpful [enums-exercise]() from the Turing School which was truly great for working through these. The repo has you work through each method in terms of `each` which really breaks down the concept and then has you execute the example using the enumerable method. A friend also wrote a few more tests for me based on additional methods I wanted to practice and I wrote a few more tests solo.

`Map`: The map function transforms. It takes each items and does _something_ to it according to what's in the block
`Select`: The select function filters. It takes each items and determines if it meets the criteria in the block. Select will return an array of items.
`Find`: Find takes each item and also filters but finds only the first. Array also has a first method which is very similar. Find will return the first in the same "type" (ie- if you're looking for a string it will find a string, etc.)

`&:method` This syntax is used all the time but I never quite "got" it. This syntax is a reference to a method. For each value, you are referencing (not calling) the method which is actually giving the instructions for when the transformation is happening. This is sort of like `on.click, @function name` when you're setting up handlers in JavaScript. So, for example, you're saying to the code, please call this method when you are actually looking at the specific value, inside the map

Here's a code example:
```
tripler = NumberTripler.new(5)

tripler.triple # 15
tripler.send(:triple) # 15
[tripler].map(&:triple) #[15]
```

The above are all ways of getting to the same block of code (map being with tripler as an array because map is an enumerbale method which needs an array)


`.with_index`: with_index can be used with any of the enumberable functions. It's often used with ordering. You can also use it with a select dropdown. And `with_index` is especially helpful with files, spreadsheets, data, etc. which doesn't have an id (ie- a user id), the index will take that place so you know exactly what row (for example) you're looking at.

`index_by`- index_by will take an array and turn it into a hash and index it a specific key
the way the database is understanding things is different from how you want to show it to users. so you need ot transform the info that's in the database so it is a certain way for how the user will actually see it. saem data but restructured.

`&` is intersection. It looks through 2 arrays and finds any items that is in both arrays.

`|` is a union. It joins together 2 arrays and gets rid of any duplicates.

