---
layout: post
title: "Scope and Context in JavaScript"
date: 2018-11-05T19:00:00+05:30
draft: true
tags : [JavaScript]
Description : "Scope and Context in JavaScript"
---
While there are many, many articles on the topic online [^1], I just wanted to add my $0.02 to it.  
**scope** is the visibility of the variable. Think of it being in the "line of sight", where line of sight is on the same level or below.  
**context** means the dependence of the variable on being in an environment. This is used for methods in objects mainly, since the context can change for every instance of the object.

However, we can change the context for any method by using the call or apply function. Do go through  [^2] - its fun and will give you intuition as to scope and contexts .

Also, i would like to mention that [^3] and [^4] helped a lot in making this post look kind of academic.


[^1]: just one of the many! [What is the Difference Between Scope and Context in JavaScript?](https://blog.kevinchisholm.com/javascript/difference-between-scope-and-context/)  

[^2]: [John Resig's Learning Advanced JavaScript ](https://johnresig.com/apps/learn/)

[^3]: [Academic markdown and citations](https://www.chriskrycho.com/2015/academic-markdown-and-citations.html).  

[^4]: [Markdown cheatsheet](https://www.markdownguide.org/cheat-sheet/)

<!--stackedit_data:
eyJoaXN0b3J5IjpbNTI2MDk5OTc4LC0yMDM2MDA3NDc5LC0yMD
IwMjI1ODAwXX0=
-->