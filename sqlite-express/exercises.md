# Exercises

### Rock Paper Scissors 1
Build a SQLite3 database called `rps.db`. Create a
table `rounds` with the following columns:
- id
- user_choice
- ai_choice
- result

The database will be used to track games of Rock,
Paper, Scissors. `id` is the primary key.
`user_choice` and `ai_choice` will be rock, paper,
or scissors. `result` will be win, lose, or tie,
according to if the user won the game.

Use an INSERT statement to test your table.

### Rock Paper Scissors 2
Using the file `rps-sql.js`, ExpressJS, and SQLite3
with your `rps.db` database, build an API with
the following endpoints:
- /
- /:choice

`/:choice` will process a game of Rock, Paper,
Scissors with the user's *:choice* of rock, paper,
or scissors against a randomly generated AI
choice. The result will be returned to the user as
a JSON object, and the "round" will be stored in
`rps.db`.

`/` will return a JSON object with the following
properties:
- total_wins
- total_losses
- total_ties
- total_user_rocks
- total_user_papers
- total_user_scissors
- total_ai_rocks
- total_ai_papers
- total_ai_scissors

Compute the values of each property from `rps.db`.

Old code may help you complete this exercise more
quickly.
