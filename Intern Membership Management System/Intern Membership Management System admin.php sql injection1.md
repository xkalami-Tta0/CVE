#  Intern Membership Management System admin.php sql injection

## NAME OF AFFECTED PRODUCT(S)

Intern Membership Management System

## Vendor Homepage

https://code-projects.org/intern-membership-management-system-in-php-with-source-code/

## Vulnerable File

admin.php

## VERSION(S)

v1.0

## Vulnerability Type

SQL injection

## DESCRIPTION

There is a SQL injection vulnerability in the admin.php file of the Intern Membership Management System project, which can be exploited by attackers to obtain sensitive data information

## Vulnerability details and POC

![image-20260107001429374](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Intern-Membership-Management-System/image-20260107001429374.4g4z836egv.webp)

![image-20260107001458085](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Intern-Membership-Management-System/image-20260107001458085.41yjh7y3lq.webp)

Data packet：

```
GET /intern/admin/edit_admin.php?admin_id=17 HTTP/1.1
Host: localhost
sec-ch-ua: "Not_A Brand";v="99", "Chromium";v="142"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Accept-Language: zh-CN,zh;q=0.9
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/142.0.0.0 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Referer: http://localhost/intern/admin/admin.php
Accept-Encoding: gzip, deflate, br
Cookie: PHPSESSID=67l3m5trr6l48dkoe6lsb3g72i
Connection: keep-alive
```

![image-20260107001531232](https://github.com/xkalami-Tta0/picx-images-hosting/raw/master/Intern-Membership-Management-System/image-20260107001531232.5tric4hghp.webp)
