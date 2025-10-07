## Drop HTTPS traffic

**Command**:

```bash
iptables -A INPUT -p tcp --dport 443 -j DROP

Explanation:

-A INPUT - adds a rule to the end of the chain
-p tcp - the rule applies to TCP packets
--dport - filter packets sent to the HTTPS port
-j DROP - the client won't get an error message
