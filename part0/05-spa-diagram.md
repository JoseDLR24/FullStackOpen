    ## Single page application diagram

    Browser->>Server: Request HTML // Endpoint: spa
    activate Server
    Server-->>Browser: Response & HTML content
    deactivate Server

    Note right of Browser: Browser processes HTML, triggers resource fetch

    Browser->>Server: Request CSS // Endpoint: main.css
    activate Server
    Server-->>Browser: Response & CSS content
    deactivate Server

    Browser->>Server: Request JavaScript // Endpoint: main.js
    activate Server
    Server-->>Browser: Response & JS content
    deactivate Server

    Note right of Browser: JavaScript function fetches JSON notes data

    Browser->>Server: Request Notes JSON // Endpoint: data.json
    activate Server
    Server-->>Browser: Notes JSON object
    deactivate Server
