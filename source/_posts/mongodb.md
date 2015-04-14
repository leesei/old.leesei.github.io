title: "MongoDB"
date: 2014-12-17 12:35:01
categories:
- app
tags:
- mongodb
- notes
toc: true
---

## drop database

```
> show dbs
db1      0.03412GB
local   0.078125GB
sessions        0.203125GB
> use db1
switched to db db1
> db.dropDatabase()
{ "dropped" : "db1", "ok" : 1 }
> show dbs
local   0.078125GB
sessions        0.203125GB
```

## reference

http://docs.mongodb.org/manual/reference/
