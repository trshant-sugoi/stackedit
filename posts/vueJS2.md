---
title: "A dive into UI javascript frameworks - Part 2"
date: 2018-07-05T01:21:43+05:30
draft: false
tags : [Javascript,JavscriptFrameworks,VueJS]
Description : "I tried learning angularjs and reactjs. but i cannot understand those frameworks on a deeper level, which make me an inneficient programmer. My aim in writing this set of posts is to have an idea what's going on under the hood. This post goes thru directives and understanding the philosophy of presentation logic that these frameowrks specialise in."
---
In this post i will be laying out an idea of how to build a front page for a blog using the components, instances laid out in my previous post, using directives to achieve our goal. 
But i will need to understand the idea behind this so This post will be about learning and testing things out, this will help me in taking good decisions finishing the blog code. 
Along the wa, i will be writing code to test my ideas. So, writing a small page to test my code, i begin with forking the hello world example from the [official guide](https://vuejs.org/v2/guide/).

```JavaScript
<!DOCTYPE html>
<html>
<head>
  <title>My first Vue app</title>
  <!-- development version, includes helpful console warnings -->
  <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
</head>
<body>
  <div id="app">
    {{ message }}
  </div>

  <script>
    var app = new Vue({
      el: '#app',
      data: {
        message: 'Hello Vue!'
      }
    })
  </script>
</body>
</html>
```
Now, if you copy that into an html file and then open it, you will be greeted with a "Hello Vue!" message. If you open your console log and type in app.message = "Hello Trshant!", you will find that the message has changed to whatever you typed. This means that the data in the app is coupled with the {{message}} part of the html; and if we change the data using ajax, it will make the nessacery change in the presentation. _awesome!_   

Moving on, i have copied this lovely todo app made in Vue and forked it -> [There you go](https://jsfiddle.net/trshant/oqka1f8p/1/). Do please open it and go thru the code and the example itself. i will go through this and explain the functionality of every line. my motive here is to understand the need for bindings and presentation logic. 






