---
layout: post
title: "Starting off with AWS - static site setup"
date: 2018-11-08T07:51:43+05:30
draft: true
tags : [AWS , starting , development ]
Description : "I started off using AWS. This is a basically a documentation of how i set up a simple static site using EC2"
---
Do read through AWS in simple english[^awsSimpleLanguage] to figure out what we are going to do here. What we are trying to accomplish is simply to host a static site.
This involves us:
- Setting up the server (called EC2 in AWS language).
- Making sure that the outer world has access to our server (setting up the group permisions).
- Ensuring FTP access is enabled (so that we can upload files to the server)( changing the group permissions to ensure everything is allowed inside ).
- Accessing the site.( using the elastic IP ) 

So first we log in to the AWS console. put in your card details. 

[^awsSimpleLanguage]:<https://www.expeditedssl.com/aws-in-plain-english/?>

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTk0MjA0MjQ5OCwtMTY3NzQ5NjEwOCwtMz
I0MjE5OTk4LDQ0NDQ1NzM0Myw1MTA5NDQwMTAsMTg4NDU1NTk2
MCw3MzA5OTgxMTZdfQ==
-->