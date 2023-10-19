---
title: Tunneling
author: janger
date: 2023-10-19
category: Network Hacking
layout: post
---

## SSH Tunneling - Local Tunneling(Local Port Forwarding) 

~~~ bash
ssh -L 8080:127.0.0.1:80 server_username@server_ip
~~~

## SSH Tunneling - Remote Tunneling(Remote Port Forwarding)

~~~ bash
ssh -R 8080:127.0.0.1:80 server_username@server_ip
~~~
