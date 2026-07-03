---
layout: post
title: 'Andrew Lunny, "Anatomy of an App", Adobe / PhoneGap'
date: 2012-04-25 17:59:44 -0700
permalink: /2012/04/25/andrew-lunny-anatomy-of-an-app-adobephonegap-10/
categories: ["html5", "trip-reports"]
tags: []
---

Notes from Andrew Lunny's talk, "Anatomy of an App", Adobe/PhoneGap
"Native versus HTML5" is not the distinction you should worry about.
"Is your App a citizen or a tourist?" Is your App a jerk or a non-jerk?
Citizens are responsible, considerate, knowledgable; Tourists are crass, self-serving, and ignorant
Alex Payne's post entitled "Shortchanging your business with user-hostile platforms" urges you not to use cross-platform frameworks because they are the gray mystery meat of client-side software. Slow, inconsistent, awkward.
Q: what is the most popular hybrid App on iOS? A: Facebook? Instapaper? APP STORE ITSELF is implemented in HTML/CSS
Q: how can your cross-platform App "pass" as native? A: don't be slow, ugly, inconsistent; do be fast, pretty, consistent, elegant
see Tim Bray's post "Three Mobile-Software Rules" post. Why isn't all software written that way?
three principles -- (1) death is certain, (2) you're not alone, (3) stop doing so much
(1) life for a mobile app is nasty, brutish, and short, so: start up quickly, listen for and cope with lifecycle events, listen to and cope with network status events, always save state always
(2) you're not alone, so make good use of android intents or iOS custom URL schemes; look ahead to web intents
(3) stop doing so much; if you don't bring along every single javascript library, you'll have fewer performance problems; avoid decoration; build lots of smaller apps
