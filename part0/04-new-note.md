This text can be displayed as a sequence diagram using:
https://www.websequencediagrams.com/

Browser->Server: GET Request https://studies.cs.helsinki.fi/exampleapp/notes 

Server-->Browser: HTML document, status 200 (ok) 

Browser->Server: GET Request https://studies.cs.helsinki.fi/exampleapp/main.css 

Server-->Browser: main.css, status 200 (ok) 

Browser->Server: GET Request https://studies.cs.helsinki.fi/exampleapp/main.js 

Server-->Browser: main.js, status 200 (ok)

note over Browser: Browser executes javascript, which will request the data with a GET request.

Browser->Server: GET Request https://studies.cs.helsinki.fi/exampleapp/data.json 

Server-->Browser: data.json, status 200 (ok)

note over Browser: Browser starts executing the event handler that populates the data into the ul and li's

note over Browser: User enters message in text field

note over Browser: User clicks Save button

Browser->Server: POST Request https://studies.cs.helsinki.fi/exampleapp/new_note

note over Server: Server adds the post to an array of post-objects

Server-->Browser: Response 302 (Re-direct, new GET Request) 

Browser->Server: GET Request https://studies.cs.helsinki.fi/exampleapp/notes 

Server-->Browser: HTML document, Status 304 (not modified)

note over Browser: Browser reloads when receiving new HTML file

Browser->Server: GET Request https://studies.cs.helsinki.fi/exampleapp/main.css 

Server-->Browser: main.css, status 200 (ok) 

Browser->Server: GET Request https://studies.cs.helsinki.fi/exampleapp/main.js 

Server-->Browser: main.js, status 304 (not modified)

note over Browser: Browser executes javascript, which will request the data with a GET request.

Browser->Server: GET Request https://studies.cs.helsinki.fi/exampleapp/data.json 

Server-->Browser: data.json including the new post, status 200 (ok)