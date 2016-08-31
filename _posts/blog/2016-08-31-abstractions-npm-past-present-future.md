---
layout: post
title: 'Abstractions: NPM: Past, Present, and Future'
date: '2016-08-31'
author: Allison McMillan
tags:
- software development
- conferences
- learning
- community
- abstractions
---

Day 3 started off with a keynote by [Laurie Voss](https://twitter.com/seldo){:target="_blank"} about [NPM](http://slides.com/seldo/abstractions-npm#/){:target="_blank"}. I don’t know much about NPM but I wish I knew more, so I took a lot of notes.

_npm past_
Npm is all about sharing code, that’s how and why they started. Npm helps you share code, make packages, discover, and install. There are over 4.5 million people using npm and over half of cpm users have only been using it for six months. JavaScript code before npm was hard to share. Some of the perks of npm as a package manager is that there is no dependency hell and there’s semantic versioning. Related to dependency hell, npm and the module loader were written at the same time so they work very nicely together. For semantic versioning, we know versions as something like 2.15.54, or breaking.feature.fix, or major.minor.patch. Using semantic versioning reduces risk and allows for lots of small modules in npm. Small modules are super popular, it’s actually one of the reasons npm is s popular. There are over 300,000 modules in npm. And this works because npm makes it really easy.

The registry stores the packages. Modules are hosting in a variety of places but everything is in the registry because you don’t want to have to just rely on GitHub. Npm exists to make sure js, node, and everything else are working well together. The registry also enables discovery. A registry is faster than having to do a ```git clone``` or something similar. Git is for developing and collaborating but npm is for distributing.

_npm present_
This section was sort of a greatest hits of cool stuff about npm you should probably know.

So first you want to make sure you’re always updating your npm by doing ```npm install -g npm```. Currently you can also use a ```scope``` command which let you publish your packages under your own name. You can also group packages together and have private packages. The ```npm init``` file controls how npm runs, you can add defaults there, change it, etc. There’s also ```promzard```. You can do ```npm install``` with ```- -save``` to add a package to your dependencies. You can also do ```- -save-dev``` to only in stall it to your dev dependencies. Bundled dependencies makes downloading packages faster. Additionally, when you ```npm install``` npm goes to the server, gets a list of all the versions, and puts one of those persons on your computer. It also puts the version into the local cache of your computer. Because of this, you can also do an install offline.

There are run scripts, mainly ```npm start```, ```npm stop```, ```npm restart```, and ```npm test```. You can use these scripts to get dev dependencies for specific things like mocha.

Now on to ```.npmignore```. It works like ```.gitignore``` and automatically excludes things from your package. You also need to remember to change your semantic versioning number when you change you package. You can do this right from the command line by doing something like ```npm version patch -m “bump to version %s.”``` There’s something called ```shrink wrap``` and then finally npm organizations. There you can give permissions to specific teams by checking out ```npm team``` and ```npm access```. In team, you can ```create```, ```destroy```, etc. and in access you can ```grant```, ```revoke```, etc.

You can work on multiple packages by linking them user ```npm link``` and you can publish with distinct tags. You can also ```npm unpiblish <pkg>@<version>```, but you actually never want to do this. First, you can’t unpublish after 24 hours. Second, once you publish, it’s out there in the world and unpublishing doesn’t get that data back.

In order to keep packages up to date you can check out ```npm outdated``` and do ```npm update```, There are package config variables that you can change with the ```npm config set``` command. There are also lifecycle hooks like ```publish```, ```test```, ```start```, etc, and each of these has a ```pre``` command and a ```post``` command to allow for work flow automation and validity checks. You can put default config options in your ```.npmrc``` file. Install the Wombat cli which gives you the latest experimental stuff and allows you to manage web hooks by doing ```npm install wombat -g```. And you can use web hooks to automatically deploy.

Wow. That was a lot of commends. So not for
_npm future_
Npm is now the package manager for javascript. There are some big challenges coming up related to discover and trust and es6 modules. For example, discovery is great but finding the best module for something you want to do is becoming really difficult AND people want to know if they can trust a specific package. And then security is an issue. There’s the node security project which checks a package against known vulnerabilities. Npm is also thinking about reliability via [greenkeeper.io](https://greenkeeper.io/){:target="_blank"} which check for outdates dependencies that will break things and about efficiency since the size of packages is becoming an issue.
