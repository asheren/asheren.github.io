---
layout: post
title: 'Abstractions: Dancing with Data'
date: '2016-08-25'
author: Allison McMillan
tags:
- software development
- conferences
- learning
- community
- abstractions
---

I’m pretty bummed because I got to this talk late, so my notes are a little sketchier than usual. I would highly recommend you check out [Barrett’s slides](https://speakerdeck.com/barrettclark/making-data-dance-abstractions) because they had lots of good information and great code samples. So here’s what I’ve got…

First, Barrett talked about window functions. The definition from the documentation is that “a window function performs a calculation across a set of table rows that are somehow related to the current row.” There are lots of window functions but the ones to focus on are ```lead()```, ```lag()```, ```first_value()```, ```last_value()```, and ```row_number()```. The slides are really good for walking through and example. We then went into subqueries and the piece to really look at is the fact that in the examples we have a base query and then named subqueries. They’re wrapped in an outer query and then we can refactor in order to DRY out the whole query. We then talked  a little bit about DB views. Barrett recommended to check out [Scenic](https://github.com/thoughtbot/scenic) which is actually something i’ve been hearing a bunch about recently.

Highlights that are just words or phrases in my notes to look into further include “view concurrently” which will be available in PostgreSQL 9.4 and subqueries for field values.

Finally, we discussed a little bit of tooling which included the psql command line, [pgadmin](https://www.postgresql.org/ftp/pgadmin3/), [navicat](https://www.navicat.com/), visual query plans (which helps explain and analyze) like [https://explain.depesz.com/](https://explain.depesz.com/) and [http://tatiyants.com/pev/#/plans](http://tatiyants.com/pev/#/plans) which will let you see the hot spots (note: this will differ depending on the environment you’re looking at). Finally, database datatypes that are awesome and you should look into more are Array, DateRange and TSRange, JSON and JSONB, and UUID. And check out upset which is an update or insert for data.
