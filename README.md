```mermaid
graph LR
    A([User / System]) -->|Uploads File| B[(Amazon S3)]
    B -->|Event Trigger| C[AWS Lambda]
    C -->|Saves Metadata| D[(Amazon DynamoDB)]
    C -->|Triggers Alert| E((Amazon SNS))
    E -->|Sends Email| F([Your Inbox])
    
    style B fill:#3F8624,stroke:#232F3E,stroke-width:2px,color:#fff
    style C fill:#F58536,stroke:#232F3E,stroke-width:2px,color:#fff
    style D fill:#3B48CC,stroke:#232F3E,stroke-width:2px,color:#fff
    style E fill:#FF9900,stroke:#232F3E,stroke-width:2px,color:#fff
