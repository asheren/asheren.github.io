---
layout: post
title: "Github Pages and Jekyll: Importing from Blogger and URL Redirects"
date: '2016-09-06'
author: Allison McMillan
share: true
tags:
- software development
- learning
- blog posts
- blogging
- jekyll
- blogger
---

As I mentioned, I’m sharing a few lessons learned from moving my site over to a github pages site using Jekyll. I was actually surprised at how much information was out there especially about importing from old blogs and redirecting urls. I purchased Daydreaminruby from name cheap and they have excellent documentation about having the right A records, CName, etc. when looking to make sure everything is hooked up right. You can find that documentation [here](https://www.namecheap.com/support/knowledgebase/article.aspx/9645/2208/how-do-i-link-my-domain-to-github-pages){:target="_blank"}. I mean seriously! Look at all those screenshots and arrows! I love it.

The I needed to import all my old blogs. I expected this to be sort of complex and annoying but it was way simpler than almost anything else i’d done with the blog. Following the instructions on the Jekyll docs, I got a backed up copy from blogger of all my posts, then I did:
```
ruby -rubygems -e 'require "jekyll-import";
JekyllImport::Importers::Blogger.run({
"source" => “PATH/TO/FILE.xml”})’
```

in the terminal and that was that! Pretty nifty.
