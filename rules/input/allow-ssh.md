## Allow SSH 


**Commands**:

```bash
iptables -A INPUT -p tcp --dport 22 -j ACCEPT
```
Explanation: \
-A INPUT - adds a rule to the end of the chain \
-p tcp - the rule applies to TCP packets \
--dport - default SSH port \
-j ACCEPT - allow incoming SSH connections


## Allowing SSH only from a specific IP address

```bash
iptables -A INPUT -p tcp -s 192.168.0.30 --dport 22 -j ACCEPT
```

Explanation:
-s — set a specific IP address

