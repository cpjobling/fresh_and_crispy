---
title: 'Bruce Eckel''s MindView, Inc: 7-9-04 Java Issues & Directions'
date: Sun, 11 Jul 2004 13:42:00 +0000
draft: false
tags: ['Uncategorised']
---

Bruce gave a talk at UC Berkley and 9 July 2004. This is his blog entry [7-9-04 Java Issues & Directions](http://mindview.net/WebLog/log-0055) which popped under my radar cover via the [Dion on Tech](http://www.almaer.com/blog/archives/000269.html) who blogged a [ServerSide new forum announcement](http://www.theserverside.com/news/thread.tss?thread_id=27239) (which has comments). The blog links to a 2 hour 16 minute streamed video.

> “Be warned, those of you who feel Java is the best language, forever and without bounds, and that it has no limitations: herein I critize Java, but in the spirit of understanding the limitations of the language. I strongly believe that understanding these limits makes you a more effective programmer.”

Here’s my summary of the key points that I made as I watched the talk for the first time. \[Times are for points at which the points are made in the talk\] Some key points worth following up on:

*   Macromedia Flex and MXML for rich client application development. Great technology which could really have an impact in the market that Applets have failed to capture provided it’s not released as an enterprise development environment with enterprise pricing!
    
*   Eclipse 3.0 as a Rich Client Platform
    
*   Java’s success in the server market: but all the problems and confusion with EJB makes its continued success uncertain. New approaches: lightweight containers, AOP, dependency injection, etc.
    
*   New features of Java 1.5
    
*   Generics and Autoboxing: Generics is really a way of making collection classes typesafe. Objects accepted are predefined and you don’t need to upcast and downcast. Autoboxingis the automaticconversion of primitive and wrapper object. Again designed to make it easier to use collection classes. Because of they way these have been implemented, they don’t work in some cases that you’d expect if you’d come from a C++ (Generics) or Smalltalk (Autoboxing) background. Worth noting is that in untyped languages like Python this is not even an issue! It just works without any syntax support!
    
*   Enumerations \[1h16m38s\]: Seems like a successful addition. And like you’ expect from the author of Thinking in Java, Bruce has some wacky ways to push the envelope much further than you ever would want to!
    
*   Attributes/Metadata (inspired by C#) \[1h23m19\]: Added, in Bruce’s opinion, because C# had them, metadata will be a big feature of EJB 3.0 and will eliminate the need to declare all those interfaces that you need to implement an Enterprise Java Bean, and possibly some of the deployment descriptor files. Similar in intent to the XDoclet tags, but handled now by the compiler. Bruce’s example was of pickling classes.
    
*   New Concurrency \[1h32m0s\]: Fixes some problems. Uses Doug Lea’s libraries. Better model but still something you haveto think about. Example is a Car washing program that puts wax on and takes wax off. New concurrency library has a new factory method that can pool threads and returns executor objects to execute a callable. This executor object cab be sent an `interruptAll` method to gracefully shutdown threads.
    
*   JUnit and Testing \[1h41m30s\]: not a new language feature, but a topic that Bruce got a lot of flack about when he published this [article](http://mindview.net/WebLog/log-0054) on his blog. He wants to make it easier to write tests. So do I so I’ll be interested to see what he comes up with (idea for mini project: see if Leo makes Bruce’s approach easier. Also doctest in python is really interesting.
    
*   Other syntax improvements
    
*   The D language
    

Great stuff!