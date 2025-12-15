"Redis is a source-available, in-memory storage, used as a distributed, in-memory key–value database, cache and message broker, with optional durability"

https://redis.io/docs/latest/develop/connect/cli/

- Use the ```redis-cli``` command to interact with redis
- The command `redis-cli -h redis15.localnet.org -p 6390 PING
- The `-a` flag will allow you to add a password
- Once connected to the redis server on, use the `INFO` command to obtain info about the server
- Use the `SELECT` command followed by the database name to select a specific database
- Use the `INFO keyspace` command to view the databases available and the number of keys in each
- The `KEYS *` returns all of the keys in a database
- To retrieve data from a database, first set the database name. In this case, it is "db0"
- The command
	- `SET db0:2 "flag"` allows you to set the database as db0 and the key value as 2. We know that the index of 2 is where the flag is, hence why we include "flag" at the end of the command
- The above command is useful, but use this instead:
	- First, get all keys with the `KEYS *` command, then simply get the key you want with `GET "keyname"` For example, I wanted the flag key, and I used `GET "flag"`
- 