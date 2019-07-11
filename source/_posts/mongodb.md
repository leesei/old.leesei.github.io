---
title: "MongoDB"
date: 2014-12-17 12:35:01
categories:
- app
tags:
- mongodb
- notes
toc: true
---

> MongoDB after 3.6 uses [SSPL](https://www.mongodb.com/licensing/server-side-public-license)

[MongoDB for GIANT Ideas | MongoDB](https://www.mongodb.com/)
[MongoDB University Online Courses](https://university.mongodb.com/courses/catalog)

[About M001](https://university.mongodb.com/courses/M001/about)
[M040: New Features and Tools in MongoDB 4.0](https://university.mongodb.com/courses/M040/about)

[Reference — MongoDB Manual](https://docs.mongodb.com/manual/reference/)
[The MongoDB 4.0 Manual — MongoDB Manual](https://docs.mongodb.com/manual/)
[MongoDB - Back to Basics - YouTube](https://www.youtube.com/playlist?list=PLyROlY1vFlbdA45cHtcId5NLxPDHJ_lpb)

[MongoDB Tutorials | Studio 3T](https://studio3t.com/knowledge-base/categories/mongodb-tutorials/)
[MongoDB Tutorial for Beginners - YouTube](https://www.youtube.com/playlist?list=PL4cUxeGkcC9jpvoYriLI0bY8DOgWZfi6u)

[MongoDB: A Beginner’s Guide – Bret Cameron – Medium](https://medium.com/@bretcameron/mongodb-a-beginners-guide-8fca0c7787a4)
[Stock Price Notifications with Mongoose and MongoDB Change Streams | www.thecodebarbarian.com](http://thecodebarbarian.com/stock-price-notifications-with-mongoose-and-mongodb-change-streams.html)

[karlseguin/the-little-mongodb-book: The Little MongoDB Book](https://github.com/karlseguin/the-little-mongodb-book) 2.6

## `mongod` server

[mongod — MongoDB Manual](https://docs.mongodb.com/manual/reference/program/mongod/)
[Authentication — MongoDB Manual](https://docs.mongodb.com/manual/core/authentication/)
[Role-Based Access Control — MongoDB Manual](https://docs.mongodb.com/manual/core/authorization/)

[Booting a mongoDB container with user specified credentials | Lakshmi Narasimhan](https://www.lakshminp.com/docker-mongodb)

[docker-library/mongo: Docker Official Image packaging for MongoDB](https://github.com/docker-library/mongo)
[docs/README.md at master · docker-library/docs](https://github.com/docker-library/docs/blob/master/mongo/README.md)

[bitnami/bitnami-docker-mongodb: Bitnami MongoDB Docker Image](https://github.com/bitnami/bitnami-docker-mongodb)

## `mongo` client

[mongo — MongoDB Manual](https://docs.mongodb.com/manual/reference/program/mongo/)
[mongo Shell Quick Reference — MongoDB Manual](https://docs.mongodb.com/manual/reference/mongo-shell/)
[Operators — MongoDB Manual](https://docs.mongodb.com/manual/reference/operator/)
[MongoDB CRUD Operations — MongoDB Manual](https://docs.mongodb.com/manual/crud/)

```
mongo --host host --port port -u database

# show databases
> show dbs
# use a database
> use <db_name>

# show collections
> show collections

# operations
> db.<collection>.<operation>(<options>)
# query
> db.foo.find({name: 'bar'})

## drop database
> use db1
switched to db db1
> db.dropDatabase()
{ "dropped" : "db1", "ok" : 1 }
> show dbs
local   0.078125GB
sessions        0.203125GB
```

Using `mongo` in shell script:

```sh
mongo "$rootAuthDatabase" <<-EOJS
                db.createUser({
                    user: $(_js_escape "$MONGO_INITDB_ROOT_USERNAME"),
                    pwd: $(_js_escape "$MONGO_INITDB_ROOT_PASSWORD"),
                    roles: [ { role: 'root', db: $(_js_escape "$rootAuthDatabase") } ]
                })
            EOJS
```

### `mongodump`/`mongorestore`

[mongodump — MongoDB Manual](https://docs.mongodb.com/manual/reference/program/mongodump/)
Dump the database in binary.

### `mongoexport`

[mongoexport — MongoDB Manual](https://docs.mongodb.com/manual/reference/program/mongoexport/)

```sh
mongoexport --db test --collection traffic --out traffic.json 
mongoexport --db users --collection contacts --type=csv --fields name,address --out /opt/backups/contacts.csv
# fieldFile can be used for CSV
```

## On the contrary

[Why You Should Never Use MongoDB « Sarah Mei](http://www.sarahmei.com/blog/2013/11/11/why-you-should-never-use-mongodb/)
[Why you should never, ever, ever use MongoDB - joepie91's Ramblings](http://cryto.net/~joepie91/blog/2015/07/19/why-you-should-never-ever-ever-use-mongodb/)
[MongoDB queries don’t always return all matching documents! — Meteor Engineering](https://engineering.meteor.com/mongodb-queries-dont-always-return-all-matching-documents-654b6594a827#.9h3o08c1d)

## Benchmark

[Comparing MongoDB performance on public clouds: AWS, Azure & DigitalOcean](https://scalegrid.io/blog/comparing-mongodb-performance-on-public-clouds-aws-azure-digital-ocean/)

## Schema Validation

[Schema Validation — MongoDB Manual](https://docs.mongodb.com/manual/core/schema-validation/)
[$jsonSchema — MongoDB Manual](https://docs.mongodb.com/manual/reference/operator/query/jsonSchema/#op._S_jsonSchema)
[draft-fge-json-schema-validation-00 - JSON Schema: interactive and non interactive validation](https://tools.ietf.org/html/draft-fge-json-schema-validation-00)

[JSON Schema | The home of JSON Schema](http://json-schema.org/)
[jsonSchema attribute conditionally required - Stack Overflow](https://stackoverflow.com/questions/38717933/jsonschema-attribute-conditionally-required)
[jsonschema - JSON schema: conditional dependency - Stack Overflow](https://stackoverflow.com/questions/47674950/json-schema-conditional-dependency)

Showing validation rules:  
```
db.getCollectionInfos({name: "myCollection"})
```

[Mongoose ODM](https://mongoosejs.com/) client side ORM and validation

## Scaling

[Replication — MongoDB Manual](https://docs.mongodb.com/manual/replication/)
[Sharding — MongoDB Manual](https://docs.mongodb.com/manual/sharding/)

[MongoDB is web scale](http://www.mongodb-is-web-scale.com/)
[Indexing, Replicating, and Sharding in MongoDB [Tutorial] | Packt Hub](https://hub.packtpub.com/indexing-replicating-and-sharding-in-mongodb-tutorial/)
[Configuring a MongoDB Replica Set for Analytics - DZone Database](https://dzone.com/articles/configuring-a-mongodb-replica-set-for-analytics)

## Data Modeling

[Data Modeling Introduction — MongoDB Manual](https://docs.mongodb.com/manual/core/data-modeling-introduction/)
[Model Data for Atomic Operations — MongoDB Manual](https://docs.mongodb.com/master/tutorial/model-data-for-atomic-operations/)

[Modelling Entity Relations In MongoDB | Alexander Paterson](https://alexanderpaterson.com/posts/modelling-entity-relations-in-mongodb) populating reference with `$match` and `$unwind`
[如何将关系型数据导入MongoDB？](http://www.infoq.com/cn/articles/migrate-from-rmdb-mongodb)
[Aggregation Pipeline Operators — MongoDB Manual](https://docs.mongodb.com/manual/reference/operator/aggregation/)
[mongoose: Referencing schema in properties or arrays | Alexander Zeitler](https://alexanderzeitler.com/articles/mongoose-referencing-schema-in-properties-and-arrays/)

[A Node.js Perspective on MongoDB 3.4: Collations | www.thecodebarbarian.com](http://thecodebarbarian.com/a-nodejs-perspective-on-mongodb-34-collations)

[Thinking in Documents: Part 1 | MongoDB](https://www.mongodb.com/blog/post/thinking-documents-part-1)
[Thinking in Documents: Part 2 | MongoDB](https://www.mongodb.com/blog/post/thinking-documents-part-2)
[MongoDB - Thinking in Documents - agile-code.com](https://www.agile-code.com/blog/mongodb-thinking-in-documents/)

[6 Rules of Thumb for MongoDB Schema Design: Part 1 | MongoDB](https://www.mongodb.com/blog/post/6-rules-of-thumb-for-mongodb-schema-design-part-1)
[6 Rules of Thumb for MongoDB Schema Design: Part 2 | MongoDB](https://www.mongodb.com/blog/post/6-rules-of-thumb-for-mongodb-schema-design-part-2)
[6 Rules of Thumb for MongoDB Schema Design: Part 3 | MongoDB](https://www.mongodb.com/blog/post/6-rules-of-thumb-for-mongodb-schema-design-part-3)

## Tips and Tricks

[Perform Two Phase Commits — MongoDB Manual](https://docs.mongodb.com/manual/tutorial/perform-two-phase-commits/)
[Expire Data from Collections by Setting TTL — MongoDB Manual](https://docs.mongodb.com/manual/tutorial/expire-data/)

[A Node.js Perspective on MongoDB 4.0: Transactions | www.thecodebarbarian.com](http://thecodebarbarian.com/a-node-js-perspective-on-mongodb-4-transactions.html)
