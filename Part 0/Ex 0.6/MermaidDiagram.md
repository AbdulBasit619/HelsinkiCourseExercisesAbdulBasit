# 0.5: New Spa note diagram

```mermaid
sequenceDiagram
    participant browser
    participant server

    Note right of browser: The user fills the input field and clicks the save button

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    Note left of server: The browser executes the callback function that renders the note provided by user with Status Code: 201 Created
    server-->>browser: {"message":"note created"}
    deactivate server

    Note right of browser: The user can see his note being created successfully
```