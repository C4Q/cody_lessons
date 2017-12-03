# Exercises

### PUG Mad Lib -- Query String
Using the file `mad-lib-qs.js`, PUG, and ExpressJS,
write an application with the following route:
- /

`/` will display a "mad lib" of your choosing.
`noun`, `verb`, and `adj` will be taken from the query
string and used in the mad lib.

EXAMPLE: If my mad lib is `One time there was this
#{adj} #{noun} who liked to #{verb}`, then a user visiting
`localhost:3000/?name=ben&verb=jump&adj=green` would see,
"One time there was this green ben who liked to jump."

HINT: Use `req.query` to access query string parameters.

### PUG Mad Lib -- Form
Using the file `mad-lib-form.js`, PUG, and
ExpressJS, write an application with the following
routes:
- /
- /mad-lib-post

`/` will return an HTML form with attributes `method="POST"`
and `action="/mad-lib-post`. The form will have
three text input fields -- `noun`, `verb`, and
`adj` -- as well as a submit button.

`/mad-lib-post` will listen for a POST request and
will return a rendered mad lib using the body data from
the request.

HINT: Use the `body-parser` middleware and `req.body`
to access the form data. Use `app.post` instead of
`app.get` to listen for the request.
