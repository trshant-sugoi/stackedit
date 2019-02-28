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
participant S as Lexical Analysis: Scanner
participant T as Lexical Analysis: Tokeniser   
participant SA1 as Syntax Analysis: CST
participant SA2 as Syntax Analysis: AST 

U ->> C  : File  
Note over C: "5+(1 )"
C ->> S  : String
Note over S: Strip text
S ->> T  : lexemes 
Note over T: Convert to Tokens
T ->> SA1 : Tokenised   
Note over SA1: Create a Parse Tree
SA1  ->> SA2 : CST
Note over SA2: Optimise the Parse Tree
SA2  ->> Next level of compiling: AST 
Note over C: Post Compilation
C ->> U: Executable  
```  

* CST : Concrete Syntax tree
* AST : Abstract Syntax tree

To understand and see these in action, Do try out <https://astexplorer.net/>. This site is amazing and will make you see in action building of an AST.  

Many thanks to <https://mermaidjs.github.io> for the sequence diagram. It is truly a pleasure to work with.  

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTc4NTI2MzA5MywxODY0OTIzNDU1LC0zND
AyMDczMTEsNDYzMzYwMDYxLC00MTQ3NDY3NjUsLTE2MjMyNTQz
NjEsMTUxMzcyMDc1OSwxNTg1MjY3MTQ0LDgzMTc3MjMwXX0=
-->