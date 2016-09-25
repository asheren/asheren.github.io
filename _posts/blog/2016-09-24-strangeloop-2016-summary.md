---
layout: post
title: "StrangeLoop 2016: A Summary"
date: '2016-09-24'
author: Allison McMillan
share: true
tags:
- software development
- learning
- conferences
- community
---

Last week, I had the pleasure of attending [Strange Loop](http://www.thestrangeloop.com/index.html) in St. Louis. Strange Loop is a great conference and one of my favorites for many reasons. First, it’s incredibly diverse… it was the first conference I ever attended where I looked around and saw handfuls of women in the audience. Second, the organizers are fantastic. I brought my 1.5 year old with me this year and we both had a great time. There was childcare provided for both the conference AND pre-conference day and activities like the City Museum opening party were family friendly. Third, it is one of the few non-ruby conferences I attend which means that my mind is stretched in a different way. My Strange Loop agenda is often filled with learnings about scalability, new programming languages, and functional programming approaches to problems. The ability to be exposed to this type of information makes me better informed and gives me a broader perspective on programming and the work I do.

This year, I started StrangeLoop at the pre-conference day attending the first ever [Elm Conf](http://www.elm-conf.us/speaker/). Elm Conf was GREAT! Last year, Richard Feldman gave an amazing [introduction to Elm](https://www.youtube.com/watch?v=FV0DXNB94NE) talk and i’ve been playing around with/keeping an eye on the language ever since. It was really fantastic to get to attend the first confernece. It started with [Evan](https://twitter.com/czaplic) speaking about the language and community… a great way to set the tone. The moved on to [Ossi](https://twitter.com/ohanhi) talking about doing client work using elm and interesting approaches and learnings he’s had through actually using elm in production. Then, there was a talk from [Luke](https://twitter.com/luke_dot_js) about the more human side of programming and elm and afterwards lightning talks. The day continued after lunch with [Joel](https://twitter.com/joelquen) talking about using random in elm through a great example of generating Roman names, [Jeff](https://twitter.com/jschomay) speaking about Storytelling, [Jessica](https://twitter.com/jessitron) talking about a cool new way to use templates which makes programming in Elm EVEN better, and [Murphy](https://twitter.com/splodingsocks) walking us through a music app written in elixir, phoenix, and elm (this is sort of what I want to explore more) that was pretty sweet. The day ended with [Richard](https://twitter.com/rtfeldman) talking about using elm to make it impossible to do things that shouldn’t be done (ie- you should only be able to compile VALID css stylesheets) and a Q & A which I sort of missed because of a small childcare issue. I would have loved to know more about who was in attendance at Elm Conf, and I hope the organizers are able to get information about who in the room is using Elm at work or in production, who is playing around with it, and for whom was Elm Conf their first exposure to Elm. I met some really friendly, awesome people throughout the day which always makes me happy when looking into a new language and I hope the Elm language and community continue to grow in a positive way.

The next day started off with a brief trip to the emergency room for [nursemaid’s elbow](https://en.wikipedia.org/wiki/Nursemaid%27s_elbow)… just one of the side-effects of deciding to bring a kid to a tech conf I guess and so I missed the first keynote. I’m just going to touch on each talk with a sentence or two on what they were about. One of the best things about Strange Loop is that they get the talks up online within days, so you can already check them all out.

[Nicola](https://www.youtube.com/watch?v=sMy4L-J6fFs) speaking about journalism and collecting data to write stories spoke about look at data from a microscopic view, tearing it apart to decide if the information journalists have are able to provide them with a full picture in order to ethically report on an issue. The talk covered a few different stories that have been published over the last few years, went over the data received from these stories, and how that data was collected in order to help the audience determine if the story was a feature (a great story to report on based on the data received) or a bug (a story that maybe had some questionable components when looking at the data and how the data was received).

[Zach](https://www.youtube.com/watch?v=_1rh_s1WmRA) spoke about what information you want to keep in mind when building a server and how to keep the factors in mind when you’re designing a system. His talk has a great example called “the parable of the pumpkin carver” which provides a great example for thinking about resource distribution and load balancing.

[Julia](https://www.youtube.com/watch?v=HfD9IMZ9rKY) who’s excitement is contagious dove into linux debugging tools covering ```strace```, ```wireshark```, ```perf```, ```egrep```, and a few more. Definitely check out this talk and the related zine for some straightforward commands that will help you debug problems faster. We explored the tools above using three mystery scenarios… the first, a missing config file, the second, a slow program, and the third, a website showing up in french instead of english.

[Adam](https://www.youtube.com/watch?v=qCUI5ryyMSE) spoke next about network defense and a need to create trustworthiness in critical systems. He provided some tools and suggestions but his main take-away was that companies, even those who are adversaries, should work together when they experience an attack because if one company is experiencing an attack, it’s likely that a similar company will have the same issue.

Afterwards, [Scott](https://www.youtube.com/watch?v=Rzdxgx3RC0Q) talked about netflix caching. As a fan and frequent user of netflix, it was pretty interesting to learn about the different pieces of the interface that are cached and how. He also talked about some of the architecture, what everything is built in, and how everything connects together.

And then lastly, I went to [Mike’s](https://www.youtube.com/watch?v=pDdE3PKy6mo) talk on Alexa and go. I seem to have not taken many notes (I’m pretty sure I was doing some therapeutic coloring which is really important at the end of a StrangeLoop day). This talk was really interesting though because it went though how modules and components of programs for new tech like Alexa are being built.

The day ended with an incredible keynote from [Ashley](https://www.youtube.com/watch?v=fNe1i7nVbXI). It was really fantastic and I highly recommend you watch it. Numerous times, it caused a lot of the audience to tear up and was really interesting and compelling.

**Day two**

Day two began with [Paul](https://www.youtube.com/watch?v=rWYifOE8LDc) talking about mobile and how mobile web has changed, evolved, and whats coming.

Then [Lee](https://www.youtube.com/watch?v=Oh5oC98ztvI) spoke about GraphQL and how the language was created. He spoke about the principles and lessons that they learning in the process. These included things like, think like a client, make sure you’re solving a real problem, and using software as communication.

Afterwards, [Andre](https://www.youtube.com/watch?v=pYbgcDfM2Ts) talked about metrics and how some numbers can be decieving. There are lots of great point in here about looking at things like runtime lag, VM lag, routing, request time, etc. but one of the most important things he talked about was to not rely on averages. Average numbers make you think that you understand whats going on and make you think that an average is also standard distribution but it’s not, so you need to look closer at the numbers.

One of the best talks I went to was [Lea’s](https://www.youtube.com/watch?v=02h74L1PmaU) about the languages for 3D knitting. This talk was really awesome. As a crafty person, it’s great to hear about some of the science and tech behind industrial knitting machines. Lea spoke about knitting terms and different machines that do industrial knitting and how they all work. She then talked about knitPaint and a variety of other languages that you can use for designing and executing patterns on a knitting machine. She went over a few libraries and other things out there as well related to programming and knitting.

Next, [Jennie](https://www.youtube.com/watch?v=L1-oLdnoigQ) talked about monitoring. She covered different types of monitoring… system monitoring, application monitoring, and business intelligence-related monitoring. She talked about scaling online games and talking about what that scale looks like (which is huge) and walked through a pipeline of information and where and how pieces need to change in order to accommodate better monitoring at scale.

In the next session, [Andy](https://www.youtube.com/watch?v=uwiaT3MoDVs) talked about Guile which is a new programming language based on Scheme. He spoke about the different types that exist in the language, aspects of the language like speed benchmarks, etc. and finally what’s coming up in language development.

Almost closing out the day, Gary talked about reproducibility, or having the same action do the same thing. He spoke through three interesting systems of react rendering functions, bundler, and git, to show different mental models and how the actions always lead to the same results, One of the main takeaways was the reproducibility leads to good mental models which leads to the tools we love where the designs aren’t obvious.

In the closing keynote, [Leigh](https://www.youtube.com/watch?v=2BvVZU4IPKc) did a great job talking about security and what folks should keep in mind.

As a sidenote, two talks I wish I went to were the talk on [Tulip](https://www.youtube.com/watch?v=lvclTCDeIsY) and the talk on [diversity](https://www.youtube.com/watch?v=4KhXwl0L61g). Definitely check them out as well if you have a moment.

If you want to check out other notes, Trevor did an amazing job [here](http://trevmex.com/page/2).
