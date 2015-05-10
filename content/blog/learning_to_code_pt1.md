+++
title = "How I learned to code [part 1]"
description = "The languages and frameworks I've learned over the past 1.2 years"
tags = []
date = "2015-05-08"
categories = [
  "About"
]
slug = "how-i-learned-to-code-1"

+++

## Disclaimer

I generally find it difficult to write about myself. This is especially true when looking back more than a year ago when I was just beginning to learn. Much of the energy that led to previous projects has been transferred onto current ones, and so I will only briefly mention or link to previous projecs. As time goes by I imagine my projects that are no longer maintained will end up being broken links as domains expire and such.

## Intro

My first time spent working on a web project was by first creating a [wiki] [] 
that would document my laboratory experience while working at Dr. Carlos [Castro's] [] lab. I find [openwetware][wetware] to be a model format for other students in scientific lab to document their research, and I'd like to encourage all investigators to make their students write their notebooks in an online or at least digital format, which makes archiving 100x better. Although I doubt openwetware will take off, there are likely other wiki hosting formats for the scientific community.

I later then did the design for the 2013 Ohio Mod team's [website][ohiomod] (slightly broken).This was primarily an exercise in Adobe Illustrator as pages are in fact a gif format with sliced links. 

___

I came to quickly enjoy for making other designs for scientific figures, documents, and posters.



### Links to reports for research

{{< fig 
link="/documents/maeslantkering.pdf" 
src="/images/maeslantkering-thumbnail.gif" 
caption="made purely for fun"
title="Rotterdam sea gate graphic" >}}

{{< fig 
link="/documents/fuel_cell.pdf" 
src="/images/fuelcells-thumbnail.gif" 
caption="made as an application for nextech materials internship as well as for scholarship"
title="Fuel Cell Report 2014" >}}


### Links to the posters of previous research projects.

{{< fig 
link="/images/Gruenbacher-poster_3-31-2011final.pdf" 
src="/images/Gruenbacher-poster-3-31-2011final_thumb.gif" 
caption="poster used at the Denman event"
title="Nishikawara Report May 2011" >}}

{{< fig 
link="/images/Denman_May2012_Gruenbacher_Poster_May1.pdf" 
src="/images/Gruenbacher-poster-3-31-2011final_thumb.gif" 
caption="poster used at the Denman event"
title="Pelotonia Report May 2012" >}}

I wanted to build an online portfolio that would incorporate my previous projects and art projects. 

___

I first started by following website and php tutorials online, with my very first tutorial series on building a dynamic website by [digicraft][] (I am very proud that I could remember the youtube channel). My very first website from scratch using php, bootstrap, and many jquery libraries was my [first about me][] website. 

My very first framework was [code igniter][] which was quickly replaced by [laravel](laravel.com) by [Taylor Otwell][]. The laravel framework was my first impression of how to implement a model view controller framework and object-relational mapping. The [laracasts video tutorials](https://laracasts.com/) by [Jeffrey Way][way] were especially useful.

During the time I was learning the Laravel framework I was attempting to implement my first startup application: X-Press Cards. It was meant to be an online service for designing and printing cards. The laravel version was first [x-press cards][xcards]. Users would be able to upload a photo, write a message, import their addresses, and the card would then be sent from the web server to a printer. After printing the cards would be sent to respective addresses.

___
## Javascript Apps

The X-Press Cards website was then [reimplemented][xcards4] in the [Angular][] 1.0 JS framework. Angular and its directives first introduced me to the concept of dividing my work into discrete components for reusability. Two other angular apps built include:

* [game of life][gol] which was based off of [null program's][null] webgl experiment. I took ~1000 existing game of life patterns and added them as a library to the game. I had meant to add navigation and an improved interface to the game for high school students to use, but it failed to garner enough interest to justify the time.
* [bullet-feed][] which was meant to be an event/location-based messaging system using the real-time benefits of firebase and websockets. It was actually originally going to be called YakYak (until we saw YikYak had already done something similar just 11 months earlier).
* [MyDrive5][] built using the MEAN stack of mongoDB, Angular, node and express. Is meant to be a free website builder wich would generate money by charging a percentage from donation processing. I also began learning node.js at this time.

Although I enjoyed the increased productivity with Angular and the many supporting open-source libraries, I also came to realize that Angular 1.0 has several problems
including:
    
* Long loading time for angular app to start
* Constrained to the Angular way of doing things rather than learning best javascript practices.
* As a complex framework it does not allow for a very deep understanding of the underlying code.
* It does everything, which means stuck with a monolithic framework with no ability to use non-Angular libraries.
* The entire website can break from angular errors or missing javascript files.
* Poor search engine optimization
* Having to repeat certain logic in the front-end app and back-end api.

Ultimately though the biggest reason I left Angular was because the very premise of a single page app is simply not justified in most cases. Unless a web page requires a complex interface such as google maps or gmail, it is often better to stick to a static or server-side rendering of the web page.This is why I became so excited when I discovered React and its premise of isomorphic rendering on both the client and server.

There is a large variety of flux implementations for React, my two favorites have been the Yahoo [fluxible][] or [flummox][], both of which directly feature the isomorphic rendering. I've had the quickest implementation of Fluxible which I've been rebuilding the [MyDrive7][] site for. 

___
## Golang

Probably my favorite language to have learned and to develop in has been the [Go Language][]. Much of its advantages come from its community and its opinionated way of doing things. As my first systems language, I've really come to enjoy the strict typing of the compiler and the minimal dependency that the compiled static-binaries offer.


[wiki]: http://openwetware.org/wiki/OhioMod2013:Team/Paul "my wiki page"
[Castro's]: https://mae.osu.edu/people/castro.39 "castro lab website"
[ohiomod]: http://openwetware.org/wiki/Biomod/2013/OSU
[wetware]: http://openwetware.org/wiki/Main_Page
[code igniter]: http://www.codeigniter.com
[taylor otwell]: http://taylorotwell.com/
[way]: https://twitter.com/jeffrey_way
[digicraft]: https://www.youtube.com/channel/UCw0ZIfZiV-BORQvok_cxNPw
[first about me]: http://paulgruenbacher.com/bootstrap/about
[xcards]: http://paulgruenbacher.com/xcards/
[Angular]: https://docs.angularjs.org/guide/di
[xcards4]: https://github.com/pgruenbacher/xcards4
[gol]: https://game-of-life-gl.firebaseapp.com/#/app
[null]: http://nullprogram.com/webgl-game-of-life/
[bullet-feed]: https://bullet.firebaseapp.com/#/intro
[mydrive5]: http://www.mydrive5.com/
[fluxible]: https://github.com/yahoo/fluxible
[flummox]: http://acdlite.github.io/flummox
[MyDrive7]:https://github.com/pgruenbacher/mydrive7
[Go Language]: https://golang.org/