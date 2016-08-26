---
layout: post
title: 'Abstractions: The Twelve-Factor Container'
date: '2016-08-26'
author: Allison McMillan
tags:
- software development
- conferences
- learning
- community
- abstractions
---

Moving right along, one of the things I loved about Abstractions was that it wasn’t focused on a specific programming language or topic. As a result, when I looked at the schedule, I knew I wanted to challenge myself to go to lots of different things… a little elixir, a little design, a little devops, and more. [Casey West’s](https://twitter.com/caseywest){:target="_blank"} talk on [The Twelve-Factor Container](http://www.slideshare.net/Pivotal/the-twelve-factor-container){:target="_blank"} was my devops for the day. And i’ve got lots of notes for this one.

In this talk, Casey covered the twelve factors that lead to operational maturity. It’s based on the factors outlined [here](https://12factor.net/){:target="_blank"}. For each factor, Casey mentioned what the factor was, what the anti-patterns the exist are and what the best practices should be. So here goes…

1. Code base deploys to a stack. The anti-pattern here is that you build separate images for staging and production and then you manage the config. You often also have tags for dev and prod. The best practice is to have feature flags or an ENV file of some sort, It takes some work to do feature flags correctly and effectively but if you put in that time at the beginning, it’s well worth it in the end.

2. Explicitly declare and isolate dependencies. Dependencies can also be abstracted and managed externally. The anti-pattern here is to look at latest but there can be major api incompatibilities and this can be very problematic because containers are an immutable packing that you’ve built. You want isolation between the build phase and the deploy phase. The best practices are to declare version numbers of upstream dependencies. Oftentimes you’l use a base image and then build on top of that and second, to depend on the base images for the default file system and run time. This makes it easier to rebuild intermediate containers.

3. Store config in env. The anti-pattern here is to have a ```config.yml``` file or hard-coded feature flags. The best practice is to simply use environment variables.

4. Treat backing services as attached resources, connecting to data stores, microservices, etc. The anti-pattern here is to rely on a stateful,long-term local disk. If you don’t use the 12-factor principles to build the application, then this is often the first issue you deal with. One env that does to this well with local disk is google cloud. He then talked a little bit about volume mounting in this scenario. The best practice to to connect to network-attached services using connection information from the environment with a service like [Vault](https://www.hashicorp.com/blog/vault.html){:target="_blank"}.

5. Strictly separate build and run stages. The anti-pattern here is to install on deploy but the best practice is to build immutable images, then build, deploy, run. Secondly, you want to respect that lifecycle of buid, run, destroy.

6. Execute the app as one or more stateless processes. The anti-pattern here is NFS or a network file system. I don’t know much about NFS so unfortunately, can’t provide more details but would be happy to be pointed in the direction of some good resources to learn more. The best practice is to schedule LRPs by distributing them across a cluster of physical hardware. This can provide a return of interfaces between the application instances and the underlying software.

7. Export services via port bindings. Don’t hard code the ports the software runs in. Get the port from the env.

8. Scale out via a process model. This takes down processes when the load is low.
(can you tell my brain was getting tired at this point in the talk?)

9. Maximize robustness with fast startup and graceful shutdown. You want to mitigate against traffic spike by having fast startup times. And you want to have a graceful shutdown if an instance blows up, you want to make sure you have have bad, corrupt, or lost data. The key term I learned while discussing this point was the “Hug of Death” which sounds very ominous.

10. Keep dev, staging and prod as similar as possible. Best practice here is to run containers in development. It helps you spin tup architectural dependencies so you can tweak instances. etc. You can also run the app in dev against the app in prod to compare if both are in containers.

11. Treat logs as event streams. The anti-patterns here is to have random log files all over the file system. Instead of doing this use STDOUT and manage logging applications and systems.

12. Finally, run admin and management tasks as 1 off processes. The best practice here is to reuse application images within specific entry points for tasks.

There are more factors to explore like api as first class in an application, secrets management, health metrics, and global distribution.


There was a short additional part about becoming cloud native and the difficulties there but I think the 12-factor walk through was really the meat of this presentation.
