---
title: 'In Web2.0 URLs are not unique anymore...'
date: Sun, 19 Sep 2010 18:41:00 +0000
draft: false
tags: ['Uncategorised']
---

… and that’s a problem because it makes RSS feed aggregation harder than it should be.

Once upon a time, Tim Berners-Lee and a few of his close friends, invented the concept of a URL[1](http://www.blogger.com/post-create.g?blogID=6991676#note1), and in the early days of the web, the ‘U’ in URL could be taken to stand for Unique (although it’s always stood for Uniform). Thus, if you typed a URL into a browser address field, it would take you to one, and only one, destination.[2](http://www.blogger.com/post-create.g?blogID=6991676#note2)

On creating a new Yahoo Pipe for #PLENK2010, I’ve discovered that, because of URL shortening services, this is no longer true and can cause issues with aggregating and curating resources on the web.

My new pipe is quite simple: I thought “wouldn’t it be a good idea to the RSS feed the from social bookmarking sites delicious.com and diigo.com of all the items that are taggedplenk2010 and create a combined RSS feed from them.” Seems a simple enough idea and [Yahoo Pipes](http://pipes.yahoo.com/) is the ideal tool with which to set this up.

Here is my [PLENK2010 Social Bookmark Aggregator](http://pipes.yahoo.com/pipes/pipe.edit?_id=aa354c126e5bb2403c983b705e41b3a4) pipe:  
[![](https://blog.cpjobling.net/wp-content/uploads/2016/11/12477-2010-09-19_2006.png?w=300)](https://blog.cpjobling.net/wp-content/uploads/2016/11/12477-2010-09-19_2006.png)  
It’s quite simple. It takes the RSS feeds for delicious bookmarks tagged plenk2010 ([http://feeds.delicious.com/v2/rss/tag/plenk2010](http://feeds.delicious.com/v2/rss/tag/plenk2010)) and diigo bookmarks tagged plenk2010 ([http://www.diigo.com/rss/tag/plenk2010](http://www.diigo.com/rss/tag/plenk2010)) and combines them in the union block. Now some people will be tagging in delicious.com, and others will be tagging in diigo.com, and some, like me, will be tagging in diigo.com, but will have set up their account to cross-post to delicious.com. With the possibility of people posting the same link in multiple places, we want to ensure that we avoid duplication, so we include the Unique block which filters the combined RSS feed to choose only those items that are unique in their link (that is their URL).

The result is displayed as a list, which you can see by following [this link](http://pipes.yahoo.com/pipes/pipe.info?_id=aa354c126e5bb2403c983b705e41b3a4). You’ll note that Yahoo provides the output of this Pipe as an RSS feed, JSON[3](http://www.blogger.com/post-edit.g?blogID=6991676&postID=2416340927591798123#note3), a My Yahoo widget, iGoogle gadget, etc. It can even be obtained as a “badge” that can be embedded in a blog or VLE.

Very useful, I’m sure you’ll agree. But there’s a problem. If you look closely at the data, you will notice that there appears to be duplication. The same bookmark appears several times even though I’ve used the unique filter. What goes on?

If you look at the links, the answer quickly becomes obvious. It is because the person who bookmarked the resource explicitly or implicitly used a bookmark shortening service such as bit.ly, tinyurl.com, or even the bookmark shortening services of the bookmark services themselves.

Thus, one of the principle value propositions of social bookmarking, the identification and enumeration of resources that have been useful to many people, is being violated. And what’s worse, it makes my pipe less useful than it could be to me and my fellow #PLENK2010 students. Perhaps social bookmarking services and other link aggregation services need to de-reference shortened URL’s to avoid degradation of the uniqueness of the URL.

* * *

Notes

1[URL](http://en.wikipedia.org/wiki/Uniform_Resource_Locator#cite_note-URL_Spec-2) (Uniform Resource Location) is is a URI (uniform resource identifier) that, _“in addition to identifying a [resource](http://en.wikipedia.org/wiki/Resource_%28Web%29 "Resource (Web)"), provides a means of locating the resource by describing its primary access mechanism (e.g., its network location)”_.

2 This has never been strictly true, for example Content Distribution Networks, web caches, etc can make it seem that the same URL points to many different locations.

3 JSON is a data specification for the web by which information, e.g. a blog post and its associated meta data, can be packaged as a text string that represents a JavaScript object.