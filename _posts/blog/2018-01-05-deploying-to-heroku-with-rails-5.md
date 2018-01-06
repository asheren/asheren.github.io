---
layout: post
title: "Deploying to Heroku with Rails 5 or Why the secrets.yml file causes trouble"
date: '2018-01-05'
author: Allison McMillan
share: true
tags:
- software development
- dotenv
- heroku
- rails 5
- deploying
---

Recently, I started a new side project (more on that in the future), and I wanted to deploy to Heroku. Now, I've done this before as part of a team workflow, but not using Rails 5. My code looked good, I referenced the Heroku docs just to make sure I'd gotten all the steps and deployed. The deploy succeeded but when I went to the site, there was an error... `An unhandled lowlevel error occurred. The application logs may have details.` So there I had my first direction. I checked the heroku logs and saw:

![error in the logs]({{ site.url }}/images/heroku_runtime_error.jpg)

Now is where things get a little confusing. I had added my `secrets.yml` file the `.gitignore` so that my secret keys, etc, wouldn't be checked in to Git, HOWEVER I had added my `SECRET_KEY_BASE` to my config vars on Heroku which I felt would solve the issue. I re-referenced the Heroku docs because generally they're amazing and I was really surprised that they didn't include anything about this issue. And I saw a handful of stack overflow answers but they seemed pretty convoluted. Heroku makes it a little difficult to deploy a single file that isn't checked in to GitHub, so, while I originally felt like using a gem for a small side project was overkill, I did end up using the `dotenv-rails` gem.

[The `dotenv-rails` gem](https://github.com/bkeepers/dotenv) is pretty straight forward. You install the gem and then create a `.env` file which you ensure is in your `.gitignore`. Then you add your ENV vars to that file and that's it. Then I redeployed and all was good on my new site.
