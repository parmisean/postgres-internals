# Appendix

## Documentation

- [Postgres Docs: Connection Established](https://www.postgresql.org/docs/curent/connect-estab.html)
- [Postgres Docs: Heap-Only Tuple (HOT)](https://www.postgresql.org/docs/current/storage-hot.html)
- [Postgres Docs: Write-Ahead Logging (WAL)](https://www.postgresql.org/docs/current/wal-internals.html)
- [Postgres Docs: Parser Stage](https://www.postgresql.org/docs/current/parser-stage.html)
- [Wiki: Yet Another Compiler-Compiler (YACC)](https://en.wikipedia.org/wiki/Yacc)

## Articles

- [Postgres Process Architecture by Hussein Nasser](https://medium.com/@hnasr/postgresql-process-architecture-f21e16459907)
- [How Does Vacuum Work in PostgreSQL by Richard Yen](https://www.enterprisedb.com/postgres-tutorials/how-does-vacuum-work-postgresql)
- [Structure of Heap Table in PostgreSQL by Azat Yakupov of Quadcode](https://medium.com/quadcode-life/structure-of-heap-table-in-postgresql-d44c94332052)

## Code Files

- [Heap Access Methods: heapam.c](https://github.com/postgres/postgres/blob/master/src/backend/access/heap/heapam.c)
- [Page Header: bufpage.h](https://github.com/postgres/postgres/blob/master/src/include/storage/bufpage.h)
- [Line Pointer Array Items: itemid.h](https://github.com/postgres/postgres/blob/master/src/include/storage/itemid.h)
- [Scanner: scan.l](https://github.com/postgres/postgres/blob/master/src/backend/parser/scan.l)
- [Grammar: gram.y](https://github.com/postgres/postgres/blob/master/src/backend/parser/gram.y)

[Query Optimization](5_query_optimization.md) | [Introduction](../README.md)
