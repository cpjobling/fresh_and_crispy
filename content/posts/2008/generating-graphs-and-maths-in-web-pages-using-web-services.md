---
title: 'Generating graphs and maths in web pages using web services'
date: Fri, 15 Feb 2008 10:07:00 +0000
draft: false
tags: ['Uncategorised']
---

Once again Tony Hirst’s \[OUseful Info\](http://blogs.open.ac.uk/Maths/ajh59) blog has led me to three new pieces of brilliant web technology. In his blog entry \[RESTful Image generation – When Text Just Won’t Do\](http://blogs.open.ac.uk/Maths/ajh59/013114.html), Tony describes how MathTran (a Mathematics rendering service developed by the Open University) could be mashed up with with the Google Charts service to provide an easy way to get mathemattical results onto web pages. Lots of interesting stuff to follow up on but here are the highlights: - Jonathan Fine’s blog entry on \[MathTrans and Google Charts\](http://jonathanfine.wordpress.com/2008/01/14/google-charts-mathtran-and-editable-png-files/) that inspired Tony’s speculations.

\- The Mathematical text rendering system \[MathTran\](http://www.mathtran.org/) which uses JavaScript to contact a web service that converts TeX embeded in the \*src\* attribute of an  tag into PNG graphics file. E.g. ![”tex:](int_0^1) becomes !\[tex: int\_0^1 x^2 dx\](http://www.mathtran.org/cgi-bin/mathtran?D=1;tex=%5Cint%20\_0%5E1%20x%5E2%5C%2C%20dx).

\- The \[Google Charts API\](http://code.google.com/apis/chart/) which takes a URL like

[http://chart.apis.google.com/chart?cht=p&chs=450×160&chd=s:DHNEDFD&chtt=Completed%20T175%20users%20stating%2038%20Current%20courses%20%28min%203%20users%29&chxt=y&chxr=0,0,10&chl=BM240%7CM150%7CM255%7CM257%7CM263%7CMU120%7CM366](http://chart.apis.google.com/chart?cht=p&chs=450×160&chd=s:DHNEDFD&chtt=Completed%20T175%20users%20stating%2038%20Current%20courses%20%28min%203%20users%29&chxt=y&chxr=0,0,10&chl=BM240%7CM150%7CM255%7CM257%7CM263%7CMU120%7CM366) and generates ![](http://chart.apis.google.com/chart?cht=p&chs=450x160&chd=s:DHNEDFD&chtt=Completed%20T175%20users%20stating%2038%20Current%20courses%20%28min%203%20users%29&chxt=y&chxr=0,0,10&chl=BM240%7CM150%7CM255%7CM257%7CM263%7CMU120%7CM366)

\- The \[Google Charts maths equation plotter\](http://www.felipebarone.com/plot-function-google.php) which takes a math formula and generates the Google Chart API code for the graph. E.g. for !\[\](http://www.mathtran.org/cgi-bin/mathtran?D=1;tex=%5Csin%28x%29-%5Ccos%28x%29%5Ccos%28x%29) we get : ![](http://chart.apis.google.com/chart?chtt=f%28x%29+%3D+sin%28x%29-cos%28x%29%2Acos%28x%29&chts=FF0000,16&cht=lxy&chs=400x400&chd=t:0,1.67,3.33,5,6.67,8.33,10,11.67,13.33,15,16.67,18.33,20,21.67,23.33,25,26.67,28.33,30,31.67,33.33,35,36.67,38.33,40,41.67,43.33,45,46.67,48.33,50,51.67,53.33,55,56.67,58.33,60,61.67,63.33,65,66.67,68.33,70,71.67,73.33,75,76.67,78.33,80,81.67,83.33,85,86.67,88.33,90,91.67,93.33,95,96.67,98.33%7C36.92,44.87,53.46,62.24,70.66,78.22,84.43,88.88,91.28,91.47,89.44,85.31,79.37,72.01,63.69,54.94,46.28,38.19,31.09,25.28,20.96,18.17,16.84,16.78,17.69,19.24,21.06,22.8,24.15,24.9,24.92,24.21,22.89,21.17,19.34,17.77,16.81,16.81,18.06,20.76,25,30.73,37.76,45.81,54.45,63.21,71.56,78.99,85.02,89.26,91.42,91.35,89.07,84.73,78.61,71.12,62.72,53.96,45.33,37.34%7C0,100%7C58.3333333333,58.3333333333%7C66.6666666667,66.6666666667%7C0,100&chco=0033FF,DDDDDD,DDDDDD,3072F3&chxt=x,y&chxl=0:%7C-6%7C-1.5%7C3%7C1:%7C-1.75%7C-0.25%7C1.25&chm=&chg=25,25,1,5)

I look forward to trying these out in my own work!

Powered by \[ScribeFire\](http://scribefire.com/).