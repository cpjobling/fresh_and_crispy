---
title: 'Aide Memoir: Setting up auto logins with SSH'
date: Fri, 10 Sep 2004 10:42:00 +0000
draft: false
tags: ['Uncategorised']
---

This is something that I always forget how to do. Here is the recipe adapted from [Linux Server Hacks](http://safari.oreilly.com/?x=1&mode=section&sortKey=title&sortOrder=asc&view=&xmlid=0-596-00461-3&g=&catid=&s=1&b=1&f=1&t=1&c=1&u=1&r=&o=1&n=1&d=1&p=1&a=0).

<

ol>

1.  First generate your key  
    $ **ssh-keygen -t rsa**

This created two files, `~/.ssh/id_rsa` and `~/.ssh/id_rsa.pub`.  
5\. Then copy the key pair to the host you want to login to

$ **ssh -l _user_**_server_ "mkdir .ssh; chmod 0700 .ssh"_\*  
$ **scp .ssh/id\_rsa.pub \*user**_**@_server_:.ssh/authorized\_keys2** 6. Now you can login using  
$ **ssh -l _eechris_**_server_\*\*

and you don’t need a password. Exchange of public keys authenticates you.