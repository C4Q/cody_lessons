# SQLite with Express

### Objectives
- [SQLite](https://www.sqlite.org/mostdeployed.html)
- [node-sqlite3](https://github.com/mapbox/node-sqlite3)

### What is SQLite?
SQLite is the most widely used database engine in
the world. It is an _embedded_, and requires
[zero-configuration](https://www.sqlite.org/zeroconf.html).
Every SQLite database is saved as a single file.

### Install on MacOS
If you're using a Mac, Sqlite is installed by
default. Hooray!

Type `sqlite3` on the command line to see it.

### Install SQLite on Chromebook-Linux
`sudo apt-get install sqlite3`

Type `sqlite3` on the command line.

### Example: Candy Database 1
Using sqlite3 and the file `candy1.db`, build a single
table database with the following columns:
- id
- name
- has_chocolate
- rating

Use CREATE TABLE, INSERT INTO, and SELECT from the
SQLite3 shell tool.

### Example: Candy Database 2
Using sqlite3 and the file `candy2.db`, build a
single table database with the same columns as the
previous.

Run the CREATE TABLE and INSERT INTO statements
from a file.

### What is node-sqlite3?
[node-sqlite3](https://www.npmjs.com/package/sqlite3)
is a module providing SQLite3 bindings you may use
in your NodeJS projects.

All languages use libraries or modules to
interface with databases.

### Installing node-sqlite3
```sh
npm init
npm install sqlite3
```

### Sample Code
```js
let sqlite3 = require('sqlite3').verbose();
let db = new sqlite3.Database(':memory:');

db.run(`
  CREATE TABLE candies(
  id INTEGER PRIMARY KEY ASC,
  name TEXT,
  has_chocolate BOOLEAN,
  rating INT
  )
  `);
db.close();
```

### db.run
Use the `.run()` method of the db object to
execute a database operation that is _not_ a
SELECT.

Use a single argument -- the SQL statement you
would like to execute.

### Example: JSCandy DB 1
Using `node-sqlite3`, the file `create.js`, and
the file `candy3.db`,

### db.get
Use the `.`

### Example: JSCandy DB 2

### Extra: .all, .each, .serialize, .parallelize
