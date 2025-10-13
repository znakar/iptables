## Prevent ICMP flood 

```bash
iptables -A FORWARD -p icmp -m limit --limit 5/s -j ACCEPT


-A FORWARD - adds a rule to the end of the chain
-p - uses icmp protocol
-m indication of the use of an additional module
--limit - The module is used to limit the frequency of matching. For example: to reduce the number of entries in logs.
5/s - package processing speed per second (maximum 5 packets per second)
