---
title: 'Mobile Accessibility'
date: Fri, 06 Aug 2010 15:02:00 +0000
draft: false
tags: ['Uncategorised']
---

_There should be a web app for that!_

Earlier today I tweeted

> A bit disappointed to be finding that major media outlets like the BBC make apps instead of making website mobile browser compatible.

After that outburst I felt some explanation was called for. I also felt a campaign coming on. So here goes.

**The Explanation**

If you have an internet enabled smart phone, then you almost certainly have a mobile web browser. Mine’s an iPhone and the browser’s Safari. Android phones presumably come with a Chrome browser and I assume that Opera is quite popular on other platforms. All these browsers are based on the latest versions of their respective rendering engines and can do a pretty large subset of HTML5, CSS3, and JavaScript. State of the art in other words. This also means that they understand the [CSS2 media type property](http://www.w3.org/TR/CSS2/media.html) and will therefore honour @media handheld to render a web page optimally for a small screen device.

But I hear you say, why is that important? Surely “_there’s an app for that_“! Well maybe there is, but consider this common scenario. You’re in your Twitter client on the mobile and you spot a link for an interesting news item on the BBC’s web site. What happens when you click the link? Does your Twitter client say “hey this guy’s got the BBC news app, we’ll use that to display this article”? No, it opens the browser either in the browser app or it uses the built-in browser to render the page in place.

And what gets rendered? The page as it would be rendered for a desktop or laptop machine, that’s what. A page designed to be displayed, in the case of the BBC, with a width of at least 976 pixels (I checked this dimension). A page for which its web designer has not considered accessibility on a screen with a of 480 pixels in landscape mode and only 320 pixels in upright mode.

Now the BBC news app is designed for the iPhone. It looks good and the navigation has been designed to work well on the smaller screen. It makes me wonder how many apps there are that are just customized browsers rather than accessible web sites designed to work well on hand held devices. I know that there are other reasons for having a customized app. Lack of flash on Apple devices forces content providers to provide an alternative. But even here, the widespread support of HTML5 video somewhat obviates even that need.

**The Campaign: There Should be Webapp for That**

I posit that _Content providers should provide web sites that work well in normal browsers!_ Give us web apps that work better or provide more features by all means, but give us accessible access to the main website as well. (And let’s face it, that should include multimedia!) Let’s name and celebrate those that do and name and shame those that don’t.

Just to be fair, my own institution [www.swan.ac.uk](http://www.blogger.com/www.swan.ac.uk) fails the test. It’s just about usable in landscape mode without zooming if you have very small fingers and very good eyesight. The same goes for the intranet, which we have control of, and the VLE which we don’t. Also, this blog, admittedly using a standard template, is not particularly accessible on the mobile.

With all that said here is the list of sites that I tried to get to from my Twitter client today that did and didn’t pass the accessibility test:

*   C- [BBC News](http://www.bbc.co.uk/news/). Frankly unusable without zooming (and video and audio, which is flash, doesn’t work either). There is a free app that overcomes these issues but it’s not callable from another app.
*   A [The Guardian](http://www%2Cguardian.co.uk/). Excellent, recognizes your browser and redirects you automatically to [m.gardian.co.uk](http://www.blogger.com/m.gardian.co.uk). No video or crosswords though! The USP for The Guardian app is off-line browsing and access to multimedia — but still not the crosswords!
*   D [Scientific American](http://scientificamerican.com/). Looks like the standard web page and is unreadable in any orientation without zooming.
*   A+ [YouTube](http://youtube.com/) … I know that there’s a standard app for YouTube, but with browser access, the web site redirects you automatically to the mobile version [m.youtube.com](http://www.blogger.com/m.youtube.com) and videos work.
*   A+ [www.w3.org](http://www.w3.org/) uses `@media` to switch to a low resolution version as you’d expect!
*   A+ [mashable.com](http://mashable.com/) uses `@media` (and possibly JavaScript) to transparently switch to a low resolution version.
*   B [apple.com/iphone](http://apple.com/iphone) Surprisingly, this is not optimized for viewing on the iPhone 3GS. Page does seem less cluttered than some sites surveyed, but small print is still too small. Perhaps it looks better on the higher resolution iPhone 4. Video is Quicktime MP4 so it works with Apple’s browser as you’d expect.

Perhaps you’d like to report your experiences in the comments or tweet a link with hashtag \[#thereisawebappforthat\](http://twitter.com/#search?q=%23thereisawebappforthat).

\*\*Does this matter?\*\*

If you are throwing your hands up in the air in bemused horror at my pedantic uninformed ranting, let me tell you that \*accessibility\* is the \*\*principle web design aim\*\* that I drum into my students from year one. From now on, more and more of your audience will be accessing your site and web applications from mobile devices. They shouldn’t be forced to download an app, even a free app, to access your site or service.