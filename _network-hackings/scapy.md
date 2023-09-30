---
title: Scapy
author: janger
date: 2023-09-30
category: Network Hacking
layout: post
---

## UDP IP spoofing

~~~ python
from scapy.all import *

SOURCE_IP = "123.123.123.123"
DESTINATION_IP = "172.30.1.10"
DESTINATION_PORT = 1111

send(IP(src=SOURCE_IP, dst=DESTINATION_IP)/UDP(dport=DESTINATION_PORT)/Raw(load="abc"))
~~~
