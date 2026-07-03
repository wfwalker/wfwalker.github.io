---
layout: post
title: 'RubyOnAles wrap-up'
date: 2011-03-26 01:43:40 -0700
permalink: /2011/03/26/rubyonales-wrap-up/
categories: ["trip-reports"]
tags: []
---

[RubyOnAles2011](http://ruby.onales.com/) was a blast! In addition to getting in some serious hacking with JQuery, Rails, and the eBird API, I got to meet some cool ruby people, hang out in the cozy environs of the [Old St. Francis School](http://www.mcmenamins.com/421-old-st-francis-school-home), and hang out with my friend and mentor @ggoodale. Here are a few of the highlights:
**Jim Weirich and Matt Yoho, "Securing your Rails App"**
I had some familiarity with most of this material, but I really appreciated their concise summary and clear demonstrations of the various security problems facing web applications today. I especially appreciated their demonstration of a cross-site scripting (XSS) attack. Happily, Rails offers some pretty simple fixes for most of these attacks (some of which I will be implementing shortly for birdwalker.com)
**Avdi Grimm on exception handling**
Avdi started by exploring the details of Ruby's exception handling mechanisms, best practices, and mechanisms for extensibility and customization.  He then segued into a broader discussion of the dangers of using exceptions to address non-exceptional behavior. His design advice that will stick with is, "Detect errors at a low level; Handle them at a high level". By detecting errors at a low level, we have the most knowledge of the root cause of the problem, and can bundle the most information into the exception object. By handling them at a high level, we have the most context for knowing whether we can continue executing and how to explain to the user.
**Rein Henrichs, Recent intrusion at PHPFog**
Rein works at PHPFog which [recently got hacked in a major way](http://blog.phpfog.com/2011/03/22/how-we-got-owned-by-a-few-teenagers-and-why-it-will-never-happen-again/). I admire how open he and his company have been in disclosing how the intrusion was done, and he seemed genuinely passionate that we all learn from his mistakes. Their blog post is definitely worth reading.
**Kyle Neath, Design Hacks for the Pragmatic-minded**
Kyle describes himself as an engineer who has ended up doing a lot of design work. He urged us to refrain from gratuitous use of weird fonts, to add more padding around text, and to use color with restraint -- all of which suits my own design aesthetics just fine. He recommend an exercise in which you describe all the objects on your page in a hierarchical text outline, and from there to consider visual containment can match the hierarchical outline. He concluded with some stern words about making presentation materials. I especially liked "Do your slides look SLEEK? Then add more contrast -- this is not web design!" Having tried more than once to make sleek slides, this really hit home.
**Jesse Proudman, "Demystifying Auto Scaling"**
Jesse described how his firm, [Blue Box Group](http://www.bluebox.net/), is building their scheme to automatically scale application servers as demand rises and falls for their clients. The implementation seems to combine their existing internal API for instantiating app servers with a Rails application monitoring service called [New Relic](http://newrelic.com/). He showed some very straightforward code examples that, as advertised, really demystified what they're doing.
**Other notes:**
[Heroku](http://heroku.com/) is a Rails hosting service that integrates so thoroughly with the standard Rails makefile that you can deploy your app to their cloud in two simple command-lines. Very slick.
Test-driven development and Pair programming are very common among this crowd, but they're both still topics worthy of conversation.
[Gemstone](http://www.gemstone.com/products/gemstone), a former Smalltalk vendor, has reappeared as the basis for a new Ruby implementation called MagLev.
Anyway, those are my big takeaways, along with a bunch of other tidbits crammed into my Notational Velocity notes. Now for some more hacking before the flight to SJC.
from Portland airport, -Bill
