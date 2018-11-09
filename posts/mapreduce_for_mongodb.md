---
layout: post
title: "Mapreduce i"
date: 2018-08-15T06:59:43+05:30
draft: true
---
Today i shall write of map reduce, specially for mongodb.
This is really great to use to do some massive computations using some primitive building blocks.
Map reduce comprises of 2 steps:
  1. Map  
  2. Reduce  

What do these terms mean, though? why is it so popular? is this worth the pain? For answering these questions and raising a few more, please read on.
The process of mapReduce is from functional programming, where any function does not have side effects, an unintended consequence of . 
**Map** is a process where, essentially, we process each data element ( calling it a **key** ) and put up our findings against it ( And call it a **value** ). 
We then perform the **reduce** operation on it, running a operation of aggregation on this emitted value, so that we can get the required result.

Since this is a tutorial for using mapreduce for mongodb, we will start with creating a database to use on this.
  

References:
1. [Mapreduce for the family](https://webofdata.wordpress.com/2012/11/05/mapreduce-for-kids/)  
2. [Can your programming language do this?](https://www.joelonsoftware.com/2006/08/01/can-your-programming-language-do-this/)  
3. [MapReduce, a really simple intro](http://ksat.me/map-reduce-a-really-simple-introduction-kloudo/)  
4. [Wikipedia article on mapreduce](https://en.wikipedia.org/wiki/MapReduce) 
5. [MapReduce example in mongodb docs](https://docs.mongodb.com/manual/tutorial/map-reduce-examples/#calculate-order-and-total-quantity-with-average-quantity-per-item)


Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE4OTQ3NDU3MSw4NDA0Mzg5MDJdfQ==
-->