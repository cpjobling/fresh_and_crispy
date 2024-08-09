---
title: 'SnipSnap running'
date: Tue, 20 Jul 2004 14:39:00 +0000
draft: false
tags: ['Uncategorised']
---

I have installed a [SnipSnap](http://www.snipsnap.org) Weblog/Wiki at [eehope.swan.ac.uk:8668/space/start](http://eehope.swan.ac.uk:8668/space/start). Not sure how to make it start as a service because it launches an instance of a Jetty web server which is a Java Daemon process that can’t be killed by killing the shell script that started it. Thus you can start the server using an `init` script, but killing the server is not so simple!