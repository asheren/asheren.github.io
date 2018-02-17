---
layout: post
title: "Ruby Memory Usage Vocab Explained"
date: '2018-02-18'
author: Allison McMillan
share: true
tags:
- software development
- garbage collection
- compaction
- memory allocation
- instructional sequences
---

 
For the past few weeks, I've been pairing with [Aaron Patterson](https://twitter.com/tenderlove) on the work he's doing trying to enable compacting garbage collection in Ruby. It's been really fantastic working together and he recently wrote a [great blog post](https://tenderlovemaking.com/2018/01/23/reducing-memory-usage-in-ruby.html) on the work that's been done. But, garbage collection is a challenging topic that folks feel is inaccessible. I'm sort of obsessed with garbage collection and [breaking down the terms and vocabulary](https://www.youtube.com/watch?v=PzSvAbceTVE) so I wanted to highlight a few of the concepts and words mentioned in his post (and some that aren't in the post but that we've been working with) in a more digestible way.

So what do I mean when I say compacting garbage collection? Currently in ruby, when objects are garbage collected, they can't be moved around, which means they can't be condensed in an optimized fashion in order to free up more of the heap. Compaction enables these objects to be moved around and the references to them (a reference tells you *where* the object is) get updated. A majority of our work so far has been looking at which of these objects can be moved without messing a whole bunch of stuff up and then how to move them and ensure the reference is updated. The terms below are some of the important ones to note and understand when thinking through and solving this issue.

First is IMEMO. IMEMOs are classes that are used internally in ruby. The ruby internals are ruby objects that shouldn't be exposed. In order to ensure that they don't get exposed, iMEMOs are specified as the class type so it's more explicit.

Next is an iseq. An iseq, or instructional sequence, is an object with the type of imemo. Instructional sequences are written in c and are compiled to git Virtual Machine instructions. Instructional sequences are important because they are often pointing or referencing objects like strings or other iseqs that we are trying to unpin or not pin in the first place, so that they can be moved and have their references updated. Iseqs were also quite important to us at this point because a lot of the work we did was to disassemble these instructional sequences on compaction in order to allow them to move.

CDHash. A CDHash is a part of a set of instructions. When the code is compiling, the instruction settings happen last. This means that objects need to stay alive until the instructions are all set and compiled. When a CDHash is garbage collected before the instructions are finished compiling, the entire program crashes. Understanding this fact was vital in debugging an issue that was happening when we were disassembling the instructional sequences.

The final term I'll go into is an embedded array. Through this whole dive in to instructional sequences, we talked a lot about arrays. You can see in Tenderlove's post a whole segment on instructional sequences and how they relate to a mark array which affects memory savings potential by reducing the size of the mark array. Though this, I learned there are embedded arrays and non-embedded arrays. An array is 40 bytes. A normal array points at malloc data with a specific size (and then the array size can grow) but if an array is small enough, we don't want to  allocate any data. If the array has less the 40 bytes of data, then instead of mallocing, we can just store the data in the array itself and then change it to malloc data if the array is more than 40 bytes. When this happens, the elements of the array are embedded inside the array itself instead of in the malloc (memory allocation) meaning it's an embedded array.

Hope this is helpful and allows some of you who are less certain of the complex technical terms to feel like you can dive in and continue to follow our work.
