---
layout: post
title: "Jeff Atwood's PHP Singularity"
date: 2012-07-18 18:42:46 -0700
permalink: /2012/07/18/jeff-atwoods-php-singularity/
categories: ["uncategorized"]
tags: []
---

I recommend [this great essay by Jeff Atwood about the horribleness of PHP and what to do about it.](http://www.codinghorror.com/blog/2012/06/the-php-singularity.html "Jeff Atwood, The PHP Singularity")
I first encountered PHP when I did the second implementation of [birdwalker.com](http://birdwalker.com "BirdWalker"), my website for birding field notes and photos. I did the first version entirely in XML and XSLT. It was a contrarian choice for building an entire website, but it did force me to learn XSLT well enough to be the go-to guy at work for XSLT questions.
Compared to XSLT, writing birdwalker.com in PHP was a dream -- so fluid, so much ongoing feedback. Problem was, I looked up a year or two later and found SQL queries right smack in the middle of my presentation logic. Blech!
Eventually, I jettisoned PHP and started again. Version three of birdwalker.com is in Ruby on Rails, and it's good enough that [I feel comfortable open sourcing it](https://github.com/wfwalker/birdwalker3 "birdwalker.com sources at github"). Jeff calls on us to "**build compelling alternatives** [to PHP] and **make sure these alternatives are equally pervasive, as easy to set up and use as possible**." I'm currently thinking Ruby on Rails is one of those, but ask me again in another year when I'm due to throw the whole thing out and start over again. :-)
