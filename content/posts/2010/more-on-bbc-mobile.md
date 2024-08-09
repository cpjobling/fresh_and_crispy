---
title: 'More on BBC Mobile'
date: Sun, 08 Aug 2010 11:56:00 +0000
draft: false
tags: ['Uncategorised']
---

On the theme of [mobile web accessibility](http://blog.cpjobling.org/2010/08/mobile-accessibility.html) (#thereisawebappforthat) I did some more exploration of the BBC’s mobile ([http://www.bbc.co.uk/mobile](http://www.bbc.co.uk/mobile)) web site and discovered that there is a mobile version of iPlayer at [http://www.bbc.co.uk/mobile/iplayer](http://www.bbc.co.uk/mobile/iplayer) which streams video in MP4 format suitable for the iPhone. Thus, I’d have to regrade the BBC’s mobile accessibility to A+ … providing that you enter the site from the root URL.

In the spirit of research, and because I teach some of this stuff, I dug a little deeper and discovered that if you visit the BBC with a conventional browser, the pages are returned using the XHTML 1.0 Strict doctype and stylesheets are provided for screen and print media with customizations for Internet Explorer 6.

On the mobile site, the doctype is the Wapforum proper subset of XHTML 1.0 ([http://www.wapforum.org/DTD/xhtml-mobile10.dtd](http://www.wapforum.org/DTD/xhtml-mobile10.dtd)) and the default stylesheet is tuned for mobile. What we used to call WML and WAP in fact.

Given that there is no conditional code or alternate stylesheets in these pages, I conclude that the BBC web server does some “browser sniffing” on arrival and checks the User-Agent field in the HTTP request. If you arrive at the home page [](http://www.bbc.co.uk)[http://www.bbc.co.uk](http://www.bbc.co.uk) with a mobile you are redirected to the mobile version of the web site. If you arrive at certain parts of the mobile site where there is media, further filtering takes place and “if you’re not on the list, you’re not getting in”.

This strategy works well, and allows the BBC to provide the mobile introduction page [http://www.bbc.co.uk/mobile/web/](http://www.bbc.co.uk/mobile/web/) if you arrive with a conventional browser at [http://www.bbc.co.uk/mobile](http://www.bbc.co.uk/mobile). This page has an embedded mobile emulator and a link to [http://www.bbc.co.uk/mobile/index.html/index.html](http://www.bbc.co.uk/mobile) if you insist on going further with a normal browser.

If you examine the URLs in the BBC website, you get a clue as to why linking to a page, say on the news site, in a Tweet might not work for all audiences. Let’s take today’s news article: [Honeybees are ‘Cleverer in the Morning’](http://www.bbc.co.uk/news/science-environment-10892913).This is the kind of quirky news headline that I’m sure you’d want to tweet. Indeed, the BBC offers you a sharing button that offers this tweet:

> BBC News – Honeybees ‘cleverer in the morning’ [http://www.bbc.co.uk/news/science-environment-10892913](http://www.bbc.co.uk/news/science-environment-10892913)

Now, let’s say I receive this tweet on my twitter client (I used Tweetdeck, but Twitterific does the same thing) on my iPhone 3GS and I follow the link. The embedded browser loads the normal news page rather than the more appropriate [http://www.bbc.co.uk/news/mobile/science-environment-10892913](http://www.bbc.co.uk/news/mobile/science-environment-10892913). The content is identical, but the doctypes, HTML headers and styleshets are different. The actual page (the one that was linked to remember) uses the conventional two column layout, rich navigational options and lots of white space and is tiny on a mobile on nomal (320 pixel wide (illustrated)) orientation and not much better at 460 pixel landscape orientation.

[![Honeybee story as displayed on mobile with 320 pixels width.](http://static.flickr.com/4121/4871663976_c86f1f9159_m.jpg)](http://www.flickr.com/photos/51214457@N00/4871663976/ "moz-screenshot-1")

The mobile version stacks the headline, picture (smaller than the one on the main page), byline, article and navigation tools and is designed to work on small resoultion displays and looks great at even 320 pixels.  
[](http://www.flickr.com/photos/51214457@N00/4871663976/ "moz-screenshot-1")[![Honeybee story as displayed on mobile device](http://static.flickr.com/4098/4871061703_4e6cce06b6_m.jpg)](http://www.flickr.com/photos/51214457@N00/4871061703/ "moz-screenshot-2")

The fix is “simple”, expect your clients to reach your web sites from a referal rather than navigation, and do the browser sniffing and redirection everywhere, not just at the top level.

Of course, I write this from the comfortable position of a critic’s armchair. I don’t underestimate the technical problem of creating a fully accessible web site as large as the BBC’s, and they clearly have addressed many of the issues. There are just a couple of grey areas left.

There is a further complicating factor. As examination of the URLs will reveal, the BBC is not one website. It has many websites, spread out across many virtual directories and even across multiple domains (students read virtual hosts). Each one is presumably managed by separate teams and it must be quite difficult to achieve consistent and correct browser-based behaviour across them all. The BBC actually makes for a good case study for my students and I see an assignment coming on!

Blogged with the \[Flock Browser\](http://www.flock.com/blogged-with-flock "Flock Browser")