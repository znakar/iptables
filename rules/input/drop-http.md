## Drop HTTP


**Commands**:

```bash
iptables -A INPUT -p tcp --dport 80 -j DROP
```
Explanation: \
-A INPUT - adds a rule to the end of the chain \
-p tcp - the rule applies to TCP packets \
--dport - HTTP port \
-j DROP - drop incoming HTTP packets
