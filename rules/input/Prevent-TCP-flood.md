## Prevent TCP flood

```bash
iptables -A INPUT -p tcp --syn -m limit --limit 10/s --limit-burst 20 -j ACCEPT
```

-A INPUT - adds a rule to the end of the chain \
-p - uses tcp protocol \
--syn - shorted version of --tcp-flags SYN,ACK,FIN,RST SYN 


m - indication of the use of an additional module \
limit - The module is used to limit the frequency of matching \
10/s - package processing speed per second  \
limit-burst - the number of packets that can be passed instantly before the limit specified by --limit takes effect \
-j ACCEPT - allows the packet to pass through the system 
