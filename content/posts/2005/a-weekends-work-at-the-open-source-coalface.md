---
title: 'A Weekend''s Work at the Open Source Coalface'
date: Mon, 11 Apr 2005 11:32:00 +0000
draft: false
tags: ['Uncategorised']
---

I got my hands dirty trying to fix a bug in [Megg](http://web1.2020media.com/j/jez/javanicuscom/megg/) last week. My main motivation, for what turned out to be a long weekend’s work, was a desire to use Mike Clark’s pragmatic [automation template](http://www.pragmaticautomation.com/cgi-bin/pragauto.cgi/Build/ProjectTemplate.rdoc) announced back in July last year.

*   It wouldn’t load from the URL.
*   It wouldn’t load when I downloaded the zip file and copied it into `./templates/pragouto-template`.
*   It wouldn’t load from `./pragauto-template`.
*   In fact, it would only work when I added it to the templates collection in the project directory and added it to megg.jar using the “ant dist” target.

Intrigued, I uploaded the latest HEAD version from the [CVS repository](http://cvs.sourceforge.net/viewcvs.py/megg/) at sourceforge. The problem became even more intriging when I ran “ant test” on my new sandbox copy and it failed!

I dug deeper and found that the test failed because megg was looking for the provided java templates directory at`./templates/java` but failing to load `./java/megg.xml` (not `./templates/java/megg.xml`!) when later attempting to parse the megg properties.

When attempting to load a directory in the local folder `./java`, megg would fail wto find template files in `./templates/java`.

Templates would be loaded fine from the templates collection distributed in the Jar file (or added by me), which is why I assume the problem has not been noticed before.

I have attempted a fix to local file handling whereby megg now tries `./java` then `./templates/java` then `$HOME/.megg/java` and finally `$HOME/.megg/templates/java` before resorting to the jar file. If fact, my added code can actually find files at any path prefix, although I haven’t yet added that feature to the CLI (e.g. as an option `-t <em>templates_dir</em>`).

I made my changes by creating a new class to represent the _TemplatesDirectory_ which also allows the code for handling local file templates to be somewhat simpler. I also took the opportunity to use [commons-io](http://jakarta.apache.org/commons/io/) to make file copy a bit more transparent and the commons-io groups’ [best practices](http://jakarta.apache.org/commons/io/bestpractices.html) advice on using _java.io.File_ object rather than strings to manipulate file names.

I haven’t yet tested the option to download from a URL (which didn’t work when I tried it before my changes). It’s next on my to-do list. However, I have invited Megg’s developer ([Jeremy Rayner](http://javanicus.com/blog2/)) to have a look and possibly merge my changes into a test branch for review. Just need to find out how to generate a patch file from CVS manual!

It was nice to be busy!