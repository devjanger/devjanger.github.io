---
title: hashcat password cracker
author: janger
date: 2024-12-30
category: password crack
layout: post
---

## MD5 cracking

~~~ bash
hashcat -m 0 "412dd4759978acfcc81deab01b382403" /usr/share/wordlists/rockyou.txt.gz --show
hashcat -m 0 hashfile.txt /usr/share/wordlists/rockyou.txt.gz --show
~~~

