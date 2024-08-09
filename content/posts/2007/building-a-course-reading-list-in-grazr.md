---
title: 'Building a course reading list in Grazr'
date: Thu, 20 Sep 2007 15:37:00 +0000
draft: false
tags: ['Uncategorised']
---

After reading [OpenLearn Unit Content Feeds via OPML](http://blogs.open.ac.uk/Maths/ajh59/010577.html) and [Click On Series 2](http://blogs.open.ac.uk/Maths/ajh59/010582.html) by Tony Hirst (both of which use [Grazr](http://www.grazr.com/): “Easy feed grazing and sharing”), I was today inspired to create a del.icio.us bookmarks and RSS feed aggregator for one of my courses which starts in a week and a half. Here’s a report on my experiences!

First-off I should say that Grazr is a web tool that takes either an RSS feed or an OPML file and, through the magic of Javascript, creates a dynamic feed viewer that can be embedded into any web page. Or altenatively, using the default tools provided, added to your Facebook, or Google start page (among other things). To use it, I first needed to create an OPML feed that would enable me to aggregate my bookmarks, RSS feeds, Podcasts, and other useful learning resources in one place, so I signed into [http://www.opmlmanager.com/](http://www.opmlmanager.com/) and created one.

Next I went to my del.icio.us account and pulled out the RSS feed for my [module](http://del.icio.us/cpjobling/eg-259) and added this to my new OPML file. I realised, that the tag [eg-259](http://del.icio.us/cpjobling/eg-259) would be too generic so I created RSS feeds for [eg-259:lecture01](http://del.icio.us/cpjobling/eg-259:lecture01), [eg-259+xhtml](http://del.icio.us/cpjobling/eg-259+xhtml) to allow some finer granularity. Finally I started to go through my “External Links” page on the Blackboard site to ensure I had all the links in del.icio.us and properly tagged. Next I exported the OPML file from [www.opmlmanager.com](http://www.opmlmanager.com/) and imported it into Grazr as a reading list. Finally I created a widget from the reading list which is here:

\[!\[\](http://grazr.com/images/grazrbadge.png)\](http://grazr.com/gzpanel.html?file=http://grazr.com/data/cpjobling/eg-259.opml)[http://grazr.com/gzloader.js?file=http://grazr.com/data/cpjobling/eg-259.opml](http://grazr.com/gzloader.js?file=http://grazr.com/data/cpjobling/eg-259.opml)

Good hey! A similar widget is also now embedded in the External Links page for this module. The beauty is that this widgets are dynamic and populated from Grazr on page load. As I continue to add new RSS feeds or bookmarks to this on-line reading list, all of the embedded Grazr widgets will automatically be updated. The widgets can be shared using a mailing list feature familiar to Flickr users, and the embeddable code can be grabbed or shared directly from each copy of the the widget itself. And of course, if that’s insufficient, the OPML can be used to create feed aggregators for your students which can be embedded in Oremi or inside their favourite RSS feed reader (did I mention Facebook is supported?).

The limitations of www.opmlmanager.com seems to be that each subscriber can only create one OPML feed per person. This won’t work for my application as I expect that I’ll want a custom feed for each of my modules (or perhaps even aggregated across a whole programme). But it turns out to not really be a restriction because the OPML format is very simple and once you’ve created your first OPML file online, you can either export it as a file, edit the XML code directly, and re-import it or, preferably, edit the XML source on-line at the Grazr site.

**Stop Press**  
As this article went “to press” I noted that Tony Hirst has blogged about the new [Grazr 2.0 Beta version](http://blogs.open.ac.uk/Maths/ajh59/010585.html) which looks awesome and will feature it’s own OPML editor!