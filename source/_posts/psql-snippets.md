---
title: PostgreSQL Snippets
date: 2021-05-24 03:52:13
categories:
  - comp.lang
tags:
  - sql
toc: true
---

[17 Practical psql Commands That You Don't Want To Miss](https://www.postgresqltutorial.com/psql-commands/)
[10 Command-line Utilities in PostgreSQL (article) - DataCamp](https://www.datacamp.com/community/tutorials/10-command-line-utilities-postgresql)

[How to switch database using Postgres](https://flaviocopes.com/postgres-how-to-switch-database/)
[How to list all databases using Postgres](https://flaviocopes.com/postgres-how-to-list-all-databases/)

# `psql`

[PostgreSQL: Documentation: psql](https://www.postgresql.org/docs/current/app-psql.html)
[Psql](http://postgresguide.com/utilities/psql.html)

```sh
export PGPASSWORD=<password>
psql -h localhost -U username -d DBNAME

psql "dbname=dbhere host=hosthere user=userhere password=pwhere port=5432 sslmode=require"
```

```sh
# run script
# https://kb.objectrocket.com/postgresql/how-to-run-an-sql-file-in-postgres-846
psql -h localhost -U username -d DBNAME -a -f script.sql

DBNAME-#> \i script.sql
```

## Docker

```sh
docker ps --filter name=postgres
docker exec -it $(docker ps --filter name=postgres -q) \
  psql -Upsql -ppassw0rd -d DBNAME

docker exec -it CONTAINER_ID \
  psql -Upsql -ppassw0rd --database DBNAME
```

# PostgreSQL tasks

> TODO: replace with PSQL statements

## User

[SQL CREATE USERS - w3resource](https://www.w3resource.com/sql/database-security/create-users.php)
[MySQL :: MySQL 5.7 Reference Manual :: 6.2.9 When Privilege Changes Take Effect](https://dev.mysql.com/doc/refman/5.7/en/privilege-changes.html)

```sql
GRANT CONNECT TO username IDENTIFIED BY password;
-- or
CREATE USER 'username' IDENTIFIED BY password;

GRANT privilege[,privilege] ON tablename TO USER username;
GRANT SELECT,INSERT,UPDATE,DELETE,CREATE,DROP,INDEX,ALTER,CREATE TEMPORARY TABLES ON tablename TO USER username;
FLUSH PRIVILEGES;
```

## Query

```sql
SHOW TABLES;
DESC tablename;
SHOW INDEX FROM Slide;
EXPLAIN SELECT * FROM Slide;

-- sample query
SELECT COUNT(*) FROM Slide;
SELECT COUNT(*) FROM Annotation;
```

## Alter table

```sql
ALTER TABLE DPMS.Snapshot
  CHANGE format format ENUM('bmp', 'jpeg', 'png', 'tiff') DEFAULT 'jpeg';

ALTER TABLE DPMS.Slide
  CHANGE vendor vendor ENUM('aperio', 'hamamatsu', 'leica', 'ventana', 'kfbio', '3dhistech', 'dmetrix', 'motic', 'unictech') NOT NULL;
```

## Delete records

```sql
DELETE FROM Slide
  WHERE Id < 5;
```

```sql
# create VIEW as shortcut
CREATE VIEW SlidesToDelete AS
    (SELECT * FROM Slide
      WHERE
        caseId = "cervical_batch" AND (
        slideId = "cervical_batch_002" OR
        slideId = "cervical_batch_004" OR
        slideId = "cervical_batch_005" OR
        slideId = "cervical_batch_006" OR
        slideId = "cervical_batch_007" OR
        slideId = "cervical_batch_008" OR
        slideId = "cervical_batch_009" OR
        slideId = "cervical_batch_010" OR
        slideId = "cervical_batch_011" OR
        slideId = "cervical_batch_013" OR
        slideId = "cervical_batch_014" OR
        slideId = "cervical_batch_020" OR
        slideId = "cervical_batch_022" OR
        slideId = "cervical_batch_024" OR
        slideId = "cervical_batch_025")
SELECT COUNT(slideId) FROM SlidesToDelete;

# Annotation references Slide
DELETE FROM Annotation WHERE slideId IN
    (SELECT slideId FROM SlidesToDelete);

# delete the slides
DROP VIEW SlidesToDelete;
# same condition as SlidesToDelete view
DELETE FROM Slide
  WHERE
    caseId = "cervical_batch" AND (
    slideId = "cervical_batch_002" OR
    slideId = "cervical_batch_004" OR
    slideId = "cervical_batch_005" OR
    slideId = "cervical_batch_006" OR
    slideId = "cervical_batch_007" OR
    slideId = "cervical_batch_008" OR
    slideId = "cervical_batch_009" OR
    slideId = "cervical_batch_010" OR
    slideId = "cervical_batch_011" OR
    slideId = "cervical_batch_013" OR
    slideId = "cervical_batch_014" OR
    slideId = "cervical_batch_020" OR
    slideId = "cervical_batch_022" OR
    slideId = "cervical_batch_024" OR
    slideId = "cervical_batch_025");
```

## #perfmatters

[PostgreSQL performance in 5 minutes - YouTube](https://www.youtube.com/watch?v=5M2FFbVeLSs) queries that shows slow queries and bottlenecks

[Database Indexing Explained (with PostgreSQL) - YouTube](https://www.youtube.com/watch?v=-qNSXK7s7_w)

```sql
EXPLAIN ANALYZE <STATEMENT>
# PG 13+
EXPLAIN (analyze true, wal true) <STATEMENT>
```
