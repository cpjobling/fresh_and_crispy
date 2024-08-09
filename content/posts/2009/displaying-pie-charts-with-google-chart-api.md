---
title: 'Displaying Pie Charts with Google Chart API'
date: Fri, 30 Jan 2009 13:06:00 +0000
draft: false
tags: ['Uncategorised']
---

<img src="http://blog.swansea.ac.uk/blog/eechris/2009/01/30/reflections-on-some-e-learning-feedback-part-1/" alt="Sample chart\](http://chart.apis.google.com/chart?chs=350x150&chd=t:60,40&cht=p&chl=Strongly Agree|Strongly Disagree)

In one of my \[current projects " title="" />I am [publishing the results](http://blog.swansea.ac.uk/blog/eechris/2009/01/30/reflections-on-some-e-learning-feedback-part-1/) (in blog form) of the first assessment of my use of e-learning that I have ever formally tried. The majority of the questions use the [Likert scale](http://en.wikipedia.org/wiki/Likert_scale) (where respondees are asked to rank their response to a statement along the scale of _Strongly-agree_ to _Strongly disagree_) and I want to present the results with pie charts like this one. I could use Excel and export the charts, as gif images, for upload to my blog, but that’s not very Web 2.0! So instead I thought I’d use the [Google Chart API](http://code.google.com/apis/chart/) instead. And here is an example of what can be achieved with a small bit of HTML magic.

The Google Chart API is a _web service_: you provide some information about the chart you want and it generates and returns a GIF image of the chart. The URL for the chart shown in this post is [http://chart.apis.google.com/chart?chs=350×150&chd=t:60,40&cht=p&chl=Strongly Agree|Strongly Disagree](http://chart.apis.google.com/chart?chs=350x150&chd=t:60,40&cht=p&chl=Strongly Agree|Strongly Disagree). To embed a chart in an HTML document, just use the Chart API URL as the `src` attribute of an image as in:

&lt!-- Use of & in the src attribute to stand for the & in the URL  
is not a spelling mistake!  
You have to use the HTML entity in order to be able to embed &  
in the URL! -->  
<img alt="Sample chart"  
src="[http://chart.apis.google.com/chart?chs=350x150](http://chart.apis.google.com/chart?chs=350x150)  
&chd=t:60,40  
&cht=p  
&aongly Agree|Strongly Disagree" />

<

p>Clearly, some familiarity with HTML is required to fully exploit this feature, but it’s well worth a look. Plus if you have a number of similar charts to produce, as my report will, you’ll probably find _copy, paste and tweek_ to be much quicker than anything you could do with traditional desktop tools.