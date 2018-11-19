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
1. Setting up the server (called EC2 in AWS language).
1. Making sure that the outer world has access to our server (setting up the group permisions).
1. Ensuring FTP access is enabled (so that we can upload files to the server)( changing the group permissions to ensure everything is allowed inside ).

So first we log in to the AWS console[^awsConsole]. Do put in your card details to complete the registration process.

Move to the EC2 page[^awsEc2] . Click on the `Launch Instance` under the 'Create Instance'. Then follow the steps below:

 - Select a suitable instance ( the first one listed, Amazon AMI, is perfect for all our needs ), click on the next button.
 - Select the correct instance type (t2 micro is perfect for this).
 - The other 3 panels, Configure instance, Add Storage and Add Tags, can be skipped, but I suggest reading everything once, just in case you need it further when you are on your own.
 - The Configure Security Group step is needed to enable traffic to the server. The default is add a new group. keep that selected. When adding the rules, select the type as 'All', source as '0.0.0.0/0' and go to the next step.
 - 'Review and Launch'. This gives you a summary of the selected options over the last 6 steps. and then...
 - Launch it!
 
 Now the server is up and running. We need to SSH into it to install the packages and then start the server.
 
 Get a key pair[^awsKeyPair]. Save the resulting .pem file safely. Use this to log into your server by SSH:
 ```bash
 ssh -i linkToPEMFile ec2-user@PublicDnsIp
 ``` 

Once in, Follow the instructions on this page[^awsInstallLamp] to install the important packages for a LAMP server.

Then, type in `sudo service httpd start` This should result in an `OK`. Then we can see the page using the Public DNS (IPv4) address. 
Now your server is online and ready to display pages.

Next up, we will use FTP to upload files to the server. This page will tell you exactly how to go about it[^awsStckOverflowFtp]. However the key thing here is the PEM file, this called the key pair, read up on this here[^awsKeyPair].  Also, remember that adding additional users is as simple[^awsEc2Users] as on a normal linux box.  


[^awsSimpleLanguage]:<https://www.expeditedssl.com/aws-in-plain-english/?>
[^awsConsole]: <https://console.aws.amazon.com>
[^awsEc2]: <https://console.aws.amazon.com/ec2>
[^awsKeyPair]: <https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html#having-ec2-create-your-key-pair>
[^awsInstallLamp]: <https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/install-LAMP.html>
[^awsStckOverflowFtp]: <https://stackoverflow.com/a/49053891>
[^awsKeyPair]: <https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html#having-ec2-create-your-key-pair>
[^awsEc2Users]: <https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/managing-users.html>

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTExNDUzNDc5MTksMTkwOTMwOTM0NSwzND
Q5MzA2NzQsMTMyMjAwMTU2OCwtNTIxNzM1OCwtNzc2NTAxMzY1
LDExNTA0MTI5NjksMTU5MTcwMzczMiwtMTY3NzQ5NjEwOCwtMz
I0MjE5OTk4LDQ0NDQ1NzM0Myw1MTA5NDQwMTAsMTg4NDU1NTk2
MCw3MzA5OTgxMTZdfQ==
-->