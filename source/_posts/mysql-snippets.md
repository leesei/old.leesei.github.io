---
title: SQL Snippets
date: 2021-05-24 03:52:13
categories:
  - comp.lang
tags:
  - sql
toc: true
---

[How to Show a List of All Databases in MySQL | Linuxize](https://linuxize.com/post/how-to-show-databases-in-mysql/)
[List (Show) Tables in a MySQL Database | Linuxize](https://linuxize.com/post/show-tables-in-mysql-database/)

# `mysql`

```sh
mysql -h DATABASE_HOST -uuser -ppassw0rd --database DBNAME
```

```sh
# run script
# https://dev.mysql.com/doc/refman/8.0/en/mysql-batch-commands.html
mysql -h DATABASE_HOST -uuser -ppassw0rd --database DBNAME < script.sql

mysql> source script.sql
mysql> \. script.sql
```

## mysqldump

[MySQL :: MySQL 8.0 Reference Manual :: 4.5.4 mysqldump — A Database Backup Program](https://dev.mysql.com/doc/refman/8.0/en/mysqldump.html)

[mysqldump - dump all mysql tables into separate files automagically? - Stack Overflow](https://stackoverflow.com/questions/3669121/dump-all-mysql-tables-into-separate-files-automagically)

```sh
mysqldump -h DATABASE_HOST -uuser -ppassw0rd DBNAME [TABLENAME] > sqlbackup.sql

# per table dump to folder
# this only works on the SQL server
sudo chown -R mysql:mysql ~/sqldump
mysqldump --user=dbuser --password --tab=~/sqldump dbname
# dump schema only
mysqldump --user=dbuser --password --no-data --tab=~/output/dir dbname
```

## Docker

```sh
docker ps --filter name=mariadb
docker exec -it $(docker ps --filter name=mariadb -q) \
  mysql -uroot -ppassw0rd --database DBNAME

docker exec -it CONTAINER_ID \
  mysql -uroot -ppassw0rd --database DBNAME
```

# SQL tasks

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
