sequenceDiagram
    participant User
    participant Browser
    participant Server

    User->>Browser: Open /exampleapp/spa
    Browser->>Server: GET /exampleapp/spa
    Server-->>Browser: HTML document

    Browser->>Server: GET /exampleapp/main.css
    Server-->>Browser: CSS file

    Browser->>Server: GET /exampleapp/spa.js
    Server-->>Browser: JavaScript file

    Browser->>Server: GET /exampleapp/data.json
    Server-->>Browser: JSON containing notes

    Browser->>Browser: Execute JavaScript
    Browser->>Browser: Render notes on the page
    Browser-->>User: Display Notes App