---
layout: post
title: 'Replacing Google Image Charts with D3.js'
date: 2014-01-31 18:02:08 -0700
permalink: /2014/01/31/replacing-google-image-charts-with-d3-js/
categories: ["html5", "ruby-on-rails"]
tags: []
---

[When I'm not in the office, I'm often out birding and photographing birds. To keep track of my life list and bird photos I wrote a Ruby on Rails site hosted at [birdwalker.com](http://birdwalker.com/ "BirdWalker"); you can see all the source on [github.](https://github.com/wfwalker/birdwalker3 "birdwalker3 on github") This post is about some recent improvements to that code]
When I first discovered [Google Image Chart API](https://developers.google.com/chart/image/), I had written little JS and was excited about how easily I could create decent-looking bar charts without including big libraries or writing a lot of code. I added a method in my Rails [ApplicationHelper](https://github.com/wfwalker/birdwalker3/blob/master/app/helpers/application_helper.rb#L47) class to generate a URL for the Google Image Chart API by encoding my parameters and data values into the expected format:

```
def counts_by_month_image_tag(totals, width=370, height=150) 
  monthly_max = 10 * (totals[1..12].max / 10.0).ceil

  stuff = {
    :chco => 555555,
    :chxt => "y",       
    :chxr => "0,0," + monthly_max.to_s,
    :cht => "bvs",
    :chd => "t:" + totals[1..12].join(","),
    :chds => "0," + monthly_max.to_s,
    :chs => width.to_s + "x" + height.to_s,
    :chl => Date::ABBR_MONTHNAMES[1..12].join("|")
  } 

  chartString = ("http://chart.googleapis.com/chart" + "?" + 
    stuff.collect { |x| x[0].to_s + "=" + x[1].to_s }.join("&")).html_safe

  ("<img src=\"" + chartString + "\" alt=\"Totals By Month\" width=\"100%\"/>").html_safe
end
```

I started using this helper from my various page templates and all was well. Time went by.
Eventually, I became disenchanted with this solution. I can develop and test the rest of the site locally on my laptop, but the external image URL's like those aren't reachable offline. The Google chart images are statically sized, so they're ill-suited to responsive design frameworks like [Twitter Bootstrap](http://getbootstrap.com/ "Twitter Bootstrap"). And, rendering charts as images doesn't allow for any interactivity. [note: Google addressed these deficiencies in a subsequent version of their Chart API, which does most of the work client-side, and adds a lot of scope for interactivity].
Meanwhile, I became more comfortable with JS and began to create more of birdwalker.com using it. After attending a conference talk about D3, I decided to copy a [sample bar chart](http://bl.ocks.org/mbostock/3885304 "Bar Chart sample") and [adapt it for my purposes](https://github.com/wfwalker/birdwalker3/issues/28 "\"replace google graphs with d3.js\""). I put the finished code in a Rails partial called [\_species\_by\_month.html.erb](https://github.com/wfwalker/birdwalker3/blob/master/app/views/sightings/_species_by_month.html.erb "_species_by_month.html.erb")
D3.js code works by chaining many function calls together. Each call has a very specific purpose, and the calls can generally go in any order. By chaining them together, you get the overall behavior you want. For example, to create the bars in my bar graph I do this:

```
var bars = svg.selectAll("rect").remove().data(sightingData).enter()
  .append("rect")
  .attr("x", function(d, i) { return x(d.month); })
  .attr("y", function(d, i) { return y(d.count);})
  .attr("height", function(d, i) { return height - y(d.count); })
  .attr("width", function(d, i) { return x.rangeBand(); })
  .attr("class", "bargraph-bar"
```

The calls to attr() specify the location and size of an SVG rectangle and assign it a CSS style name. By calling data() you can iterate over an array of data; by calling enter() you can create new SVG nodes for each item in the array. In this case, we iterate over twelve numeric values representing birding activity during each month of the year and create twelve rectangles.
These new graphs resize nicely as elements within my Bootstrap layout. And I was able to create a tooltip when mousing over each bar like this:

```
svg.selectAll("rect").on("mouseover.tooltip", function(d){
    d3.select("text#" + d.month).remove();
    svg
    .append("text")
    .text(d.count)
    .attr("x", x(d.month) + 10)
    .attr("y", y(d.count) - 10)
    .attr("id", d.month);
});
```

And remove the tooltip on mouse exit like this:

```
svg.selectAll("rect").on("mouseout.tooltip", function(d){
    d3.select("text#" + d.month).remove();
});
```

The tooltips are styled with CSS just like the other graph elements.
So far, my experience with D3 has been really great. I now have graphs that work well in a responsive layout, don't require external image links, and have some interactivity. Suggestions and code reviews welcome!
-Bill
