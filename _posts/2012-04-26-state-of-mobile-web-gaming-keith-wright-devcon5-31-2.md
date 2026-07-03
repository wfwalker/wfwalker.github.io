---
layout: post
title: 'State of Mobile Web Gaming, Keith Wright, DevCon5'
date: 2012-04-26 00:46:14 -0700
permalink: /2012/04/26/state-of-mobile-web-gaming-keith-wright-devcon5-31-2/
categories: ["html5", "trip-reports"]
tags: []
---

Within Android, breathtaking diversity of screen resolution, processor speed -- HTML/JS/CSS parse speed ranges from 0.4 to 1.4 seconds (put JS at end of the page!) even with JS in cache
later OS version doesn't guarantee better device (see Cricket Mobile)
In his world, Canvas is too slow on mobile devices for gaming; don't count on Web Workers, WebGL. WebSockets, etc.
Monetization is less smooth; Distribution is hard; Google+ has no mobile games story
He lists off lots of game engines and libraries; they don't use any of them (100k library is too big!)
Speed is everything, especially during game load; use local / session storage; all games are one page load
client cache is limited; iOS 4.3 had total 4MB limit; Android had total 2MB limit; try to limit HTML pages to 25k if you want them to be cached
local storage is OK up to 5 MB, after which it gets ugly
Avoid DOM updates to make mobile browsers happy
Do use CSS transitions
Do use CSS four color gradients instead of repeating images for 3D-looking buttons
CHALLENGE: can you design a two lane road for a side-scrolling game using CSS gradients?
Q: are data URI's useful for mobile game performance? A: reduces network request but 30% bigger than raw file
Q: use gzip on mobile? A: yes, always
avoid CSS box-shadow and text-shadow, they killed mobile performance
do use CSS3 animations (webkit keyframes example) to make waving flags
do use stepped animation, but expect to use lots of proprietary ways to find next available frame time
pre-ICS Android disregards absolutely-positioned items when doing click events. The z-index problem.
orientation change is slow and unreliable
cheaters -- don't store game state in the DOM; wrap all javascript in closures; single page load defeats URL hacking attempts; sign requests with timestamp
