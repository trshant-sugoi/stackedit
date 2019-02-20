---
title: "An essay on web components"
date: 2018-12-05T09:00:00+05:30
draft: true
tags : [programming,JavaScript,WebComponents]
Description : "My attempt at understanding of web components."
---

Components are a way to define custom HTML elements. These are reusable and since, they can be all custom JavaScript, can be shared as an  npm package. They have a home at webcomponents.org[^home].  

We have a few concepts to understand here:
 1. **Document fragment**: The individual templates of the different components will reside as Document fragments. 
 2. **Shadow Dom**: This is the part of HTML that never will render on the screen. Document fragments will be in this. As a developer, thats all we will need to know.
 3. **JavaScript web component APIs**. This link will be explain this much better than I ever will [^atGoogle].

My understanding of web components was helped in a big way because of Cory's[^blogPost1] and sitepen's[^sitepen] posts.  

So How do we start?


[^atGoogle]: (https://developers.google.com/web/fundamentals/web-components/customelements)  
[^blogPost1]: (https://coryrylan.com/blog/introduction-to-web-components)
[^sitepen]: (https://www.sitepen.com/blog/2018/07/06/web-components-in-2018/)
[^home]: (https://www.webcomponents.org/introduction)
[^moduleImport]: (https://jakearchibald.com/2017/es-modules-in-browsers/)

> Written with [StackEdit](https://stackedit.io/).


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTgxNTUwNTE4MywtODI2MzkyNjMyLC04OD
AyNjI5MDFdfQ==
-->