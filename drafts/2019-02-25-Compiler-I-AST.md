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
User ->> Compiler: File  

Compiler ->> Lexical Analyser: Tokenise  
Lexical Analyser ->> Syntax Analysis: Create Parse Tree 
```

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIwNDkzMTA4MDEsMTUxMzcyMDc1OSwxNT
g1MjY3MTQ0LDgzMTc3MjMwXX0=
-->