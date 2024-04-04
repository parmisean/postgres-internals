# Query Optimization

The [EXPLAIN](https://www.postgresql.org/docs/current/sql-explain.html) statement is a powerful tool for understanding how Postgres executes your queries, providing insights into the query plan chosen by the query optimizer.

## Cost Statistics

Postgres cost statistics are an arbitrary unit used to estimate the cost of executing a query plan. The costs are anchored to a single sequential page read for the table, and each row estimated or processed by the query increases the cost by .001. There will be additional costs for things like a non-sequential page read which will add 4.0.

The cost will be displayed near the top of the explain results, similar to the following example `(cost=0.00..15.00 rows=1000 width=0)`. The first number is the startup cost for the query, the second number is the total cost of the query. Using this example, we can see the query retrieved the data from 5 sequential pages and 1000 rows were processed.

## Buffer Statistics

Each buffer is typically 8KiB in size and is used to cache data pages in memory. The buffer statistics in the query plan show how many buffers were read and written during the query execution, and will indicate the amount of disk IO required to execute the query.

## Optimizing a Query

[Query Parser](4_query_parser.md) | [Introduction](../README.md) | [Appendix](6_appendix.md)
