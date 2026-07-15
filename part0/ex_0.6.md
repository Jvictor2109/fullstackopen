``` mermaid
sequenceDiagram
    participant browser
    participant server

    Note right of browser: User writes a new note and submits
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa <br> (with the note on the body)
    activate server
    server-->>browser: 201 Created
    deactivate server
Note right of browser: The Javascript file updates the note list without reloading the page
```
