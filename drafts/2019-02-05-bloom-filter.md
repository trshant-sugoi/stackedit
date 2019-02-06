---
title: "Implementing A Bloom Filter"
date: 2018-07-01T07:51:43+05:30
draft: false
tags : [Algorithm , BloomFilter]
Description : "A note on implementing a bloom filter"
---

Here is how the interaction between the client/server will take place:
```mermaid
sequenceDiagram
Client ->> Server: Hi! here's my master hash
Server ->> Database: SQL
Note left of Database: Here is where<br/>the thinking <br/>happens.
Database ->> Server: Data not in the client
Server ->> Client: There you go....
```

Murmur Hash : The master hash is the ANDed product of all the individual hashes. The hashing function used here is the murmur hash which has a lot of improvements over the normal SHA256. In NodeJS, this is how we use it.




> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTE1MDMzMTIwNCw0MDMxMjMzMjJdfQ==
-->