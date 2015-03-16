sqlstream: stream MySQL replication events to Apache Kafka.
===========================================================

Sqlstream connects to a MySQL instance as a replicant and
produces the replication events read onto an Apache Kafka
topic. The events are produced as a JSON-serialized map, keyed
by the server-id which produced the event.

## Configuration

Sqlstream accepts a single argument, its configuration file
which has the following format:

```
mysql.host=localhost
mysql.port=3306
mysql.user=replicant
mysql.password=replicant
topic=sqlstream
bootstrap.servers=localhost:9092
```

## Caveats

- No support for keeping track of offsets
- No configurable key or serialization

## License

Copyright 2015 Pierre-Yves Ritschard <pyr@spootnik.org>

Permission to use, copy, modify, and distribute this software for any
purpose with or without fee is hereby granted, provided that the above
notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES
WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR
ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN
ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF
OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.