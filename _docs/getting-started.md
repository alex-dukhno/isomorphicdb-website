---
title: Getting Started
---

Currently, `isomorphicdb` is not distributed in a binary format. Experimentally, we
support a docker image. So you have to have Docker installed on your machine.

You can pool the image with the following command:

```shell
docker pull ghcr.io/alex-dukhno/isomorphicdb:latest
```

To start up application you need to invoke the following command:

```shell
docker run -it -d -p 5432:5432 ghcr.io/alex-dukhno/isomorphicdb
```

If you crashed the database docker instance we highly appreciated if you rerun
scenario with the following command and post a bug with backtrace:

```shell
docker run -it -d -e RUST_BACKTRACE=1 -p 5432:5432 docker.pkg.github.com/alex-dukhno/isomorphicdb/isomorphicdb
```
Thanks!

To connect to database you have to have `psql` on your machine, it can be installed
with `PostgreSQL` from the [official website](https://www.postgresql.org) or with
package manager like `homebrew` or `apt-get`.

Then you can start client with the command:

```shell
psql -h 127.0.0.1 -W
```

After entering random password you should see `psql` prompt similar to:

```shell
psql (12.2, server 0.0.0)
Type "help" for help.

username=>
```

Now you can run `SQL` queries. This is a snipet supported queries:

```sql
create schema SMOKE_QUERIES;

create table SMOKE_QUERIES.VALIDATION_TABLE(column_test smallint);

insert into SMOKE_QUERIES.VALIDATION_TABLE
values (1);

select column_test
from SMOKE_QUERIES.VALIDATION_TABLE;

update SMOKE_QUERIES.VALIDATION_TABLE
set column_test = 2;

select column_test
from SMOKE_QUERIES.VALIDATION_TABLE;

delete
from SMOKE_QUERIES.VALIDATION_TABLE;

select column_test
from SMOKE_QUERIES.VALIDATION_TABLE;

drop table SMOKE_QUERIES.VALIDATION_TABLE;

create table SMOKE_QUERIES.MANY_COLUMNS_TABLE (column_1 smallint, column_2 smallint, column_3 smallint);

insert into SMOKE_QUERIES.MANY_COLUMNS_TABLE values (1, 2, 3);

select column_1, column_2, column_3 from SMOKE_QUERIES.MANY_COLUMNS_TABLE;

insert into SMOKE_QUERIES.MANY_COLUMNS_TABLE values (4, 5, 6), (7, 8, 9);

select column_1, column_2, column_3 from SMOKE_QUERIES.MANY_COLUMNS_TABLE;

select column_1, column_3 from SMOKE_QUERIES.MANY_COLUMNS_TABLE;

select column_1, column_2 from SMOKE_QUERIES.MANY_COLUMNS_TABLE;

select column_2, column_3 from SMOKE_QUERIES.MANY_COLUMNS_TABLE;

select * from SMOKE_QUERIES.MANY_COLUMNS_TABLE;

select column_3, column_1, column_2 from SMOKE_QUERIES.MANY_COLUMNS_TABLE;

select column_3, column_2, column_1 from SMOKE_QUERIES.MANY_COLUMNS_TABLE;

select column_3, column_2, column_3, column_1, column_2 from SMOKE_QUERIES.MANY_COLUMNS_TABLE;

update SMOKE_QUERIES.MANY_COLUMNS_TABLE set column_1 = 10, column_2 = -20, column_3 = 30;

select column_3, column_2, column_1 from SMOKE_QUERIES.MANY_COLUMNS_TABLE;

drop table SMOKE_QUERIES.MANY_COLUMNS_TABLE;

drop schema SMOKE_QUERIES;
```

Happy hacking!
