---
layout: post
title: "Scope and Context in JavaScript"
date: 2018-11-15T19:00:00+05:30
draft: false
tags : [programming,softwareEngineering]
Description : "Noun and Verb based software design. How this can simplify software design."
---
Today i came to know of a new thing and quite frankly, it blew my mind.  

**Thinking in terms of verbs and nouns**: This fantabulous idea was spoken to me by my mentor this evening. its also there on the web[^vnp].

so what does this mean?
consider this requirement: __we need to add a additional phone number to a user.__
so here we have verbs:
 1. add  

nouns: 
 1. user
 2. additional phone number

so we can add a new variable 'additional phone number' to a 'user' class and a new method to change this variable 'add'. This is definitely something to understand how to design your classes and methods to interact with other classes. 
another important use would be to  change contexts while programming. see above. the program here is written with reference to the user, i.e., noun based, and keeping the verb as the context, we program the nouns around it. but we can also write atomic functions where the noun is the context and the verb is passed to it. This is a functional programming paradigm and can ease the software design process there too.  

[^vnp]: (https://wbsimms.com/programming-nouns-verbs/)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwODg4MjU4MDFdfQ==
-->