---
title: 'The Ted Neward Challenge (AOP without the buzzwords)'
date: Wed, 02 Jun 2004 09:07:00 +0000
draft: false
tags: ['Uncategorised']
---

Adrian Colyer has tried to describe AOP without using the buzzwords. An attempt to answer a challenge thrown down at the last TSS symposium in [The Aspects Blog](http://jroller.com/page/colyer/20040531#the_ted_neward_challenge_aop). It boils down to DRY (don’t repeat yourself).

> So what we’ve really got in any non-trivial software application is not the ideal 1-to-1 mapping between concept and implementation, but an n:m mapping. No wonder software gets so hard to maintain, and so hard to understand, and so complex. And _it’s not your fault_. The tools that object-oriented languages give us don’t enable the clean mapping of every design concept into a single implementation construct … and consequently neither do they allow each implementation construct to map cleanly onto a single design concept. This is the problem that aspect-oriented programming attempts to help us solve. It’s about getting as close to a 1-to-1 mapping as we can. AOP addresses the problem by introducing a new construct known as an aspect that is able to capture in one place the implementation of design requirements, such as the view-notification requirement \[all views have to be notified if the model changes\] in MVC, which OOP cannot.