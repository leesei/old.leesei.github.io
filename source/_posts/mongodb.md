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

[MongoDB 4.2 vs 4.0, 3.6, 3.4, and 3.2 Benchmarks - hartator - Medium](https://medium.com/@hartator/mongodb-4-2-vs-4-0-3-6-3-4-and-3-2-benchmarks-ee96a09ef231)
3.4 is faster

[About M001](https://university.mongodb.com/courses/M001/about)
[M040: New Features and Tools in MongoDB 4.0](https://university.mongodb.com/courses/M040/about)

[Reference — MongoDB Manual](https://docs.mongodb.com/manual/reference/)
[The MongoDB 4.0 Manual — MongoDB Manual](https://docs.mongodb.com/manual/)
[MongoDB - Back to Basics - YouTube](https://www.youtube.com/playlist?list=PLyROlY1vFlbdA45cHtcId5NLxPDHJ_lpb)

[MongoDB Tutorials | Studio 3T](https://studio3t.com/knowledge-base/categories/mongodb-tutorials/)
[MongoDB Tutorial for Beginners - YouTube](https://www.youtube.com/playlist?list=PL4cUxeGkcC9jpvoYriLI0bY8DOgWZfi6u)
[Manipulating Data With MongoDB. Learn the basics of CRUD with PyMongo | by Benedict Soh | Towards Data Science](https://towardsdatascience.com/manipulating-data-with-mongodb-bd561f09d76a)

[MongoDB: A Beginner’s Guide – Bret Cameron – Medium](https://medium.com/@bretcameron/mongodb-a-beginners-guide-8fca0c7787a4)
[Stock Price Notifications with Mongoose and MongoDB Change Streams | www.thecodebarbarian.com](http://thecodebarbarian.com/stock-price-notifications-with-mongoose-and-mongodb-change-streams.html)

[karlseguin/the-little-mongodb-book: The Little MongoDB Book](https://github.com/karlseguin/the-little-mongodb-book) 2.6

[Simple Steps to Optimize Your App Performance with MongoDB, Redis, and Node.js - By](https://hackernoon.com/simple-steps-to-optimize-your-app-performance-5700d8b58f58)
[Performance Best Practices: Hardware and OS Configuration | MongoDB](https://www.mongodb.com/blog/post/performance-best-practices-hardware-and-os-configuration)

## Percona Server for MongoDB

[MongoDB Runs Better with Percona](https://www.percona.com/solutions/mongodb-runs-better-with-percona)
[Percona Server for MongoDB](https://www.percona.com/software/mongodb/percona-server-for-mongodb)

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
[mongo Shell Methods — MongoDB Manual](https://docs.mongodb.com/manual/reference/method/)

[MongoDB CRUD Operations — MongoDB Manual](https://docs.mongodb.com/manual/crud/)
[Operators — MongoDB Manual](https://docs.mongodb.com/manual/reference/operator/)

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

[mongodump — MongoDB Database Tools](https://docs.mongodb.com/database-tools/mongodump/)
[mongorestore — MongoDB Database Tools](https://docs.mongodb.com/database-tools/mongorestore/)

```sh
mongodump --archive="mongodump-test-db" --db=test
# with database name change
mongorestore --archive="mongodump-test-db" --nsFrom='test.*' --nsTo='examples.*'
```

### `mongoexport`/`mongoimport`

[mongoexport — MongoDB Database Tools](https://docs.mongodb.com/database-tools/mongoexport/)
[mongoimport — MongoDB Database Tools](https://docs.mongodb.com/database-tools/mongoimport/)

```sh
mongoexport --db test --collection traffic --out traffic.json
mongoexport --db users --collection contacts --type=csv --fields name,address --out /opt/backups/contacts.csv
# fieldFile can be used for CSV
```

```sh
mongoimport --db test --collection traffic traffic.json
# the CSV has header line
mongoexport --db users --collection contacts --type=csv --headerline contacts.csv
```

## Admin UI

[mongo-express - Docker Hub](https://hub.docker.com/_/mongo-express)
[mongo-express/mongo-express: Web-based MongoDB admin interface, written with Node.js and express](https://github.com/mongo-express/mongo-express)
[Too fast, too insecure: Securing Mongo Express web administrative interfaces - Help Net Security](https://www.helpnetsecurity.com/2019/04/26/securing-mongo-express-web-administrative-interfaces/)

## On the contrary

[Why You Should Never Use MongoDB « Sarah Mei](http://www.sarahmei.com/blog/2013/11/11/why-you-should-never-use-mongodb/)
[Why you should never, ever, ever use MongoDB - joepie91's Ramblings](http://cryto.net/~joepie91/blog/2015/07/19/why-you-should-never-ever-ever-use-mongodb/)
[MongoDB queries don’t always return all matching documents! — Meteor Engineering](https://engineering.meteor.com/mongodb-queries-dont-always-return-all-matching-documents-654b6594a827#.9h3o08c1d)

## #perfmatters

[Comparing MongoDB performance on public clouds: AWS, Azure & DigitalOcean](https://scalegrid.io/blog/comparing-mongodb-performance-on-public-clouds-aws-azure-digital-ocean/)

[Analyze Query Performance — MongoDB Manual](https://docs.mongodb.com/manual/tutorial/analyze-query-plan/)
[Query Plans — MongoDB Manual](https://docs.mongodb.com/manual/core/query-plans/)

[Partitions — MongoDB Realm](https://docs.mongodb.com/realm/sync/partitions/)
[Partition Strategies — MongoDB Realm](https://docs.mongodb.com/realm/sync/partition-strategies/#std-label-partition-strategies)

## Indexes

[MongoDB Performance 101: How To Improve the Speed of MongoDB App](https://medium.com/better-programming/mongodb-performance-101-how-to-improve-the-speed-of-mongodb-app-a59f2390ee5)
[Indexing Strategies — MongoDB Manual](https://docs.mongodb.com/manual/applications/indexes/)

[Indexes — MongoDB Manual](https://docs.mongodb.com/manual/indexes/)
[Compound Indexes — MongoDB Manual](https://docs.mongodb.com/manual/core/index-compound/)
[Multikey Indexes — MongoDB Manual](https://docs.mongodb.com/manual/core/index-multikey/) for arrays in documents
[Hashed Indexes — MongoDB Manual](https://docs.mongodb.com/manual/core/index-hashed/) when index field > 1024 bytes
[db.collection.createIndex() — MongoDB Manual](https://docs.mongodb.com/manual/reference/method/db.collection.createIndex/)

[[SERVER-3294] Ability to keep data on disk in ~ index order - MongoDB Jira](https://jira.mongodb.org/browse/SERVER-3294) WiredTiger does not implement index clustering

## Sessions API

Since 3.6, provides causal consistency, multi-document transactions

[Transactions | MongoDB](https://www.mongodb.com/transactions)
[Transactions — MongoDB Manual](https://docs.mongodb.com/master/core/transactions/)
[Session — MongoDB Manual](https://docs.mongodb.com/manual/reference/method/Session/)

[Mongoose: Transactions](https://mongoosejs.com/docs/transactions.html)

## Schema Validation

[Schema Validation — MongoDB Manual](https://docs.mongodb.com/manual/core/schema-validation/)
[$jsonSchema — MongoDB Manual](https://docs.mongodb.com/manual/reference/operator/query/jsonSchema/#op._S_jsonSchema)

> see `serialization.md#json-schema`

Showing validation rules:

```
db.getCollectionInfos({name: "myCollection"})
```

[Mongoose ODM](https://mongoosejs.com/) client side ORM and validation
[Introduction to Mongoose for MongoDB](https://www.freecodecamp.org/news/introduction-to-mongoose-for-mongodb-d2a7aa593c57/)

## Scaling

[Replication — MongoDB Manual](https://docs.mongodb.com/manual/replication/)
[Sharding — MongoDB Manual](https://docs.mongodb.com/manual/sharding/)

[MongoDB is web scale](http://www.mongodb-is-web-scale.com/)
[Indexing, Replicating, and Sharding in MongoDB [Tutorial] | Packt Hub](https://hub.packtpub.com/indexing-replicating-and-sharding-in-mongodb-tutorial/)
[Configuring a MongoDB Replica Set for Analytics - DZone Database](https://dzone.com/articles/configuring-a-mongodb-replica-set-for-analytics)

## Data Modeling

[Data Modeling Introduction — MongoDB Manual](https://docs.mongodb.com/manual/core/data-modeling-introduction/)
[Database References — MongoDB Manual](https://docs.mongodb.com/manual/reference/database-references/)
[Model Data for Atomic Operations — MongoDB Manual](https://docs.mongodb.com/master/tutorial/model-data-for-atomic-operations/)

[Modelling Entity Relations In MongoDB | Alexander Paterson](https://alexanderpaterson.com/posts/modelling-entity-relations-in-mongodb) populating reference with `$match` and `$unwind`
[如何将关系型数据导入 MongoDB？](http://www.infoq.com/cn/articles/migrate-from-rmdb-mongodb)

[Mongoose v5.12.13: Query Population](https://mongoosejs.com/docs/populate.html)
[mongoose: Referencing schema in properties or arrays | Alexander Zeitler](https://alexanderzeitler.com/articles/mongoose-referencing-schema-in-properties-and-arrays/)

[A Node.js Perspective on MongoDB 3.4: Collations | www.thecodebarbarian.com](http://thecodebarbarian.com/a-nodejs-perspective-on-mongodb-34-collations)

[Thinking in Documents: Part 1 | MongoDB](https://www.mongodb.com/blog/post/thinking-documents-part-1)
[Thinking in Documents: Part 2 | MongoDB](https://www.mongodb.com/blog/post/thinking-documents-part-2)
[MongoDB - Thinking in Documents - agile-code.com](https://www.agile-code.com/blog/mongodb-thinking-in-documents/)

[6 Rules of Thumb for MongoDB Schema Design: Part 1 | MongoDB](https://www.mongodb.com/blog/post/6-rules-of-thumb-for-mongodb-schema-design-part-1)
[6 Rules of Thumb for MongoDB Schema Design: Part 2 | MongoDB](https://www.mongodb.com/blog/post/6-rules-of-thumb-for-mongodb-schema-design-part-2)
[6 Rules of Thumb for MongoDB Schema Design: Part 3 | MongoDB](https://www.mongodb.com/blog/post/6-rules-of-thumb-for-mongodb-schema-design-part-3)

## Aggregation

> MongoDB 5.0 deprecated map-reduce and improved aggregation pipeline

[Aggregation — MongoDB Manual](https://docs.mongodb.com/manual/aggregation/)
[Aggregation Reference — MongoDB Manual](https://docs.mongodb.com/manual/reference/aggregation/)
[Aggregation Pipeline Operators — MongoDB Manual](https://docs.mongodb.com/manual/reference/operator/aggregation/)

## Tips and Tricks

[Perform Two Phase Commits — MongoDB Manual](https://docs.mongodb.com/manual/tutorial/perform-two-phase-commits/)

[A Node.js Perspective on MongoDB 4.0: Transactions | www.thecodebarbarian.com](http://thecodebarbarian.com/a-node-js-perspective-on-mongodb-4-transactions.html)

[Backup MongoDB inside of Docker the right way - cupcakearmy](https://blog.nicco.io/2019/08/15/backup-mongodb-inside-of-docker-the-right-way/)

[Using MongoDB as realtime DB with nodeJS. - Noteworthy - The Journal Blog](https://blog.usejournal.com/using-mongodb-as-realtime-db-with-nodejs-c6f52c266750) need replica sets instead of stand along server

[How to traverse MongoDB super-large collections efficiently? | Develop Paper](https://developpaper.com/how-to-traverse-mongodb-super-large-collections-efficiently/)
[Henrique S. Coelho - hcoelho.com - Fixing memory problems with Node.js and Mongo DB](https://hcoelho.com/blog/33/Fixing_memory_problems_with_Node.js_and_Mongo_DB)

[node.js - Mongoose (mongodb) batch insert? - Stack Overflow](https://stackoverflow.com/questions/16726330/mongoose-mongodb-batch-insert/24848148#24848148) no need to use Bulk API, `Model.collection.insertMany()` is fast enough (and without out of heap issue) (`Model.insertMany()` suffers from these issues)
[javascript - Bulk insert in MongoDB using mongoose - Stack Overflow](https://stackoverflow.com/questions/37379180/bulk-insert-in-mongodb-using-mongoose/37379532)
[Bulk Operations in MongoDB - dbKoda - Medium](https://medium.com/dbkoda/bulk-operations-in-mongodb-ed49c109d280)
[Guy Harrison - Yet Another Database Blog - Bulk inserts in MongoDB](http://guyharrison.squarespace.com/blog/2016/11/7/bulk-inserts-in-mongodb.html)

[feliixx/mgodatagen: Generate random data for MongoDB](https://github.com/feliixx/mgodatagen)

### TTL/Auto expiry

Create index on a date field with `expireAfterSeconds` option

```js
db.collection.createIndex({ createdAt: 1 }, { expireAfterSeconds: 60 }); // auto field (Mongoose)
db.collection.createIndex({ expireAt: 1 }, { expireAfterSeconds: 0 }); // manual field
```

Using manual field you can change the expire period without recreating the index.

[TTL Indexes — MongoDB Manual](https://docs.mongodb.com/manual/core/index-ttl/)
[Expire Data from Collections by Setting TTL — MongoDB Manual](https://docs.mongodb.com/manual/tutorial/expire-data/)
[How to Erase Expired Docs Automatically with MongoDB (TTL index) | Hacker Noon](https://hackernoon.com/how-to-erase-expired-docs-automatically-with-mongodb-ttl-index-97283wll)
[MongoDB Auto Expire Documents - DEV Community](https://dev.to/sks147/mongodb-auto-expire-documents-6c9)

---

## MangoDB

[A truly Open Source MongoDB alternative - getmango](https://www.mangodb.io/) expose PostgreSQL as MongoDB API
