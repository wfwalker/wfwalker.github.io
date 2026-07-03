---
layout: post
title: 'David Kaneda @ DevCon5 NYC'
date: 2012-07-23 15:35:48 -0700
permalink: /2012/07/23/david-kaneda-devcon5-nyc/
categories: ["html5", "trip-reports"]
tags: []
---

David Kaneda is talking at DevCon5 NYC talking about cross-device development:
\* You only get access to four touch events on most devices right now. See [Boris Smus's pointer.js](http://smus.com/mouse-touch-pointer/) as a nice abstraction layer. Enhance your hit radius for touch to make it easier to touch your target.
\* Scrolling is really hard. You need a library like [Swipe.js](http://swipejs.com/) or [iScroll](http://cubiq.org/iscroll-4) to give you the momentum and friction physics that you get on iPhone. Of course, David thinks [Sencha Touch](http://www.sencha.com/products/touch/) is the best; he's biased, since he spent months working on scrolling as part of the Sencha team. (Note: unfortunately, Sencha doesn't support Gecko).
\* Beware of measuring distances in pixels. Retina displays automagically compensate when you use pixel units in CSS, Android does not.
\* Read the user interface guidelines for iOS, Windows [Metro](http://msdn.microsoft.com/en-US/library/windows/apps/hh465424), [Android](http://developer.android.com/design/index.html). For example, iOS uses Sheets where Android uses Overlays. Standard icons for stuff like Reply, Trash, Bookmarks, Back are all different. Try to follow the platform-specific conventions (i. e., don't be a tourist) and leverage the universal stuff.
\* Buy some devices! Hold onto your old phones, use them for testing. Don't upgrade the iOS on your old phones, it's hard to go back. Buy old phones from your friends. Pay to attend Google I/O.
\* Lots of mobile interfaces are heading towards type-based minimalist interfaces while iOS becomes elaborate and [skeuomorphic](http://en.wikipedia.org/wiki/Skeuomorph). For example, the iOS Address Book interface makes non-geek users comfortable right away. The minimalist interfaces seem like they'll be a lot more portable, but for complex desktop Apps it may not scale up to having toolbars with 40 icons.
\* Use CSS to give yourself various fallback positions for fonts, backgrounds [but [beware the performance hit of fancy CSS](http://perfectionkills.com/profiling-css-for-fun-and-profit-optimization-notes/)].
\* Sometimes, you just have to use User Agent detection (followed by tagging DOM with platform-based classes and then fixing it all in CSS).
