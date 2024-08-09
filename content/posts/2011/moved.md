---
title: 'Moved'
date: Mon, 28 Feb 2011 19:43:37 +0000
draft: false
tags: ['Uncategorised']
---

I have moved my blog using the instructions [How to Move from blogger to wordpress with permanent 301 redirection](http://www.sensehow.com/how-to-move-from-blogger-blog-to-wordpress-with-permanent-301-redirection/) provided by Aaslin Sathrak on [SenseHow.com](http://www.sensehow.com/ "Visit SenseHow.com.").

In outline, I created a special template page on [http://blog.cpjobling.org](http://blog.cpjobling.org) that redirects to a special WordPress page. This page interprets the redirected URL and finds the reference to the original blogger page permalink that was stored in the page metadata when I exported my blogger pages to WordPress. This is used to look-up the wordpress permalink for the relocated page and then WordPress is asked to issue an **HTTP 301 Moved Permanently** reponse that tells Google and others that the original blogger URL has now moved to WordPress. If all works well, I’ll be changing the title of this blog to Fresh and Crispy in a week or so. In the meantime, please let me know if you find any broken links.