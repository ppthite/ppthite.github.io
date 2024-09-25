# DDoS Attack Sequence Diagram

```mermaid
sequenceDiagram
    participant Attacker
    participant BotNet
    participant WebServer
    participant Firewall
    
    Attacker->>BotNet: Command to launch attack
    BotNet->>WebServer: Flood traffic to overload server
    WebServer->>Firewall: Request analysis of traffic
    Firewall->>WebServer: Traffic analysis and alert
    Firewall->>BotNet: Block IPs from bots
    BotNet->>Attacker: Report blocked bots
