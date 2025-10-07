## Reject HTTPS traffic

**Command**:

```bash
iptables -A INPUT -p tcp --dport 443 -j REJECT
```
Explanation:

-A INPUT - adds a rule to the end of the chain
-p tcp - the rule applies to TCP packets
--dport - filter packets sent to the HTTPS port
-j REJECT - reject the connection and notify the client of the error
