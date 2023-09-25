---
title: misc
author: janger
date: 2023-09-25
category: forensic
layout: post
---

**Windows command prompt Files merging**

```cmd
copy /b a.txt+b.txt+c.txt output.txt
```

<br>

**Windows Powershell Check file integrity(SHA, MD5)**

```powershell
Get-FileHash .\document.pdf
```

https://learn.microsoft.com/ko-kr/powershell/module/microsoft.powershell.utility/get-filehash?view=powershell-7.3



<br>

**Windows anti-forensic NTFS File System Volume cipher**

```cmd
cipher /w:c:
```

https://learn.microsoft.com/ko-kr/windows-server/administration/windows-commands/cipher


<br>