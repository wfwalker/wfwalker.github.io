---
layout: post
title: 'HTML5 Gaming, Ashley Gullen (Scirra) and Tyler Smith (appMobi), DevCon5'
date: 2012-04-26 23:55:59 -0700
permalink: /2012/04/26/html5-gaming-ashley-gullen-scirra-and-tyler-smith-appmobi-devcon5-6/
categories: ["html5", "trip-reports"]
tags: []
---

Notes from HTML5 Gaming, Ashley Gullen (Scirra) and Tyler Smith (appMobi), DevCon5
Scirra makes [Construct2](http://www.scirra.com/construct2 "construct2")
The number one reason why your App is slow -- software rendering instead of HW acceleration
Why? graphics card drivers are a big, abysmal mess; browsers blacklist bad drivers; those users lose
Roughly half of web users have blacklisted graphics card drivers!
Lenovo won't let you download graphics card drivers from nVidia et al due to customization
**Drivers alone are holding back HTML5 gaming on the desktop**
iOS webkit when packaged in native app turns off GPU support. Lame.
Android stock browser has no GPU support.
You have to use native wrappers like appMobi, CocoonJS to solve this problem on mobile; PhoneGap doesn't work for gaming
[Google Closure Compiler](https://developers.google.com/closure/compiler/ "Google Closure Compiler") reduces ~800k of Ashley's engine into ~80k; woah
[Awesomium](http://awesomium.com/ "Awesomium") lets you distribute HTML5 games on desktop; fast, could be used to skip driver blacklist
