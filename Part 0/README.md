0.4: nueva nota

browser -> server: HTTP POST https://studies.cs.helsinki.fi/exampleapp/new_note Payload: TEXT

server -> browser: HTTP-RESPONSE The server response is with the code 302 and reload the content of the page

note over browser:
browser reload the page

browser -> server: HTTP GET 200 https://studies.cs.helsinki.fi/exampleapp/notes The page reload and get the html content

server -> browser: notes.html

browser -> server: HTTP GET 200 https://studies.cs.helsinki.fi/exampleapp/main.css The browser interprets the html and proceeds to make a request to the server to obtain the css code

server -> browser: main.css

browser -> server: HTTP GET 200 https://studies.cs.helsinki.fi/exampleapp/main.js The browser interprets the html and proceeds to make a request to the server to obtain the javascript code

server -> browser: main.js

browser -> server: HTTP GET 200 https://studies.cs.helsinki.fi/exampleapp/data.json Get the data from the server, obtain a json.

server -> browser: data.json

note over browser:
browser executes the event handler
that renders notes to display

browser -> server HTTP GET 200 https://studies.cs.helsinki.fi/favicon.ico Obtain the favicon image

server -> browser: favicon.ico

0.5 Single Page App

browser -> server HTTP GET 200 https://studies.cs.helsinki.fi/exampleapp/spa Get the html from the page

server -> browser: spa. HTTP RESPONSE HTML 200 The server return the html for show to the user.

browser -> server HTTP GET 200 https://studies.cs.helsinki.fi/exampleapp/main.css The browser interprets the html and proceeds to make a request to the server to obtain the css code

server -> browser: main.css

browser -> server HTTP GET 200 https://studies.cs.helsinki.fi/exampleapp/spa.js The browser interprets the html and proceeds to make a request to the server to obtain the javascript code

server -> browser: spa.js

browser -> server HTTP GET 200 https://studies.cs.helsinki.fi/exampleapp/data.json

server -> browser: data.json

note over browser:
browser executes the event handler
that renders notes to display

browser -> server HTTP GET 200 https://studies.cs.helsinki.fi/favicon.ico

server -> browser: favicon.ico

0.6: Nueva nota

browser -> server HTTP POST 201 https://studies.cs.helsinki.fi/exampleapp/new_note_spa Send to the server the new note

server -> browser: The server response is a message in json {"message":"note created"}

note over browser:
browser executes the event handler
that renders notes to display
