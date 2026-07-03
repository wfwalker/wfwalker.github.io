---
layout: post
title: 'birdwalker.com and the difference between Apps and Websites'
date: 2012-04-24 14:51:19 -0700
permalink: /2012/04/24/birdwalker-com-and-the-difference-between-apps-and-websites/
categories: ["html5"]
tags: []
---

For my first six months of working at Mozilla on [our Apps ecosystem](https://developer.mozilla.org/en/Apps "Apps at MDN"), I would tell everyone that HTML5 developers should have an easy time getting their stuff into our Marketplace, because "it's just the web". And there are lots of advantages to being an experienced web developer when it comes to making a successful HTML5 App.
And then I tried it myself.
Here's [LucidChart](https://www.lucidchart.com/demo "LucidChart"), a fully-featured diagramming tool, running in a web browser. It's got a menu bar, it lets you open, edit, save, and close documents, it's got drag-and-drop. Awesome! So why does this look so weird?
[![LucidChart App in a Browser](/assets/images/lucid-chart1.png "LucidChart App in a Browser")](/assets/images/lucid-chart1.png)
Once you start looking at it, doesn't all that browser UI look weird up there? What would I expect the back button to do? Likely, it'll take me away from LucidChart right in the middle of trying to delete some text. And why shouldn't LucidChart's menubar be up at the top of the screen where my OS really puts menubars? hint: these are all things we can fix by establishing a standards-based Web Runtime for Apps.
Conversely, look at my own website, [birdwalker.com](http://birdwalker.com/ "birdwalker.com"), as an App:
![birdwalker.com as an App](/assets/images/birdwalker.png "birdwalker.com as an App")

It looks rather App-like -- the App name is in the title bar, an edit menu, and no browser back button. I was very proud of it at first. But then I started to ask -- do my other Apps have hyperlinked content? Shouldn't those tab-like things at the top remain visible as I scroll through the content? No, and yes. I've got some work to do!
