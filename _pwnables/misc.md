---
title: misc
author: janger
date: 2023-09-25
category: pwnables
layout: post
---


> **Check file information**

```bash
file ./chall
```

output
```text
./chall: ELF 64-bit LSB executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=662f66798546b59e005b4
```


<br>

> **Check file memory mitigation**

```bash
checksec --file=./chall
```

output
```text
[*] '/home/attacker/ground/chall'
    Arch:     amd64-64-little
    RELRO:    Partial RELRO
    Stack:    No canary found
    NX:       NX enabled
    PIE:      No PIE (0x400000)
```

<br>

> **Useful utility Tools**

Hex to String Converter - https://codebeautify.org/hex-string-converter

String to Hex Converter - https://codebeautify.org/string-hex-converter


