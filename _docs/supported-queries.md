---
title: Supported Queries
permalink: /docs/supported-queries/
redirect_from: /docs/supported-queries.html
---

IsomorphicDB supports `INSERT`, `UPDATE`, `DELETE` and `SELECT` statements.

## Inserts

You can insert single row or multiple withing a single query.
For example:

```sql
insert into my_table values (1, 2, 3);

insert into my_table values (1, 2, 3), (4, 5, 6), (7, 8, 9);
```

## Updates, Deletes and Selects

Updates, Deletes and Selects support `WHERE` clasue so you can filter data that you want to update, delete or select.
Please, refere to [Supported Types](/docs/supported-types/) to see what operators you can use with what data types.

For example:

```sql
select foo from my_table where bar = 'baz';

delete from my_table where foo > 1;
```

The same is applicable for `SET` operators inside Update queries.

```sql
update my_table set foo = 1 + 2 * foo where bar > 'baz';
```
