# Sample Network Security Configuration

This section contains example configurations for securing the clinic's network.

## Firewall Rules Example:
The following is a sample firewall rule to restrict external access to internal clinic systems:

```bash
# Block all incoming traffic except for necessary ports (e.g., HTTP, HTTPS, VPN)
iptables -A INPUT -p tcp --dport 80 -j ACCEPT  # Allow HTTP
iptables -A INPUT -p tcp --dport 443 -j ACCEPT # Allow HTTPS
iptables -A INPUT -p tcp --dport 1194 -j ACCEPT # Allow VPN
iptables -A INPUT -j DROP  # Block everything else
