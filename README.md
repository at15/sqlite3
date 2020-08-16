# sqlite3

A pure go package for reading sqlite3 database file.

## Motivation

I need to read sqlite3 database file on windows. There is an existing [sqlite3 cgo binding](http20github.com/mattn/go-sqlite3).
However a pure go version is more portable and easier to compile.

## Alternative

Export to csv using sqlite3 binary, e.g. write `a.txt` and shell out to `sqlite3`

```
.mode csv
.output data.csv
SELECT * FROM page_views LIMIT 100
```

```bash
sqlite3 foo.db < a.txt
```
