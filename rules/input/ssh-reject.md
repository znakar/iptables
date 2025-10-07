## Reject SSH connection

**Command**:

```bash
iptables -A INPUT -p tcp --dport 22 -j REJECT

Explanation:

-A INPUT - adds a rule to the end of the chain
-p tcp - the rule applies to TCP packets
--dport - reject SSH connection
-j REJECT - reject the connection and notify the client of the error

