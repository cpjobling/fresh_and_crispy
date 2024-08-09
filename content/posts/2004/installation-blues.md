---
title: 'Installation Blues'
date: Mon, 19 Jul 2004 16:01:00 +0000
draft: false
tags: ['Uncategorised']
---

I’ve just spent the whole day trying to install [OpenCMS](http://www.opencms.org/) on my SuSE 9.1 box. I got stuck trying to get access to MySQL. In the end I had to delete MySQL and delete the old databases. When I reinstalled I noticed that it advised my to

mysqladmin -u root password '_password_'  
mysqladmin -u root -h **_hostname_** passwd '_password_'

I didn’t do the latter first time around! When I fixed the error and changed the DB url to `jdbc:mysql:<em>hostname</em>:3306/` it finally all worked. Permissions on MySQL is a black art at the best of times, but I wish there was a note to this affect somewhere in the documentation. Oh, for a decent user manual!

Anyway, after about 5 hours of hair pulling, here is my new OpenCMS server: [http://eehope.swan.ac.uk:8080/opencms/opencms](http://eehope.swan.ac.uk:8080/opencms/opencms). I hope that [SnipSnap](http://www.snipsnap.org) goes better tomorrow.