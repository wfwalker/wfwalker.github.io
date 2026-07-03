---
layout: post
title: 'Highlights of the first Web Audio Conference'
date: 2015-02-03 16:44:36 -0700
permalink: /2015/02/03/highlights-of-the-first-web-audio-conference/
categories: ["uncategorized"]
tags: []
---

I recently had the pleasure of attending and presenting at the first [Web Audio Conference](http://wac.ircam.fr "IRCAM"), co-sponsored by [IRCAM](http://www.ircam.fr/?L=1 "IRCAM") and [Mozilla](https://www.mozilla.org/en-US/ "Mozilla"). I wanted to share some of the great things that I learned about there.
[Meyada, Hugh Rawlinson](http://hughrawlinson.github.io/meyda/ "Meyada")
Meyada is a library for computing various properties of an audio signal, including various measure of perceived loudness. These measures are great for creating visualizations that users perceive as correlated with sounds. Hugh used them to make [live visualizations inside his talk slides](http://fiala.uk/meyda-presentation/#1 "Meyada presentation"), very slick.
[Extending Csound to the Web](http://wac.ircam.fr/pdf/wac15_submission_14.pdf "Extending Csound to the Web")
Csound is a well-established programming language for generating and manipulating sound. Because it is written in standard C and has very few platform dependencies, it is an ideal candidate for cross-compilation with Emscripten and asm.js. The authors noted that the resulting code was not as fast as the PNaCL version they created, but that it was plenty fast enough to render many sounds in near real-time, and currently has a better cross-platform story.
[musicn.js, Chris Lowis](https://github.com/chrislo/musicn.js "musicn.js")
Csound traces its lineage back to the MUSIC-N languages originated by Max Mathews at Bell Labs in 1957. Chris's talk showed both how much has changed since then and how the fundamental ideas from MUSIC-N endure.
[Lissajous, Kyle Stetz](http://punkave.com/window/2014/09/05/improvising-with-code "Lissajous")
Kyle Stetz described a very opinionated system he built for controlling live music by writing code in the Google Chrome Console window. He put his ideas on the line by doing a live demo in front of us, which was quite well-received. Although the system may not generalize to all styles of music, I think we all admired his clarity of purpose and great presentation.
[HyperAudio](http://hyperaud.io/ "HyperAudio")
HyperAudio is a clean, simple UI for searching, browsing, and excerpting videos with spoken word audio, especially speeches and debates. The experience does rely on the hard work of creating  transcripts of the audio with very accurate timings; as automation makes that process easier, tools like HyperAudio will change the way ordinary people relate to video.
[EarSketch, Jason Freeman](http://earsketch.gatech.edu/ "EarSketch")
Jason Freeman and his colleagues at Georgia Tech brough a unique perspective to WAC. Instead of concentrating on how to use web technology to make music, they are interested in how to use web-based music tools to teach fundamental computer science concepts. When they use these techniques with high school students, they can show a significant increase in the number of traditionally under-represented groups in computer science.
The Tomb of the Grammarian Lysias, Ben Houge
The evening of the second day of the conference featured six different "Web Gigs", which were participatory musical experiences designed around many mobile phones in a concert space with a centralized coordinator and sound system. In my opinion, the most successful of these was Ben Houge's The Tomb of the Grammarian Lysias. The piece consists of solo vocalist singing an ancient poem in the original greek accompanied by snippets of vocal sounds. The accompaniment is played through the mobile phone speakers of everyone in the room, under the composer's control. The carefully designed sounds emanating from dozens of speakers throughout the room gave a wonderfully diffuse, ethereal quality to the piece, while his clear singing voice provided a visceral, earthy contrast to all the technology involved.
