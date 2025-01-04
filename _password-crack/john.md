---
title: john the ripper password cracker
author: janger
date: 2024-12-30
category: password crack
layout: post
---

## cracking htpasswd using mask

~~~ bash
john htpasswd -1=[0-9a-z] --mask='G4HeulB?1' --max-length=11
~~~

[https://github.com/openwall/john/blob/bleeding-jumbo/doc/MASK](https://github.com/openwall/john/blob/bleeding-jumbo/doc/MASK)


## cracking /etc/shadow

~~~ bash
john --wordlist=/usr/share/wordlists/rockyou.txt unshadowed.txt
~~~

[https://erev0s.com/blog/cracking-etcshadow-john/](https://erev0s.com/blog/cracking-etcshadow-john/)
