---
layout: post
title: 'Caridy Patino @ DevCon5 NYC'
date: 2012-07-24 03:18:59 -0700
permalink: /2012/07/24/caridy-patino-devcon5-nyc/
categories: ["html5", "trip-reports", "uncategorized"]
tags: []
---

Caridy describes how Yahoo! built Axis on three different platforms using Mojito. He talked a lot about lessons learned while building a complex UX on iOS, Android, and Chrome desktop.

* Build mobile products atop platforms designed for mobile products, lest you inherit a lot of technical debt
* No such thing as "write once, run everywhere." Axis has 547 different mockups
* Abstract communication when possible
* Try to reduce fragmentation
* Refreshing WebViews (HTML parts) can be painful; usually, refresh when returning from background is enough for most cases
* It is very difficult to experiment in iOS and Android because it's hard to do A/B testing
* Expect network craziness
* WebViews are not first class citizens in iOS

Axis has to solve this question -- how do you produce the right HTML, JS, CS per runtime and per request? To solve it, sometimes JS runs in browser, sometimes on server. Other times there are "Native Bridges" for iOS and Android.
Adaptation in Mojito reacts to screen size, connection speed, feature detection, and so forth. [YUI](http://yuilibrary.com/) helps considerably with such adaptation.
Glossary:

* Mojito: a Javascript application framework using YUI and Node.js
* Shaker: a static asset rollup tool
* Mojit: a sub-application
* Cocktails: platform that includes Mojito
