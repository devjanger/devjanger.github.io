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

## Windows Powershell Check file integrity(SHA, MD5)

~~~ powershell
Get-FileHash .\document.pdf
~~~

[https://learn.microsoft.com/ko-kr/powershell/module/microsoft.powershell.utility/get-filehash?view=powershell-7.3
](https://learn.microsoft.com/ko-kr/powershell/module/microsoft.powershell.utility/get-filehash?view=powershell-7.3
)



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
