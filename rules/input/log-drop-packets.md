## Log dropped packets


**Commands**:

```bash
iptables -A INPUT -j LOG --log-prefix "Dropped: "
```
Explanation: \
-A INPUT - adds a rule to the end of the chain \
-j LOG - write down the package information \
--log-prefix "Dropped: " -  adds the prefix “Dropped” to each log entry \


### To check the logs, use the command:
dmesg | grep "Dropped"
