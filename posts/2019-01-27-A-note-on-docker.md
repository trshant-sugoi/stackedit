---
layout: post
title: "Noun and verb based programming"
date: 2019-01-27T19:00:00+05:30
draft: false
tags : [programming,softwareEngineering,docker]
Description : "A note on Docker."
---
Docker is a buzzword right now.  
It is a lightweight virtualisation system, which does not add to your system and maintains developer sanity.  
Since its not a full blown VM, git handles things beautifully. your configured dev environment can be moved to the production system, setting only the environment variable in place for the respective production/test/dev systems. And you get to save some HDD space, which is also quite expensive.  
Basically, you are leaving nothing to chance. And using kubernetes, you can maintain all your containers.  
Before we go into the article, we both need to know what I will only be explaining a few key concepts in the docker world. Once we understand these, we can go forward to learning about them.  
The main terms to understand here are:  
**1. files** : These are the files you need dockerised.  
**2. images** : These are the systems you want to encapsulate the files in.    
**3. container** : These are what we build using the images and files.  
Simple enough, I suppose!

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTc2Nzk5NjQxOCwtMTM0NjQyNTg4OV19
-->