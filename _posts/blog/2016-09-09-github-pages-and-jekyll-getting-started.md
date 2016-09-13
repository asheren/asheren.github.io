---
layout: post
title: "Github Pages and Jekyll: Getting Started"
date: '2016-09-06'
author: Allison McMillan
share: true
tags:
- software development
- learning
- blog posts
- blogging
- jekyll
---

For many years I used blogger to blog about tech-related topics. A few weeks ago, I finally decided that I would take the plunge and move my blog over to GitHub pages. I started by outlining the parts of this process. first, I’d need to determine what information I wanted on my blog. Then, I’d need to find a template I liked. I briefly debated doing the whole design on my own but ultimately, it didn’t make sense to do so with so many good templates out there. After, i’d need to populate the new content. Finally, I wanted to get all my previous blog posts imported into the new GitHub pages. All of this was actually surprisingly easy.

I ended up using the [so simple](https://mmistakes.github.io/so-simple-theme/){:target="_blank"} theme. There were some plusses and minuses to this. The main plus was that I really like the design and documentation. The minus was that there were a lot of features and items I knew I wasn’t using which meant I needed to spend some time carefully cutting code, deleting sections, and making sure I wasn’t accidentally deleting a piece of code I needed.

There were two tricky things I ran into when I started that I wanted to share.

1. There are actually different docs related to getting started on a Jekyll blog and github pages. I started by using [these docs](https://pages.github.com/){:target="_blank"}. When I ran into trouble getting everything working, I was pointed in the direction of [this link](https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/){:target="_blank"}. What the second link and set of docs does is basically set up Jekyll and using Github pages via a Github pages gem. The gem pulls in everything you need for it to all work nicely together. So, in short, if you’re getting started and google ‘Github pages blog with Jekyll”, don’t follow the instructions in the more basic post, make sure to build your blog with Jekyll using the github pages gem.
2. When I started working with the theme, things weren’t actually loading and working like they were supposed to. This is because I had downloaded the ```_site``` folder in addition to everything else. What I later learned was that ```_site``` is auto generated by Github pages so if you’re using a theme and you see that before you start entering your unique content, you can delete it and it’ll regenerate when you run ```jekyll build``` and ```jekyll serve```.
