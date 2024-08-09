---
title: 'Warp'
date: Wed, 07 Jul 2004 23:17:00 +0000
draft: false
tags: ['Uncategorised']
---

Warp is a new literate programming tool created by Harold Thimbleby of UCL to help accurately write about programs. The approach is described more fully in [Explaining code for publication](http://www.uclic.ucl.ac.uk/usr/harold/warp/#warp). The idea, in a nutshell, is to mark-up source code with commented XML tags so that code can then be extracted by the _warp_ tool into a file that can be included in a word document or LaTeX file or even (using JavaScript) an HTML file.

The extracted code (which can be as much as a whole compilation unit or merely a fragment) is guaranteed to match the source code. The source code can be edited using conventional tools — no need for a literate programming markup a la WEB, or outlining editor like LEO. The documentation can be prepared using conventional word processing tools like word, LaTeX or even reStructuredText — the only requirement is the ability to include another file.

A possible downside is that code and documentation are kept separate (but who really keeps them together?) which increases the “cognitive distance” between the explanation and the code to be explained.

A couple of positive advantages are that

*   _warp_ is a Java program so it’d be easy to add to a Java project’s build process.
    
*   It’s open source, so useful extensions, e.g. a reStructuredText filter, should be possible
    
*   It uses XML so many other filtering tasks are possible with XSLT and scripting
    

I have an immediate requirement for a version of _warp_ that could support the docutils format. I’ll let you know if that’s an itch that can be scratched.