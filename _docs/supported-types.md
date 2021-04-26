---
title: Supported Types
permalink: /docs/supported-types/
redirect_from: /docs/supported-types.html
---

IsomorphicDB supports `numeric`, `character` and `boolean` types.

The following operators are supported for all types

| Binary Operators | Description |
|:----------------:|-------------|
| `a = b` | equality |
| `a <> b` | inequality |
| `a != b` | inequality |
| `a > b` | greater |
| `a >= b` | greater than |
| `a < b` | less |
| `a <= b` | less than |

## Numeric types

Among supported `numreic` types are `smallint`, `integer` and `bigint`.

The following operators are supported for numeric types

| Binary Operators | Description |
|:----------------:|-------------|
| `a + b` | addition |
| `a - b` | subtraction |
| `a * b` | multiplication |
| `a / b` | division |
| `a % b` | modulo |
| `a ^ b` | exponent |
| `a & b` | bitwise and |
| `a | b` | bitwise or |
| `a # b` | bitwise xor |
| `a << b` | bitwise shift left |
| `a >> b` | bitwise shift right |

| Unary Operators | Description |
|:---------------:|-------------|
| `+a` | unary plus (no operation) |
| `-a` | negation |
| `|/a` | square root |
| `||/a` | cube root |
| `a!` | factorial |
| `!! a` | factorial |
| `@a` | absolute value |
| `~a` | bitwise not |

## Character types

IsomorphicDB supports `char` and `varchar` types

The following operators are supported for character types

| Binary Operators | Description |
|:----------------:|-------------|
| `a LIKE b` | if `a` matches with `b` |
| `a NOT LIKE b` | if `a` does not matche with `b` |
| `a || b` | concatenation |

## Boolean types

The following operators are supported for boolean types

| Binary Operators | Description |
|:----------------:|-------------|
| `a AND b` | logical and |
| `a OR b` | logical or |

| Unary Operators | Description |
|:---------------:|-------------|
| `NOT a` | logical not |

Examples of creating table with different types

```sql
create table numbers (
    sm_int smallint,
    regular_int integer,
    bg_int bigint
);

create table strings (
    var_str varchar(255),
    const_str char(255)
);

create table only_bool (
    logic boolean
);
```
