---
layout: post
title: 'Abstractions: Kubernetes Abstractions'
date: '2016-08-30'
author: Allison McMillan
tags:
- software development
- conferences
- learning
- community
- abstractions
---

My second day ended (sort of) with [Kelsey Hightower’s](https://twitter.com/kelseyhightower){:target="_blank"} talk on [kubernetes](http://kubernetes.io/){:target="_blank"}. As I mentioned before, I did want to get a little exposure to some Dev-ops-y stuff and kubernetes is a new thing I’ve heard in passing recently. The talk was focused on container deployments using kubernetes. Kubernetes is a framework for building distributes systems. The key kubernetes abstractions are that it assumes you app is in a container, there are pods, secrets, and services.

After that very brief intro, Kelsey then jumped right into a demo (he warned us at the beginning that this wouldn’t be an intro to kubernetes talk but rather something a little more advanced). The demo was that we have a container and we want to run it. Kubernetes does the deployment but we do not want to pin the app to nodes. He showed some simple commands to create the deployment in kubernetes and launch 5 pods. Then looked at these pods, then got nginx running. Kelsey mentioned to update servers, you set the image and then update the declaration inside kubernetes which will do a rolling update without any drops.

He spoke about building your own schedule, saying the anything you create in kubernetes is in a central class and needs the global cluster state. We want them to feel reactive. And finally we want to use a resource scheduler to look at incoming workloads and make decisions about placement to make sure we’re efficiently using resources When the video is posted, check out the awesome Tetris example used in order to explain this concept... and give Kelsey an excuse to play Tetris on stage.

Finally, he walked through a great example related to updating certs in an application which helped explain the usefulness of a framework like kubernetes.

The slides for this talk aren’t up yet, but it looks like Kelsey has done it a number of times so recordings of this talk or very similar ones are online.
