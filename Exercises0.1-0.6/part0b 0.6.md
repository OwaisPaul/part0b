```mermaid 
sequenceDiagram
    participant browser
    participant server
    Note right of browser: submission is handled by code defined in a JavaScript file that the browser loads.
   Note right of browser:  request contains a new note  JSON [{"content": "hey man","date": "2025-02-23T08:51:21.864Z"}]
    browser->>server:   POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: JSON{"message":"note created"}
       
    Note left of server: The server responds to the request with a status code of 201 created . 
    Note left of server: This time, the server does not request a redirect like in our previous exercise.
    Note left of server: The browser remains on the same page, and no further HTTP requests are made
   ```