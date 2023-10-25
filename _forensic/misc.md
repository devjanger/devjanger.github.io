---
title: misc
author: janger
date: 2023-09-25
category: forensic
layout: post
---

## Windows command prompt Files merging

~~~ console
copy /b a.txt+b.txt+c.txt output.txt
~~~

<br>

## Windows Powershell Check file checksum(SHA, MD5)

~~~ powershell
Get-FileHash .\document.pdf
~~~

[https://learn.microsoft.com/ko-kr/powershell/module/microsoft.powershell.utility/get-filehash?view=powershell-7.3
](https://learn.microsoft.com/ko-kr/powershell/module/microsoft.powershell.utility/get-filehash?view=powershell-7.3
)

~~~ powershell
CertUtil -hashfile .\document.pdf MD5
~~~

[https://superuser.com/questions/245775/is-there-a-built-in-checksum-utility-on-windows-7](https://superuser.com/questions/245775/is-there-a-built-in-checksum-utility-on-windows-7)

<br>

## Linux Check file checksum(SHA, MD5)

~~~ bash
cat ./file.apk | openssl sha256
~~~

<br>

## Windows anti-forensic NTFS File System Volume cipher

~~~ console
cipher /w:c:
~~~

[https://learn.microsoft.com/ko-kr/windows-server/administration/windows-commands/cipher](https://learn.microsoft.com/ko-kr/windows-server/administration/windows-commands/cipher)


<br>


## Linux Exiftool

~~~ bash
exiftool IMG.png
~~~

<br>

## Python calculate CRC32

~~~ python
from zlib import crc32
f = open('a.txt', mode='rb')
crc = crc32(f.read())
print(hex(crc))
~~~

<br>
