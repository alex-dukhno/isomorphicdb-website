---
title: Getting Started
permalink: /docs/getting-started/
redirect_from: /docs/getting-started.html
---

Currently, `isomorphicdb` is not distributed in a binary format. Experimentally, we
support a docker image. So you have to have Docker installed on your machine.

## Pulling Docker Image

You can pool the image with the following command:

```shell
docker pull ghcr.io/alex-dukhno/isomorphicdb:latest
```

To start up application you need to invoke the following command:

```shell
docker run -it -d -p 5432:5432 ghcr.io/alex-dukhno/isomorphicdb
```

---
**NOTE**
If you crashed the database docker instance we highly appreciated if you rerun
scenario with the following command and post a bug with backtrace:

```shell
docker run -it -d -e RUST_BACKTRACE=1 -p 5432:5432 ghcr.io/alex-dukhno/isomorphicdb
```
Thanks!

---

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

Now you can run `SQL` queries.
Please refere to [Supported Queries](/docs/supported-queries/)
