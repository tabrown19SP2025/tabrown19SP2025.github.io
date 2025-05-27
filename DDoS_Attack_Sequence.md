sequenceDiagram
    participant Attacker
    participant BotNet
    participant Firewall
    participant WebServer

    Attacker->>BotNet: Command bots to begin DDoS
    BotNet->>WebServer: Flood with HTTP requests
    WebServer->>Firewall: Request overload alert
    Firewall->>WebServer: Analyze traffic patterns
    Firewall->>BotNet: Identify IPs and block traffic
    BotNet->>WebServer: Continue request flood
    Firewall-->>Attacker: Traceback attempt (optional)
    Firewall->>WebServer: Filtered traffic allowed
    WebServer-->>Legit Users: Partial or full service restored
