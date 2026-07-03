---
layout: post
title: 'Using Google Maps in a responsive design'
date: 2014-05-07 22:07:51 -0700
permalink: /2014/05/07/using-google-maps-in-a-responsive-design/
categories: ["html5", "ruby-on-rails"]
tags: []
---

[When I'm not in the office, I'm often out birding and photographing birds. To keep track of my life list and bird photos I wrote a Ruby on Rails site hosted at [birdwalker.com](http://birdwalker.com/ "BirdWalker"); you can see all the source on [github.](https://github.com/wfwalker/birdwalker3 "birdwalker3 on github") This post is about some the evolution of that code]
I love maps and I love visualizing data, so when I started to accumulate location-based birding observations, I knew I wanted to visualize my data on a map. I created a Rails partial template called [\_google.html.erb](https://github.com/wfwalker/birdwalker3/blob/master/app/views/locations/_google.html.erb "source for _google.html.erb") that let me insert maps into any of my other templates. All was well.
Since the first version of that template I've struggled with two issues that I expect other web developers will encounter.

## 1. Making Google Maps responsive

When I first brought my Google Maps into a Twitter Bootstrap design, I found the Bootstrap CSS would resize the container for the map, as I hoped. Unfortunately, Bootstrap could not magically adjust the scaling or center of the map. As the map got smaller, it would show only the upper left corner of the original map area.
To fix this problem, I wrote a function to retrieve the width of the container, pass that info the Google Maps API, and trigger a resize event.

```
function resizeBootstrapMap() {
    var mapParentWidth = $('#mapContainer').width();
    $('#map').width(mapParentWidth);
    $('#map').height(3 * mapParentWidth / 4);
    google.maps.event.trigger($('#map'), 'resize');
    console.log(mapParentWidth);
}
```

I also added an event listener to invoke this function whenever the window changed size:

```
// resize the map whenever the window resizes
$(window).resize(resizeBootstrapMap);
```

## 2. How much interactivity should I provide?

When I finally got my maps to size up and down responsively, I was very pleased. I used Bootstrap's grid layout, so that the multiple columns on big screens would collapse down to one column when viewed on phones, with the map taking up almost the whole width of the screen (you can use Firefox's [responsive design view](https://developer.mozilla.org/en-US/docs/Tools/Responsive_Design_View "Responsive Design View") to see this in action).
When you embed a Google Map, you get a lot of interactivity by default -- panning, zooming, the ability to click on map pins and other objects. On laptops and desktops, I like the result. I can embed a map showing you an overview of [all the places I've birded in my home county](http://birdwalker.com/counties/2 "birdwalker.com interactive county map"), where you can also let you zoom in and find the names and descriptions of each. But this interactivity can be a problem on phones. It became difficult to scroll through and beyond one of these maps. I'd be dragging my finger on the phone, and instead of scrolling the page, I'd be panning the map.
I then tested two alternatives. First, I tried using the [Google Static Maps API](https://developers.google.com/maps/documentation/staticmaps/?csw=1 "Google Static Maps API"), which has no interactivity. However, it doesn't work with Bootstrap's responsive layout for all the same reasons I discussed in [my post about D3.js](http://softwarewalker.com/2014/01/31/replacing-google-image-charts-with-d3-js/ "Replacing Google Image Charts with D3.js"). Second, I tried using the dynamic Maps but [disabling most event handlers](https://github.com/wfwalker/birdwalker3/commit/045b8644b9eecedeca9902ee447b44edb59bfc4b "disabling google maps interactivity"). This also works, but eliminates the ability to browse the map and see the metadata I've associated with each map pin.
So, for now, I've [restored the panning controls and draggable maps](https://github.com/wfwalker/birdwalker3/commit/5d5bb9ebfb2ac527ac56560d6e964f3ecc7fe679 "restore interactivity to google maps rails partial") and just try to scroll carefully. Thoughts? I'd love to hear from you how you solved this problem.
