---
layout: post
title: 'Tyler Smith (AppMobi) @ DevCon5 NYC'
date: 2012-07-23 17:16:45 -0700
permalink: /2012/07/23/tyler-smith-appmobi-devcon5-nyc/
categories: ["html5", "trip-reports", "uncategorized"]
tags: []
---

Tyler Smith talks about how to make great cross-platform games with HTML5
\* Research and choose an HTML5 game engine (see [bebraw's excellent list at github](https://github.com/bebraw/jswiki/wiki/Game-Engines)) based on features you need, size, cost, and mobile compatibility. Beware of open source projects that aren't being maintained or don't have active user communities. Consider:

* Does it scale for screen resolutions?
* Does it support touch inputs?
* Does it pre-render?

\* For mobile, you have to pre-render tile backgrounds, conserve Canvas drawing calls, and make small binaries for sounds and images.
\* Be prepared for radically different screen rations (4:3 iPad, 7:4 some Android, 3:2 iPhone)
