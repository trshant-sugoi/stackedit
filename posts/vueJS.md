# My understanding of UI javascript frameworks.
I tried learning angularjs and reactjs. but i cannot understand those frameworks on a deeper level, which make me an inneficient programmer. I need to understand these on a much more deeper level so i can understand whats going on under the hood.   
My motive in writng this is to understand how a client facing javascript framework works. This, i believe, will help me understand the underlying system so i can debug errors faster. Such kind of frameworks are much evolved, so the nomenclature and the way of functioning, is almost the same on a superficial level. i will not be going into any code here. i will only be writing it from a 20ft view.  
Recently, i started reading through VueJS and somehow it seems to resonate with me, so i decided to read only the documentation and understand how everything comes together. Below are what i learned. 
## Terms i should know about.
### Instance
This provides a context ( or **Scope** ) for the application to work with. While you can have multiple instances on a page, it mostly is better to use just one since it simplifies things later.
### Component
This can be thought of as a collection of visually separate elements. these can be global or local, and flexibe enough to reuse the same components for different purposes 
### Directive
the logic flow of the data is managed by directives. I will deal with this in the next post where i will be looking at code.  
 
## An example 
I am going to look at my blog and see if i can make this into a VueJS application. Visually this can be separated into components. 

