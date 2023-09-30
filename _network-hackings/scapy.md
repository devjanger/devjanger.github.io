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
SOURCE_PORT = 2222
DESTINATION_IP = "172.30.1.10"
DESTINATION_PORT = 1111

send(IP(src=SOURCE_IP, dst=DESTINATION_IP)/UDP(sport=SOURCE_PORT, dport=DESTINATION_PORT)/Raw(load="abc"))
~~~

Result(server side):
~~~ text
Received from ('123.123.123.123', 2222)
Received: b'abc'
~~~

## Sniffing FTP

~~~ python
from scapy.all import *

packet_filter = "tcp and port 21"

def sniff_ftp(packet):
    if packet.haslayer(TCP) and packet.haslayer(Raw):
        if packet[TCP].dport == 21:
            print(packet[Raw].load.decode())

sniff(filter=packet_filter, prn=sniff_ftp)
~~~
