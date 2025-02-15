---
Title: Supported connection clients
description: Info about Redis client libraries and supported clients when using the discovery service.
weight: 10
categories: ["RS"]
aliases: [/rs/administering/designing-production/supported-clients-browsers/,
         /rs/administering/designing-production/supported-clients-browsers.md,
         /rs/connections/supported-clients-browsers/,
         /rs/connections/supported-clients-browsers.md,
         /rs/databases/connections/supported-clients-browsers.md,
         /rs/databases/connections/supported-clients-browsers/,
         /rs/databases/connect/supported-clients-browsers,
         /rs/databases/connect/supported-clients-browsers.md,
         ]
---
You can connect to Redis Enterprise Software databases programmatically using client libraries.

## Redis client libraries

To connect an application to a Redis database hosted by Redis Enterprise Software, use a [client library](https://redis.io/clients) appropriate for your programming language.

You can also use the `redis-cli` utility to connect to a database from the command line.

For examples of each approach, see the [Redis Enterprise Software quickstart]({{<relref "/rs/installing-upgrading/quickstarts/redis-enterprise-software-quickstart">}}).

Note: You cannot use client libraries to configure Redis Enterprise Software.  Instead, use:

- The Redis Software [admin console]({{< relref "/rs/installing-upgrading/quickstarts/redis-enterprise-software-quickstart" >}})
- The [REST API]({{<relref "/rs/references/rest-api">}})
- Command-line utilities, such as [`rladmin`]({{<relref "/rs/references/cli-utilities/rladmin">}})

### Discovery service

We recommend the following clients when using a [discovery service]({{< relref "/rs/databases/durability-ha/discovery-service.md" >}}) based on the Redis Sentinel API:

- [redis-py](https://github.com/redis/redis-py) (Python Redis client)
- [Hiredis](https://github.com/redis/hiredis) (C Redis client)
- [Jedis](https://github.com/redis/jedis) (Java Redis client)
- [node-redis](https://github.com/redis/node-redis) (Node.js Redis client)

If you need to use another client, you can use [Sentinel Tunnel](https://github.com/RedisLabs/sentinel_tunnel)
to discover the current Redis master with Sentinel and create a TCP tunnel between a local port on the client and the master.

