graph LR
    User[User (Browser)] -->|1. Upload Photo| NodeJS[Node.js Backend]
    subgraph Server Resource
        NodeJS -->|2. Spawns Child Process| Python[Python Script (rembg)]
        Python -->|3. Heavy AI Calculation| RAM{High RAM Usage}
        Python -->|4. Save Result| Disk[(Local Disk Storage)]
    end
    NodeJS -->|5. Read File & Send| User

    style Python fill:#ffcccc,stroke:#cc0000,stroke-width:2px,color:black
    style RAM fill:#ffeb3b,stroke:#fbc02d,stroke-width:2px,color:black
