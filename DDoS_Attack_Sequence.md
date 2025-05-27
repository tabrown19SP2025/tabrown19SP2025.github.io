```mermaid
sequenceDiagram
    participant Attacker
    participant BotNet
    participant Firewall
    participant WebServer

    Attacker->>BotNet: Sends attack command to bots
    BotNet->>WebServer: Begins sending large volumes of traffic
    WebServer->>Firewall: Detects overload and alerts firewall
    Firewall->>Firewall: Analyzes incoming traffic patterns
    Firewall-->>WebServer: Begins filtering suspicious traffic
    Firewall->>BotNet: Blocks known bot IP addresses
    BotNet->>WebServer: Continues DDoS with rotating IPs
    Firewall->>Firewall: Applies rate limiting and behavioral filtering
    Firewall-->>WebServer: Allows filtered legitimate traffic
    WebServer-->>Users: Attempts to restore access to valid users
