    ## New note in single page application diagram

    User->>Browser: Interact with SPA
    Browser->>Browser: Input new note content
    Browser->>Browser: Click "Save" button

    Browser->>api: Send note data // Endpoint: /api/notes
    activate api
    api->>database: Store new note
    database-->>api: Confirmation
    deactivate api
    api-->>Browser: Response
    Browser->>Browser: Update UI with new note

    Note over Browser: User sees the newly added note
