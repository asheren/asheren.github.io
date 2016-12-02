---
layout: post
title: "RubyConf 2016 writeup"
date: '2016-11-21'
author: Allison McMillan
share: true
tags:
- software development
- speaking
- conferences
- open source
- remote work
- computer science
- documentation
- servers
---


I was lucky enough to be a speaker this year at RubyConf 2016. You can check out my talk, “Even the Justice League Works Remotely” [here](http://confreaks.tv/videos/rubyconf2016-even-the-justice-league-works-remotely){:target="_blank"} on Confreaks, see the slides [here](https://speakerdeck.com/asheren/even-the-justice-league-works-remotely){:target="_blank"}, and the related blog post [here](http://collectiveidea.com/blog/archives/2016/11/21/even-the-justice-league-works-remotely){:target="_blank"}. And while that was really exciting, the more important part is that I got to see old friends, make new ones, and learn a WHOLE lot. Here are some of the highlights…

In Matz’s [Keynote](http://confreaks.tv/videos/rubyconf2016-opening-keynote){:target="_blank"}, there were some really interesting things discussed. Matz focused on the community, talking about keeping Ruby relevant through innovation and the strength of the community. He also introduced guilds which is a new concurrency model. Every object belongs to a guild and you can transfer object between guilds. Guilds run on independent threads and every guild is parallel. This seems like an interesting idea that will continue to evolve in the near future. The other thing that was discussed are type interfaced and a new type of static analysis that will be coming that will be like structural typing with type inference… words that i’m excited to learn more about.

I saw an amazing talk by [Chris Arcand](https://twitter.com/chrisarcand){:target="_blank"} called [Deletion Drive Development](http://confreaks.tv/videos/rubyconf2016-deletion-driven-development-code-to-delete-code){:target="_blank"}. I made a decision a couple minutes into the talk to stop taking notes and just follow along. It was a super interesting talk about figuring out what pieces of code are no longer being used, looking at edge cases and the different pieces you need to look at in terms of looking at the Ruby parser, processing the Sexpression, etc. The slides are excellent and the talk is really good. Highly recommended.

[Jeff Cohen’s](http:///www.twitter.com/jeffcohen){:target="_blank"} ’s talk on [CS-The Good Parts](http://confreaks.tv/videos/rubyconf2016-computer-science-the-good-parts){:target="_blank"} finally explained to this non-cs degree holder what a linked list is and what a binary tree is so that was pretty awesome.

[Tara Scherner de la Fuente](https://twitter.com/mediaremedial){:target="_blank"}’s [keynote](http://confreaks.tv/videos/rubyconf2016-you-have-the-empathy-of-a-goat-documenting-for-the-user){:target="_blank"} had some really great points. First, a top to use  Docs Doctor which is apparently now [Code Triage](https://www.codetriage.com/){:target="_blank"}. My favorite part were her tips for writing… just do it, write a readme, write installation instructions or do the second draft of a thing. To make it good you want to use simple sentences, no jargon, think about the context and user, write your way to the main point and then move the main point to the top, and use specific examples.

[Andre Arko](https://twitter.com/indirect){:target="_blank"}’s talk on [Contributing to open source](http://confreaks.tv/videos/rubyconf2016-from-no-oss-experience-to-the-core-team-in-15-minutes-a-day){:target="_blank"} gave a very honest look at the tradeoffs to consider when working on open source projects and actually acknowledged why some people legitimately can’t spend the time contributing to open source so applause for that. The part of the talk I liked the most was the overall message that you should do the thing that has the tradeoffs you’re happy with.

[Jonan](https://twitter.com/thejonanshow){:target="_blank"}’s [talk](http://confreaks.tv/videos/rubyconf2016-building-hal-running-ruby-with-your-voice){:target="_blank"} about using alexa and hal to deploy was really great. I learned a ton of new concepts and it was a lot of fun to watch. I also want to do a shout out to [Brandon](https://twitter.com/tehviking){:target="_blank"}’s [talk](http://confreaks.tv/videos/rubyconf2016-the-long-strange-trip-of-a-senior-developer){:target="_blank"} about becoming a senior developer was also really good. He spoke about 12 traits of senior developers and different levels that folks will be at **for that specific characteristic** when they’re junior, mid, senior, or beyond.

Lastly, the talk I think I took the most notes at was [Stella](https://twitter.com/practice_cactus){:target="_blank"}’s talk about [servers](http://confreaks.tv/videos/rubyconf2016-the-little-server-that-could){:target="_blank"}. This is actually something that has come up recently and an area I wanted to level up in so it was perfect. She talked about sockets, listening for requests, handling requests, and closing a socket. There was great information about stream sockets and datagram sockets, stepping through how a server works and common problems or issues.

All in all, as usual, RubyConf was a great time and I continue to love how friendly, welcoming, and nice our community continues to be.
