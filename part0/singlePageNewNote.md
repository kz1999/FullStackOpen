sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa {"content": "Some text", date: "2026-01-01..."}
    activate server
    server-->>browser: 201 Created {"message": "note created"}
    deactivate server