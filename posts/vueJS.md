---
title: "A dive into UI javascript frameworks"
date: 2018-07-01T07:51:43+05:30
draft: false
tags : [Javascript,JavscriptFrameworks]
Description : "I tried learning angularjs and reactjs. but i cannot understand those frameworks on a deeper level, which make me an inneficient programmer. My aim in writing this set of posts is to have an idea what's going on under the hood."
---
My motive in writing this is to understand how a client facing JavaScript framework works at a deeper level. This, i believe, will help me understand the underlying system so i can architect the system correctly. Such kind of frameworks are evolved, so the nomenclature and the way of functioning, is almost the same on a superficial level. i will not be going into any code here. i will only be writing it from a 200ft view.  
Recently, i started reading through VueJS and somehow it seems to resonate with me, so i decided to read only the documentation and understand how everything comes together. Below are what i learned. 
## Terms i should know about.
### Instance
This provides a context ( or **Scope** ) for the application to work with. While you can have multiple instances on a page, it mostly is better to use just one since it simplifies things later.
### Component
This can be thought of as a collection of visually separate elements. these can be global or local, and flexibe enough to reuse the same components for different purposes 
### Directive
the logic flow of the data is managed by directives. I will deal with this in the next post where i will be looking at code.  
 
## An example 
I am going to look at a blog's front page layout and see if i can make this into a VueJS application. Visually this can be separated into components. 

![Layout of components](https://i.imgur.com/HlMWRaK.jpg)

Now we can see 1 instance, 3 different components, one of which is used 2 times with different data. Just so that we get this right avoiding too much confusion about what goes where, i will concentrate on the components:

**header** - This is just the header, with a list of links and a banner image.  
**list_posts_with_description** - This component gives a list of post titles, with a date and description.   
**list_of_post_titles** - This component gives a list of post titles. it is reused twice. once to show the list using date as the grouping  and the second time using a tag as the grouping. 

In the next post, i will write the code for each of the components.
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTEzNjIyOTEwNV19
-->