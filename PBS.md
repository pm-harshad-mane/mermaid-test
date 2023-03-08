flowchart LR
    A[Hard edge] -->|Link text| B(Round edge)
    B --> C{Decision}
    C -->|One| D[Result one]
    C -->|Two| E[Result two]

## Prebid Server Flow
flowchart LR
    A[Entry Point] --> B[Raw Auction Request]
    B --> C[Processed Auction Request]
    C --> D[Bidder Request]
    D --> E[Raw Bidder Response]
    E --> F[All Processed Bid Responses]
    F --> G[Processed Auction Response]