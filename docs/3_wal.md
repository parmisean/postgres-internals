# Write-Ahead Logging (WAL)

[Write-Ahead Logging (WAL)](https://www.postgresql.org/docs/current/wal-internals.html) is a key feature of Postgres that ensures durability and data integrity by writing changes to the database to a log before applying them to the actual data files. This mechanism provides several benefits, including crash recovery, replication, and efficient use of disk I/O.

![WAL Lifecycle Example](../image/wal_lifecycle.png)

## WAL Files and Log Sequence Numbers (LSN)

The WAL records are stored in a series of segments, called WAL files. These records contain the details necessary to describe the changes made to the database. Each WAL file is a fixed size, typically 16MB, and is written sequentially to disk. When a WAL file is full, Postgres switches to a new WAL file and continues writing new records.

Each WAL record is identified by a Log Sequence Number (LSN). The LSN is stored in the page header of each data page, and is used to track the progress of replication or crash recovery, as well as ensuring that changes are applied in the correct order.

WAL files are stored until they are no longer needed for crash recovery or replication. Once a WAL file is no longer needed, background processes like `autovacuum` will reclaim the space used by the tuples that were marked as dead or unused in the WAL file.

TODO:

- Explain how WAL is used in replication
- Explain checkpointer process

[Heap Storage](2_heap_storage.md) | [Introduction](../README.md) | [Query Parser](4_query_parser.md)
