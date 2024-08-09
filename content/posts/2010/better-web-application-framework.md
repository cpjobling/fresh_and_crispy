---
title: 'Better Web Application Framework'
date: Thu, 17 Jan 2008 16:18:00 +0000
draft: false
tags: ['Uncategorised']
---

For a web application that I am developing as part of a research project I have decided on using \[Python\](http://python.org/) for the business logic. The reasons being that the application will use fixed-point binary arithmetic, units, and data output as line-graphs. Python seems to have the libraries that I’ll need for this and is better suited for rapid development than Java.

Part of the requirements that I have been researching this last week have been concerned with the identification of a suitable web application framework for Python. I started out this week assuming that this would be \[Django\](http://www.djangoproject.com/) and even bought the \[book\](http://www.djangobook.com/)! However, because this is research, I have the luxury of time so I’ve done some additional research and decided that the alternative frameworks \[TurboGears\](http://turbogears.org/) and \[Pylons\](http://pylonshq.com/) were also worth a look. Searching Google for getting started screencasts and videos I discovered a \[wonderful video\](http://video.google.co.uk/videoplay?docid=6297126166376226181&q=turbogears&total=20&start=0&num=10&so=0&type=search&plindex=0) of a web application framework comparison presentation by Sean Kelly. In this presentation, Sean uses J2EE (Servlets and JSPs), Rails, DJango, TurboGears, Zope/Plone and even Enterprise Java Beans (JBoss) to develop a simple time-tracker application and reports his experiences. Rails, Django and TurboGears come out (roughly in that order), but the big surprise is that \[Zope\](http://www.zope.org/)/\[Plone\](http://plone.org/) comes out top! So, maybe I need to rethink!

I’ve embedded the video here as it’s not only a useful and timely comparison of web application frameworks, it’s also an example of just how useful and inspirational a simple presentation can be!

[http://video.google.com/googleplayer.swf?docId=6297126166376226181&hl=en-GB](http://video.google.com/googleplayer.swf?docId=6297126166376226181&hl=en-GB)

Powered by \[ScribeFire\](http://scribefire.com/).
---
### Comments:
#### 
[Paulo Simões](http://twitter.com/pgsimoes "") - <time datetime="2010-09-15 23:57:00">Sep 3, 2010</time>

Some months ago a I've tried to do something on Pipes. I bit tricky but really usefull to build PLE connections... Paulo
<hr />
#### 
[Chris Jobling](http://blog.cpjobling.me/ "cpjobling@gmail.com") - <time datetime="2010-09-16 00:23:00">Sep 4, 2010</time>

Paulo, for very simple use-cases, for example aggregating some RSS feeds, doing some filtering, removing duplicates, pipes is very simple. For more complex manipulations, I think you do need more expertise and some programming experience. I'm very much a beginner! As I mentioned in my post, Tony Hirst (@psychemedia on twitter) is my mentor in this!
<hr />
#### 
[psychemedia](http://ouseful.info "tony.hirst@gmail.com") - <time datetime="2010-09-16 01:45:00">Sep 4, 2010</time>

Have OPML, will travel...Here's a recipe from @cogdog about how to Downe's OPML file and generate a custom search engine that will search over all the specified blogs...:[http://cogdogblog.com/2010/04/19/two-timing-xml](http://cogdogblog.com/2010/04/19/two-timing-xml)/And if you want "instant" results from the custom search engine once you've created it, @mhawksey can show you how:[http://www.rsc-ne-scotland.org.uk/mashe/2010/09/google-custom-instant](http://www.rsc-ne-scotland.org.uk/mashe/2010/09/google-custom-instant)/
<hr />
#### 
[Cris]( "criscrissman@gmail.com") - <time datetime="2010-09-16 06:21:00">Sep 4, 2010</time>

Your screencast was awesome, Chris. I created a dashboard in NetVibes, added it to my Symbaloo homepage and now I'm in the RSS feed business. Thanks so much!
<hr />
#### 
[Chris Jobling](http://blog.cpjobling.me/ "cpjobling@gmail.com") - <time datetime="2010-09-16 13:44:00">Sep 4, 2010</time>

You are very welcome! I have used NetVibes in the past but always went back to Google Reader. Using it to create a dashboard for an on-line course seems a very good idea though and I'll be experimenting further.
<hr />
#### 
[Chris Jobling](http://blog.cpjobling.me/ "cpjobling@gmail.com") - <time datetime="2010-09-16 13:48:00">Sep 4, 2010</time>

Tony One of the problems with the simple pipe I came up with was the OPML parser block itself. Although Stephen Downes' OMPL is available as a URL, and therefore in a sense always up to date, the parsing into feeds seems to take too long and the pipe often times out before it can generate results. I need access to the raw data that is being used to create the PLENK2010 daily I think! But thanks for the tips, I'll follow them up.
<hr />
#### 
[Chris Jobling](http://blog.cpjobling.me/ "cpjobling@gmail.com") - <time datetime="2010-09-16 17:58:00">Sep 4, 2010</time>

Not only did his blog show me how ... @mkawksey went and gone and done it! http://www.rsc-ne-scotland.org.uk/mashe/search/plenk2010.html!
<hr />
#### 
[Linn](http://enperfektlektion.blogspot.com "gustavssonlinn@hotmail.com") - <time datetime="2010-09-16 18:15:00">Sep 4, 2010</time>

Very interesting! I want try to use an aggregator. But to complicated right now. I just added the link to The Daily as a bookmark on my igoogle, to keep the course separated from the rest in the RSS-reader.
<hr />
#### 
[Chris Saeger]( "chris_saeger@yahoo.com") - <time datetime="2010-09-18 03:55:00">Sep 6, 2010</time>

This is great work. It is just what I was looking for. I was about to ask you for this kind of help in the plenk moode but got your blog info instead. Much easier to connect here. Thanks much, @chris\_saeger
<hr />
#### 
[Chris Jobling](http://blog.cpjobling.me/ "cpjobling@gmail.com") - <time datetime="2010-09-19 21:05:00">Sep 0, 2010</time>

I'm glad it's been useful.
<hr />
