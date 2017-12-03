# Challenge

### Joke API 1
Build a database called `jokes.db` with SQLite3.
Create a table `jokes` with the following columns:
- id
- setup
- punchline

Use an INSERT statement to test your table.

### Joke API 2
Using the file `jokes.js`, ExpressJS, and
`jokes.db`, build an application with the
following routes:
- /
- /add
- /joke

`/` will return an HTML response with a form with
attributes `method="POST"` and `action="/add"`.
The form will have two text inputs, _setup_ and
_punchline_, and a submit button.

`/add` will accept a POST request from the form
and enter a new joke into the database, then
redirect back to `/`.

`/joke` will return an HTML response with a
random joke.
