---
title: 'Replace occurrence of string in files under directory tree'
date: Wed, 13 Sep 2006 15:45:00 +0000
draft: false
tags: ['Uncategorised']
---

This Python recipe “[ASPN : Python Cookbook : Replace occurrence of string in files under directory tree](http://aspn.activestate.com/ASPN/Cookbook/Python/Recipe/120991)” has a comment that reminded me of the power of Perl.

I am updating my slides for a lecture course that uses [rst2s5](http://docutils.sf.net/docs/user/slide-shows.s5.html) (a utility that uses [Docutils](http://docutils.sourceforge.net/)/[reStructuredText](http://docutils.sourceforge.net/rst.html) to generate [S5](http://meyerweb.com/eric/tools/s5/) slides). When I wrote the original slides for last year’s course, rst2s5 was still in the Docutils Sandbox. It has now been promoted into the official Docutils distribution but some changes have been made. One of these was that  
the directive

.. handout::

has been changed to

.. class:: handout

so I had a need for to make a search/replace in every file in a collection.

I know that there is a recipe for this in my copy of the Perl Cookbook (but I didn’t have a copy of that to hand), so I looked it up on the [Python Cookbook](http://aspn.activestate.com/ASPN/Cookbook/Python/). And there (in the comments to the above link) I found the Perl recipe:

find . -name '\*.txt' -print | xargs perl -pi  
\-e 's/.. handout::/.. class:: handout/'

Now that’s simple … and it worked!