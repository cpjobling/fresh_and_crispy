---
title: 'Keep it DRY, keep it shy and tell the other guy'
date: Mon, 24 May 2004 17:07:00 +0000
draft: false
tags: ['Uncategorised']
---

Andy Hunt and Dave Thomas [The Pragmatic Programmers](http://www.PragmaticProgrammer.com) have published a brilliant article with the above title in Andy Hunt and Dave Thomas, “OO in one sentence: Keep it DRY, Shy and Tell the Other guy”, _IEEE Software_, Vol.21 No. 3, pp 101–103, May/June 2004. In outline their main points are:

*   DRY (don’t repeat yourself) states:> _Every piece of knowledge must have a single, unambiguous, and authoritative representation representation within a system._ (Hunt and Thomas, _[The Pragmatic Programmer](http://www.amazon.co.uk/exec/obidos/ASIN/020161622X/ref=sr_aps_books_1_1/202-5418779-1971851)_, Addison Wesley, 2000.)
    
    Non-authoritative information (e.g. for EJB all the various interfaces and configuration files) should ideally be generated from the authoritative sources. The DRY principle also applies to build process, code reviews, and documentation.
    
*   Shy means code should not reveal information about itself unless really necessary. There are four axes of undesirable coupling that violate the Shy principle:
    
*   _static coupling_ occurs when a program module needs another to compile. Some coupling is often necessary, but it should be minimised. Inheritence is a particularly nasty source of unanticipated coupling and delegation (_uses a_, _has a_) is often preferable to _is a_.
    
*   _dynamic coupling_ occurs when a class needs the services of another class. A good example of what can go wrong is code like `auction.getLot().getHighestBid().getBidder().getPerson()` (called a _train wreck_ that appears in one of my lab exercises. The client (`auction`) needs to know too much about its collaborating classes and is therefore fragile.
    
*   _Domain coupling_ occurs when too much information about business logic appears in code. It can often be reduced by the judicious use of meta data that is kept in properties or databases.
    
*   _Temporal coupling_ occurs when code execution is dependent on a particular execution order. Code that may one day be expected to run concurrently should be designed to be concurent.
    

A corollary of shy code is that code should not be nosy (could be paraphrased as _mind your own business_!

*   Tell the Other Guy \[or [Tell, Don’t Ask](http://www.pragmaticprogrammer.com/articles/jan_03_enbug.pdf) (_IEEE Software_, Jan/Feb 2003)\]. Don’t think of methods as function calls rather as sending a message. Make the other class responsible for providing a service, don’t expect a data return!

Great stuff as usual and well worth quoting in all my software engineering courses!

<

p>While on this note it’s probably worth noting that the Pragmatic Programmers are also bloggers: Andy Hunt blogs in [/ndy’s Weblog](http://www.toolshed.com/blog) and Dave Thomas as [PragDave](http://pragprog.com/pragdave). Both are on my Blog role at [Bloglines.com](www.bloglines.com).