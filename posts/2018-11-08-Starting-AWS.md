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

So first we log in to the AWS console[^awsConsole]. Do put in your card details to complete the registration process.
Move to the EC2 page[^awsEc2] . Click on the `Launch Instance` under the 'Create Instance'. Then follow the steps below:
 - Select a suitable instance ( the first one listed, Amazon AMI, is perfect for all our needs ), click on the next button.
 - Select the correct instance type (t2 micro is perfect for this).
 - 

[^awsSimpleLanguage]:<https://www.expeditedssl.com/aws-in-plain-english/?>
[^awsConsole]: <https://console.aws.amazon.com>
[^awsEc2]: <https://console.aws.amazon.com/ec2>

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTE5MTIxNDQ5LDExNTA0MTI5NjksMTU5MT
cwMzczMiwtMTY3NzQ5NjEwOCwtMzI0MjE5OTk4LDQ0NDQ1NzM0
Myw1MTA5NDQwMTAsMTg4NDU1NTk2MCw3MzA5OTgxMTZdfQ==
-->