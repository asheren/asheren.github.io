---
layout: post
title: "Namespacing the Off function"
date: '2017-12-29'
author: Allison McMillan
share: true
tags:
- namespacing
- learning
- tricks and tips
---
The other week I learned about  the JQuery `off` function and the cool things you can do with namespacing around that. Using the off function, you can provide a specific handler so that you remove a specific item. Now the danger in this is that you can remove everything that has that handler and that's when namespacing comes in to play. You can namespace `off` and the specific handler you're looking for so that you can essentially scope the handler in order to find a specific handler instead of removing ALL of the related handlers. This way you know that you're changing something within a specific context instead of anywhere that the handler may exist within the application.
