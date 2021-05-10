---
layout: post
title:  "Road a head a.k.a. Roadmap"
author: Alex Dukhno
---

Building anything is hard. Implementing your ideas is hard. You can start with its evaluation or as a side project to see if you like to work on it.

I started [IsomorphicDB][11] about a year ago. Git says the first commit was on 20 April 2020. During the year I had realized a couple of times that I would love to work on it full time. On the other hand I don't want to write yet another database that is very similar to those that people use now and jump straight head into "actions". You can be quickly buried in ever growing TODO list influenced by existing databases or SQL engines.

Working in software industry for a long time left some marks in your brain what is a "status quo". You are building up experience and get used to existing technologies and expectations of others about them. The more senior you are the more times you are involved into process of decision-making on usage of particular technology. If you are lucky you will know what is real business expectations and requirements - essentially you realize why certain technology was chosen and not just heard architects' words: "we choose X for Y among M, N and X".

Reading paper about ongoing research helps to expand my view on "what could be possibly done in the future". In the database field it seems popular "self-driven" database. It is like a self-driven car, however a database. Such a database has ability to adapt by itself to changing load over time.
Most of the papers that I encounter with talk about improving or sustain performance during increasing load. Simple example is that database creates a temporal index (or indexes) for tables columns that regularly accessed to speed-up read queries. At the same time the database should take into account that additional index requires additional memory and makes writes slower.

Researchers often refer to the fact that there are lots of databases and all of them have lots of configuration options. To be more precise - hundreds of them. For example, [some of motivations][4] behind [Sled][1] (embedded database written in [Rust][2]) is that [RocksDB][3] (another key-value storage that often used as embedded data store) gives users tons of flexibility and at Facebook, where RocksDB is developed, teams use machine learning to discover optimal configuration for particular use case.

Having conversation on self-driven databases with [Alex Petrov][5] helps me recognize that there is not much in self-driven databases research about routine daily DBAs or SREs tasks, like back up of a database. This conversation led me to what I would love to work on. If you have ideas or experienced something that you think could be improved by implementing adaptation mechanisms in databases I would like to hear from you. You can DM me on [twitter][6] or [email][7] me, create an [issue][8] or a [discussion][9] in the project repository, or join [discord server][10] and chat there.

Thanks for the reading and contributing your ideas.

[1]: https://sled.rs
[2]: http://rust-lang.org/
[3]: https://rocksdb.org
[4]: https://sled.rs/motivating_experiences.html
[5]: https://twitter.com/ifesdjeen?s=21
[6]: https://twitter.com/alex_dukhno?s=21
[7]: mailto:alex.dukhno@icloud.com
[8]: https://github.com/alex-dukhno/isomorphicdb/issues/new
[9]: https://github.com/alex-dukhno/isomorphicdb/discussions/new
[10]: https://discord.gg/PUcTcfU
[11]: https://github.com/alex-dukhno/isomorphicdb
