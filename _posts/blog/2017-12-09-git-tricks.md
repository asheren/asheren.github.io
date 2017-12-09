---
layout: post
title: "Git Tricks"
date: '2017-12-09'
author: Allison McMillan
share: true
tags:
- git
- learning
- tricks and tips
---

This week I learned two cool git tricks.

First, use `git push --force-with-lease` insted of just force pushing. What does force with lease do? Well, it ensures that you're not overwriting someone else's code with your own to make sure you don't lose work (and piss off your coworkers). Recently, a coworker and I were working on the same branch AND we were working alternate hours and irregular schedules. We tried our hardest to make sure we were communicating when either of us did work on the code and what we changed but we also knew that wouldn't be perfect. So we also made sure to use `--force-with-lease` to make sure we weren't overwriting each other's changes.

Second, I learned about `git reset --hard head^`. In the past, I've always used `git reset --hard HEAD~<number>` trying to figure out how many commits I needed to roll back. This is most commonly used (for me) when I accidentally commit onto the wrong brach (for example `master` when I really want to commit to a feature branch). By using `git reset --hard head^`, the carrot essentially "pops" off the last commit so that you can then switch to the branch you wanted to ACTUALLY commit the code to and commit it again.


