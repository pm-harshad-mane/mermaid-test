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
    UserBrowser-->PubMaticTranslator: Request(Secure/Http2)
    PubMaticTranslator-->PubMaticAdServer: Request(Non-Secure/Http2)
    PubMaticAdServer-->PubMaticTranslator: Response(Non-Secure/Http2)
    PubMaticTranslator-->UserBrowser: Response(Secure/Http2)   
```
