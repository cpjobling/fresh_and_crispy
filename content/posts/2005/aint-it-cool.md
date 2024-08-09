---
title: 'Ain''t it cool!'
date: Mon, 04 Apr 2005 10:17:00 +0000
draft: false
tags: ['Uncategorised']
---

Just watched this [Screencast](http://weblog.infoworld.com/udell/2005/04/03.html#a1206) from Jon Udell on the power of client-side scripting and web services. It it Jon demonstrates a little [bookmarklet](http://weblog.infoworld.com/udell/stories/2002/12/11/librarylookup.html) that takes an ISBN from a page (demo works with Amazon) and looks the book up in a library. Jon’s blog has a [page](http://weblog.infoworld.com/udell/stories/2002/12/11/librarylookupGenerator.html) where you can create your own bookmarklet for various library catalogue systems so I created one for Swansea University. Here’s it is:

javascript:var%20re=/(\[/-\]|is\[bs\]n=)(d{7,9}\[dX\])/i;if(re.test(location.href)==true){var%20isbn=RegExp.$2;

void(win=window.open('[http://voyager.swan.ac.uk'+'/cgi-bin/Pwebrecon.cgi?SAB1='+isbn+'&BOOL1=all%20of%20](http://voyager.swan.ac.uk'+'/cgi-bin/Pwebrecon.cgi?SAB1='+isbn+'&BOOL1=all%20of%20)  
these&FLD1=ISBN%20(ISBN)&DB=local&CNT=25','LibraryLookup','scrollbars=1,resizable=1,location=1,

width=575,height=500'))}

To use this, copy it into notepad and remove the newlines, then just drag the bookmarklet to the browser toolbar. Now when you visit Amazon and see a book you’d like, click on the bookmark and a pop-up window will show you if it’s in the library. Cool!

<

p>Jon takes this further further by using a Firefox plugin called [Greasemonkey](http://greasemonkey.mozdev.org/) which allows its user to add bits of DHTML (“user scripts”) to any webpage to change its behavior. Jon’s greasemonkey script allows the Amazon web page to be changed on the fly to show if the book is in the library and if it’s out, when it’s due back! Now that’s cool!