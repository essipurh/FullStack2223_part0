# FullStack22_23

### 0.1 - 0.3
ei palauteta GitHubiin

### 0.4: new note diagram
sequenceDiagram
Browser->>Server: HTTP POST https://studies.cs.helsinki.fi/exampleapp/new_note
Note left of Browser: Sending HTTP POST request to the address new_note, the data is sent as the body of the request
Server->>Browser: 302 Found
Note right of Server: Server responds with HTTP status code 302, URL redirect, asking the browser to make a new HTTP Get request to the location set in the header (/exampleapp/notes)
Browser->>Server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/notes
Server->>Browser: HTTP Status Code 200, HTML code
Browser->>Server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.css
Server->>Broswer: HTTP Satus Code 200, CSS-file main.css
Browser->>Server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.js
Server->>Broswer: HTTP Satus Code 200, JS-file main.js
Note left of Browser: execution of the javascript code. Hence the following json data request:
Browser->>Server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/data.json
Server->>Broswer: HTTP Satus Code 200, JS-file main.js [{Content: ... }]
Note left of Browser: Browser renders the notes including new added note to the screen

### 0.5: Single Page App
sekvenssikaavio SPA sivun avaamiselle
[spa05](../osa0/spa05.png)

### 0.6: Uusi muistiinpano
sekvenssikaavio uuden muistiinpanon lisäykselle (SPA-versio)
[new_note_spa06](../osa0/new_note_spa06.png)
