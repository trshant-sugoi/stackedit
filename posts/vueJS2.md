---
title: "A dive into UI javascript frameworks - Part 2"
date: 2018-07-05T01:21:43+05:30
draft: false
tags : [Javascript,javascript frameworks,VueJS]
Description: "I tried learning AngularJS and React. But I cannot understand those frameworks on a deeper level. My aim in writing this set of posts is to have an idea what's going on under the hood. This post goes thru directives and understanding the philosophy of presentation logic that these frameworks specialize in."
---
In this post I will be laying out an idea of how to build a front page for a blog using the components, instances laid out in my previous post, using directives to achieve our goal. 
But I will need to understand the idea behind this so This post will be about learning and be testing things out, this will help me in taking good decisions finishing the blog code. 
Along the way, I will be writing code to test my ideas. So, writing a small page to test my code, I begin with forking the hello world example from the [official guide](https://vuejs.org/v2/guide/).

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
Now, if you copy that into an HTML file and then open it, you will be greeted with a "Hello Vue!" message. If you open your console log and type in app.message = "Hello Trshant!", you will find that the message has changed to whatever you typed. This means that the data in the app is coupled with the {{message}} part of the HTML; and if we change the data using ajax, it will make the necessary change in the presentation. _awesome!_   

Moving on, I have copied this lovely todo app made in Vue and forked it -> [There you go](https://jsfiddle.net/trshant/oqka1f8p/1/). Do please open it and go thru the code and the example itself. I will go through this and explain the functionality of every line. my motive here is to understand the need for bindings and presentation logic.  

I will be going thru the HTML and then the JS. But before we do that, we will ask ourselves the important questions - The Objective/Brief of our task.  

We want to build a small to-do app. This should have a text box and a button next to it, on the top. when you type in something and hit the button or press enter, this should populate underneath, with a checkbox to its left. we also need a delete button. When you click the checkbox, the text should be struck out.  

Since we have some clarity on what we need, we move on to the code. Do have a look:

```html
<!-- Main Div Holding our Application Data -->
<div class="container" id="todo">
  <!-- Panel for holding our input -->
  <section class="panel">
    <input type="checkbox" id="mark-all" v-bind:checked="areAllSelected" v-on:click="selectAll">
    <input type="text" placeholder="What do you need to do?" autofocus class="text-input" v-model="newTask" v-on:keyup.enter="addTask">
    <button v-on:click="clearList">Clear List</button>
  </section>
  <!-- Unordered list for holding our todo items -->
  <ul class="list">
    <li v-for="task in taskList" v-bind:class="{done: task.checked}">
      <input type="checkbox" class="checkbox" v-model="task.checked">
      <label for="checkbox">{{ task.text }}</label>
      <button class="delete" v-on:click="removeTask(task)">X</button>
    </li>
  </ul>
  <!-- This stringifies the contents of the data object and displays it on the page -->
  <pre>{{ $data }}</pre>
</div>
```

**The main input with button** : look at the contents of the `<section class="panel">` element. So we have a checkbox (which is not in the brief above the code), an input and a button. All this is in HTML..but whats the v-on and v-bind and v-model?  
These are called directives. They are very very important and so, we should understand what they do. These are event listeners and provide binding with the data source or functions that we will build.  
Here, we have a few directives. I will list them and provide an explanation:  
  - **v-bind**: This binds an attribute of the element with the output of a function, which is constantly evaluated, or some data element. here we see `v-bind:checked="areAllSelected"` - this binds the output of a _constantly evaluated function_ areAllSelected to the _checked_ property of the checkbox.  
  - **v-on**: This is an event listener. This executes a function on the occurrence of that event. `v-on:click="selectAll"` - here the function selectAll is executed when the click event executes on this element. Another instance of the v-on is the `v-on:keyup.enter="addTask"`. Intuitively, you can say that this is supposed to execute addTask on the event of the enter button is released.  
  - **v-model**: This binds the data to the element value when that value is an attribute. 

We will now go through the rest of the code - the `ul` element. We encounter something different here - the `v-for="task in taskList"` bit. This is a 'for' loop. it loops through each element ( called _task_ ) in the data _taskList_. 

I think we can now go thru the Javascript and will find it self-explanatory. 
