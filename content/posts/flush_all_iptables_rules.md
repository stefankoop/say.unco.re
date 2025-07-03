---
title: "Flush All Iptables Rules"
date: 2016-07-29T12:23:19+02:00
draft: false
toc: false
images:
tags:
  - linux
  - security
  - iptables
---

```bash
# set all chains to ACCEPT
iptables -P INPUT ACCEPT
iptables -P FORWARD ACCEPT
iptables -P OUTPUT ACCEPT

# flush all rules
iptables -F

# Delete all chains
iptables -X

# reset counters
iptables -Z

# flush and delete all NAT and MANGLE chains/tables
iptables -t nat -F
iptables -t nat -X
iptables -t mangle -F
iptables -t mangle -X
iptables -t raw -F
iptables -t raw -X
```
