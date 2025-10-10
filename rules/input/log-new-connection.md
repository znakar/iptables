## Logging new connection


**Commands**:

```bash
iptables -I INPUT 1 -m state --state NEW -j LOG --log-prefix "NEW: "
```
Explanation: \
-I INPUT 1 - adds a rule to the beginning of the chain \
-m connects an additional module state \
--state NEW - the state module parameter, which indicates packets that initiate new connections \
-j LOG - log packet information


