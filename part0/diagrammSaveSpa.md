 ```mermaid
sequenceDiagram
    participant browser
    participant server

    Note right of browser: The user inputs a new note into the textfield and enters save. Afterwards it will add the new note to the list.

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: Redirect to /exampleapp/notes
    deactivate server

    Note right of browser: The browser executes the callback function that renders the notes
```
