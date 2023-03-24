This text can be displayed as a sequence diagram using:
https://www.websequencediagrams.com/

Browser->Server: GET Request https://studies.cs.helsinki.fi/exampleapp/spa 

Server-->Browser: HTML document spa, status 200 (ok) 

Browser->Server: GET Request https://studies.cs.helsinki.fi/exampleapp/main.css 

Server-->Browser: main.css, status 200 (ok) 

Browser->Server: GET Request https://studies.cs.helsinki.fi/exampleapp/spa.js 

Server-->Browser: spa.js, status 200 (ok)

note over Browser: Browser executes JavaScript, which will request the data with a GET request.

Browser->Server: GET Request to Request URL: https://studies.cs.helsinki.fi/exampleapp/data.json 

Server-->Browser: data.json, status 200 (ok)

note over Browser: Browser start executing the event handler that populates the data into the ul and li's