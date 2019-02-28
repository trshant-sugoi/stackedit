---
title: "Building a compiler-part1. AST"
date: 2019-01-27T19:00:00+05:30
draft: false
tags : [CompSci,compilerTheory,AST]
Description : "Building your own compiler (Part 1): How to build a Abstract Syntax Tree"
---  
**What is an AST?**:


**Define your rules**:  

---  
**Define your grammer**:  

Below diagram is based on [Vaidehi Joshi's](https://medium.com/basecs/leveling-up-ones-parsing-game-with-asts-d7a6fc2400ff) awesome post on ASTs:

```mermaid
sequenceDiagram
participant U as User  
participant C as Compiler   
participant S as Scanner
participant T as Tokeniser   
participant SA1 as CST
participant SA2 as AST 

Note over S,T: Lexical Analysis
Note over SA1,SA2: Syntax Analysis
U ->> C  : File  
Note over C: " 5+(1*12) "
C ->> S  : String
Note over S: Strip text <br/>"5+(1*12)"
S ->> T  : lexemes  
Note over T: Convert to Tokens<br/>["5","+","(","1","*","12",")"]
T ->> SA1 : Tokenised   
Note over SA1: Create a Parse Tree
SA1  ->> SA2 : CST
Note over SA2: Optimise the Parse Tree
SA2  ->> Next level of compiling: AST 
Note over C: Post Compilation
C ->> U: Executable  
```  

* CST : Concrete Syntax tree
	```
	graph TD
		B["fa:fa-twitter for peace"]
		B-->C[fa:fa-ban forbidden]
	        B-->D(fa:fa-spinner);
	        B-->E(A fa:fa-camera-retro perhaps?);
	```
* AST : Abstract Syntax tree

To understand and see these in action, Do try out <https://astexplorer.net/>. This site is amazing and will make you see in action building of an AST.  

Many thanks to <https://mermaidjs.github.io> for the sequence diagram. It is truly a pleasure to work with.  

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTQ4MjYwMDI4NSwtMTY3NTE1NjczNSwtMT
A4Mzk5MjY3MiwxODY0OTIzNDU1LC0zNDAyMDczMTEsNDYzMzYw
MDYxLC00MTQ3NDY3NjUsLTE2MjMyNTQzNjEsMTUxMzcyMDc1OS
wxNTg1MjY3MTQ0LDgzMTc3MjMwXX0=
-->