---
title: 'Giving up the Ghost'
date: Sun, 18 Sep 2016 12:33:34 +0000
draft: false
tags: ['Blog', 'blogging', 'ghost', 'wordpress']
---

_![2016-09-18_1429-300x197](https://blog.cpjobling.net/wp-content/uploads/2016/12/2016-09-18_1429-300x197.png)Fresh and Crispy_ has been running as a self-hosted [Ghost](https://ghost.org/) blog for a couple of years now but today I moved it back over to a self-hosted Wordpress blog.

One of the main reasons for the move is that [upgrading the Ghost software is a painfully slow manual process](http://support.ghost.org/how-to-upgrade/). Other reasons include my desire to try technologies like [Mike Caulfield's Wikity](https://hapgood.us/2015/12/09/introducing-wikity/) which needs a Wordpress multi-site and the sheer convenience of being able to blog from the Wordpress App.

To transfer my content, I had to use the Python script [ghost2wp.py](https://gist.github.com/tzangms/a5b640e4368204426310) provided by _tzangms_ to convert from Ghost's JSON format to WordPress's xmlrpc. But that went very smoothly.

The Ghost blog will stay active as [ghost.cpjobling.me](http://ghost.cpjobling.me) for a while: at least until I have transferred some of the tags over.