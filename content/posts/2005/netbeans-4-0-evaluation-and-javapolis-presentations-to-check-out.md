---
title: 'NetBeans 4.0 Evaluation and JavaPolis presentations to check out'
date: Fri, 18 Mar 2005 19:40:00 +0000
draft: false
tags: ['Uncategorised']
---

Just watched Tim Boudreau’s JavaPolis presentation/demo of [Netbeans 4.0](http://www.javalobby.org/av/javapolis/45/boudreau-netbeans4). Looks good and worth a look over the weekend. I’m keen to try out the much discussed Eclipse project import feature and the mobile application developer tools which, if they work, will give me something more concrete to put into my final Software Applications lectures on “Embedded Systems”.

<

p>The last time I used Netbeans, I was put off by the fact that it came with it’s own copy of the JDK (which I already had) so it was a bit of a disk hog for no good reason; Mounting a CVS repository only worked if you had a CVS client installed and Ant was not as well integrated. Eclipse worked with whatever JDK I had installed, CVS and Ant “worked out of the box” and so I just got more productive quicker in Eclipse. Things may have changed now. In Netbeans 4.0 Ant _is_ the project file, J2SE 5.0 support is built-in (Eclipse is behind the curve on that one, the compiler works fine, but the code editors can’t parse the new syntax features!) and hopefully CVS now works without extra tools.

<

p>From an educational use perspective, I’ve had some sucess using Eclipse to drive an agile software development project with 21 student developers all working on the same code base. However, I started to get problems when I bolted on Maven to get the nice project reports I’ll need to assess my students’ work. Maven needed “bog-standard” SSH access to the CVS repository. Eclipse’s variation `cvs -d:extssh:... checkout` crippled Maven builds, using `cvs -d:ext:... checkout` crippled Eclipse! There’s a work-around, but it’s a pain! Eclipse’s other big drawback is that iit’s a great Java code developer but to make it a great GUI developer or a great J2EE or J2ME app developer, you need to download loads of extra plugins. I want my students to have easy access to these tools, not to have to jump through hoops. Furthermore, getting all this stuff on the network at my University is a big problem if installation is more complex than double click on the _\*.msi_ file!

<

p>It’s clear that I’ve talked myself into some enthusiasm for this trial. I’ll blog some notes as I go to to report my findings.