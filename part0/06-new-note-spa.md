This text can be displayed as a sequence diagram using:
https://www.websequencediagrams.com/

Browser->Server: GET Request https://studies.cs.helsinki.fi/exampleapp/spa 

Server-->Browser: HTML document spa, status 200 (ok) 

Browser->Server: GET Request https://studies.cs.helsinki.fi/exampleapp/main.css 

Server-->Browser: main.css, status 200 (ok) 

Browser->Server: GET Request https://studies.cs.helsinki.fi/exampleapp/spa.js 

Server-->Browser: spa.js, status 200 (ok)

note over Browser: Browser executes JavaScript spa.js, which will request the data with a GET request.

Browser->Server: GET Request to Request URL: https://studies.cs.helsinki.fi/exampleapp/data.json 

Server-->Browser: data.json, status 200 (ok)

note over Browser: Browser start executing the event handler that populates the data into the ul and li's

note over Browser: User enters message in text field

note over Browser: User clicks Save button

note over Browser: Default behaviour is prevented, Brower doesn't refresh

note over Browser: Event handler adds the new note to the list.

note over Browser: Event handler rerenders the list with ul and li's, and sends the new note to the server.

Browser->Server: POST Request https://studies.cs.helsinki.fi/exampleapp/new_note_spa

Server-->Browser: status 201 (created)