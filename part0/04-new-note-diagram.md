    ## New note diagram.
    
    User->>Browser: Create a new note
    Browser->>Server: POST request to create a new note // Endpoint: new_note
    activate Server
    Server-->>Browser: Response (302) & Redirect to /notes
    deactivate Server

    User->>Browser: Visit /notes page
    Browser->>Server: GET request for CSS file // Endpoint: main.css
    activate Server
    Server-->>Browser: CSS file response
    deactivate Server

    Browser->>Server: GET request for JavaScript file // Endpoint: main.js
    activate Server
    Server-->>Browser: JavaScript file response
    deactivate Server

    Note over Browser: JavaScript executed, fetching JSON data

    Browser->>Server: GET request for notes JSON data // Endpoint: data.json
    activate Server
    Server-->>Browser: Notes JSON object response
    deactivate Server