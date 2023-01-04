```mermaid
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail!
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!
```

```mermaid
sequenceDiagram
    participant UserBrowser
    participant PubMaticTranslator
    participant PubMaticAdServer
    UserBrowser->>PubMaticTranslator: POST-Request(Secure/Http2)
    PubMaticTranslator->>PubMaticAdServer: POST-Request(Non-Secure/Http2)
    loop RTB-Auction
        PubMaticAdServer->>PubMaticAdServer: Fetch bids from DSPs and conduct real-time auction
    end
    PubMaticAdServer->>PubMaticTranslator: Response(Non-Secure/Http2)
    PubMaticTranslator->>UserBrowser: Response(Secure/Http2)   
```

```mermaid
sequenceDiagram
    participant UserBrowser
    participant CloudflareTunnel
    participant PubMaticTranslator
    participant PubMaticAdServer
    UserBrowser->>CloudflareTunnel: POST-Request(Secure/Http3)
    CloudflareTunnel->>PubMaticTranslator: POST-Request(Non-Secure/Http2)
    PubMaticTranslator->>PubMaticAdServer: POST-Request(Non-Secure/Http2)
    loop RTB-Auction
        PubMaticAdServer->>PubMaticAdServer: Fetch bids from DSPs and conduct real-time auction
    end
    PubMaticAdServer->>PubMaticTranslator: Response(Non-Secure/Http2)
    PubMaticTranslator->>CloudflareTunnel: Response(Non-Secure/Http2)
    CloudflareTunnel->>UserBrowser: Response(Secure/Http3)   
```
